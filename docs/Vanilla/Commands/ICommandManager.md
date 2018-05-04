# 命令管理器

命令管理器是CT提供的,管理命令提供的接口. 因此,你可以使用命令管理器来获取和执行命令.  
你可以从一个 [IServer](/Vanilla/Game/IServer) 对象获取关于它的信息.

## 导入这个模块
为了避免发生一些不期而遇的问题(比如声明数组),最为安全,也是最为推荐的方式就是导入相关的模块. 
`import crafttweaker.commands.ICommandManager;`

## ZenGetters

| ZenGetter | 类型                               |
|-----------|------------------------------------|
| commands  | Map<String, [ICommand](ICommand)\> |


## ZenMethods
- int executeCommand([ICommandSender](ICommandSender) sender, String rawCommand);
- List<String\> getTabCompletions([ICommandSender](ICommandSender) sender, String input, @Optional [IBlockPos](/Vanilla/World/IBlockPos) pos);
- List<[ICommand](ICommand)\> getPossibleCommands([ICommandSender](ICommandSender) sender);
