# 实践

## 安装之后
让我们开篇点题. 在开始创建方块和其他的之前, 你应该运行一次游戏使ContentTweaker的安装生效. 这将让ContentTweaker创建它需要的文件夹.

## 重要的文件夹
在你经过上述操作后,ContentTweaker会在.minecraft文件夹内创建名为 `resources` 的资源文件夹. ContentTweaker将会从这个文件夹内读入所有资源.包括但不限于:
- 所有的模型  
- 材质  
- 语言文件(lang)

之后将会对该文件夹中的更多内容进行详细的说明.  
如果你需要在ZenScripts脚本中调用ContentTweaker,你需要在文件头加入 ```#loader contenttweaker``` .  

## 第一个方块
为了让你更了解ContentTweaker在CraftTweaker中是怎么工作的,我将把基本的内容展示. 我将使用ContentTweaker创建一个方块. 虽然还有很多东西可以展示,但我并不会这样做. 我将创建一个方块. 如果你想找到这些方法的意义和作用,你可以去翻阅wiki的其他页.  
```
#loader contenttweaker

import mods.contenttweaker.VanillaFactory;
import mods.contenttweaker.Block;

var antiIceBlock = VanillaFactory.createBlock("anti_ice", <blockmaterial:ice>);
antiIceBlock.setLightOpacity(3);
antiIceBlock.setLightValue(0);
antiIceBlock.setBlockHardness(5.0);
antiIceBlock.setBlockResistance(5.0);
antiIceBlock.setToolClass("pickaxe");
antiIceBlock.setToolLevel(0);
antiIceBlock.setBlockSoundType(<soundtype:snow>);
antiIceBlock.setSlipperiness(0.3);
antiIceBlock.register();
```
这将创建一个方块,它的属性类似Minecraft的冰块.将这个脚本放入"scripts"文件夹,并遵守与CraftTweaker脚本相同的规则. 

## 资源
你需要一个文件后缀为 `png` 的图片文件作为刚才创建的这个方块的材质.将它放入 `resources/contenttweaker/textures/blocks` 文件夹. (如果你已经将ContentTweaker加载,这个文件夹应该已经创建了) png文件的名称应该要和你刚才输入的 `方块名称` 一致.
例如:刚才写入的方块名称是 `anti_ice` ,那这个图片的文件名应是 `anti_ice.png`.  
如果你打算在这个方块栈里不使用某些必要的数据, ContentTweaker将会使用默认的数据以保证正常运行.  
[语言文件也属于资源](https://minecraft-zh.gamepedia.com/%E8%B5%84%E6%BA%90%E5%8C%85). 按照常理,ContentTweaker已经生成了en_US.lang文件.你需要在这个lang语言文件内使用 `tile.contenttweaker.<block_name>.name=Block name` 的格式来定义这个方块的displayName.例如: `tile.contenttweaker.anti_ice.name=Anti ice`  
此外,en_US.lang是游戏在语言为English时使用的语言文件,如果你要详细了解,我认为你应该去查查wiki.  
这两者都是示例,你应该还可以使用ContentTweaker加载你的模型,材质,以及定义displayName
