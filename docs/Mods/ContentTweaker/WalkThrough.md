# 实践

## 安装之后
让我们开篇点题. 在开始创建方块和其他的之前, 你应该需要运行一次游戏使ContentTweaker的安装生效. 这将让ContentTweaker创建所谓它需要的"资源文件夹".

## 那些重要的文件夹
在你经过上述操作后,ContentTweaker会在.minecraft文件夹内创建名为 `resources` 的资源文件夹. ContentTweaker将会从这个文件夹内读入所有资源.包括但不限于:
- 所有的模型  
- 材质  
- 语言文件(lang)

之后将会对该文件夹中的更多内容进行详细的说明. 如果你需要在ZenScripts脚本中调用ContentTweaker,请在文件头加入 ```#loader contenttweaker``` 以调用ContentTweaker.

## 你的第一个方块
为了让你更了解ContentTweaker在CraftTweaker中是怎么工作的,我将把基本的内容展出,比如创建一个方块. 虽然还有很多的东西可以展示,但我不会在这里展示. 首先,我将创建一个方块.这些方法你能在wiki的其他页上找到.
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
这将创建一个属性类似Minecraft的冰块的方块,将这个脚本放入"scripts"文件夹,并遵守CraftTweaker脚本相同的规则. 

## 资源
你需要一个文件后缀为 `png` 的文件作为刚才这个冰块的材质.将它放入 `resources/contenttweaker/textures/blocks` 文件夹. (如果你已经将ContentTweaker加载,这个文件夹应该已经创建了) zs文件的名称应该和你输入的"名称"相对应,也就是一致.
例如:刚才写入的名称是 `anti_ice` ,那文件名应是 `anti_ice.png`. 
如果你准备在这个方块定义里不使用某些必要的数据, ContentTweaker将会使用默认的数据以保证其正常运行.  
[语言文件也属于资源](https://minecraft-zh.gamepedia.com/%E8%B5%84%E6%BA%90%E5%8C%85). 按照常理,ContentTweaker已经生成了en_US.lang文件.你需要在该文件内使用 `tile.contenttweaker.<block_name>.name=Block name` 的格式来定义这个方块的displayName.例如: `tile.contenttweaker.anti_ice.name=Anti ice`  
这两者都是示例,你应该还可以使用ContentTweaker加载你的模型,材质,以及定义displayName
