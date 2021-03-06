# VBoxDude

Version 0.0.0.6 - Add support for resolving disk UUID

```c#
    var vm = new VirtualBoxDude().VMFactory.CreateFromName("VirtualMachineName");
    var diskPaths = await vm.GetDiskPathsAsync();
    string diskUUID = await vm.GetDiskUuidAsync(diskPaths.First());
```

Version 0.0.0.5 - Fix method names

Version 0.0.0.4 - Get virtual disk paths

```c#
IEnumerable<string> listOfDiskPaths = await new VirtualBoxDude().VMFactory.CreateFromName("VirtualMachineName").GetDiskPathsAsync();
```

Version 0.0.0.3 - Import virtual machine from file

```c#
new VirtualBoxDude().VMFactory.ImportFromFile(@"C:\Some-OS-image.ova", "NewVirtualMachineName");
```

Version 0.0.0.2 - Functionality to start a VM

```c#
new VirtualBoxDude().VMFactory.CreateFromName("VirtualMachineName").Start();
```
