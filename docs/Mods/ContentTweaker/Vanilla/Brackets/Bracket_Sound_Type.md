# 声音类型


这个尖括号引用允许你引用一个在游戏中的声音类型
目前支持的声音类型有:

<details>
	<summary>单击该处以查看目前支持的声音类型</summary>
	<ul>
		<li>Wood(木头)</li>
		<li>Ground(泥土)</li>
		<li>Plant(杂草)</li>
		<li>Stone(石头)</li>
		<li>Metal(金属)</li>
		<li>Glass(玻璃)</li>
		<li>Cloth(皮革)</li>
		<li>Sand(沙子)</li>
		<li>Snow(雪)</li>
		<li>Ladder(楼梯)</li>
		<li>Anvil(铁砧)</li>
		<li>Slime(史莱姆)</li>
	</ul>
</details>

若想引用一个声音类型,你需要这么做:

```
<soundtype:name>

<soundtype:wood>
```

如果你输入的声音类型能被CraftTweaker在游戏中找到,他将返回一个 [ISoundTypeDefinition](/Mods/ContentTweaker/Vanilla/Types/Sound/ISoundTypeDefinition) 对象
