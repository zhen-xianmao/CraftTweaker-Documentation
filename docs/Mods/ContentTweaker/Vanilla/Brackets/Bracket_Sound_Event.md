# 声音事件

这个尖括号引用允许你引用一个在游戏中的声音事件  
点[这里](https://minecraft.gamepedia.com/Sounds.json)查看原版的所有声音事件!  


你需要这样引用声音事件:

原版:
```
<soundevent:name>

<soundevent:ambient.cave>
```
Mod:
```
<soundevent:modID:name>

<soundevent:minecraft:ambient.cave>
```

如果这个声音类型被找到,就会返回一个[ISoundEventDefinition](/Mods/ContentTweaker/Vanilla/Types/Sound/ISoundEventDefinition)对象
