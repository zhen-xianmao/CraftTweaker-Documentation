# 方块

这个尖括号引用支持使你能够使用它来引用一个在游戏中的方块. 它只能引用已经在游戏中注册的方块,所以请注意,如果使用它引用了一个来自于mod的方块后,添加或删除这个mod会造成一系列问题
方块通常是这么引用的:

```
<block:modID:blockName>

<block:minecraft:dirt>
```

如果这个方块被CraftTweaker找到,他会返回一个 [ICTBlockState](/Mods/ContentTweaker/Vanilla/Types/Block/ICTBlockState) 对象. 
Please refer to the [respective Wiki entry](/Mods/ContentTweaker/Vanilla/Types/Block/ICTBlockState) for further information on what you can do with th
请参考[相应的Wiki条目](/Mods/ContentTweaker/Vanilla/Types/Block/ICTBlockState),以获得有关这些内容的详细信息.
