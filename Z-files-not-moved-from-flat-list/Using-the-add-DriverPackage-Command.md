---
title: Using the add-DriverPackage Command
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3ac9e8d5-63ec-4ce8-86fc-85d28011050b
---
# Using the add-DriverPackage Command
Adds a driver package to the server.  
  
## Syntax  
  
```  
WDSUTIL /Add-DriverPackage /InfFile:<Inf File path> [/Server:<Server name>] [/Architecture:{x86 | ia64 | x64}] [/DriverGroup:<Group Name>] [/Name:<Friendly Name>]  
```  
  
## Parameters  
  
|Parameter|Description|  
|-------------|---------------|  
|InfFile:<Inf File path>|Specifies the full path of the .inf file to add.|  
|\/Server:<Server name>|Specifies the name of the server. This can be the NetBIOS name or the FQDN. If no server name is specified, the local server is used.|  
|\/Architecture:{x86 &#124; ia64 &#124; x64}|Specifies the architecture of the driver package.|  
|\[\/DriverGroup:<Group Name>\]|Specifies the name of the driver group to which the package should be added.|  
|\[\/Name:<Friendly Name>\]|States the friendly name for the driver package.|  
  
## <a name="BKMK_examples"></a>Examples  
To add a driver package, type one of the following:  
  
```  
WDSUTIL /verbose /Add-DriverPackage /InfFile:"C:\Temp\Display.inf"  
```  
  
```  
WDSUTIL /Add-DriverPackage /Server:MyWDSServer /InfFile:"C:\Temp\Display.inf" /Architecture:x86 /DriverGroup:x86Drivers /Name:"Display Driver”  
```  
  
#### Additional references  
[Command-Line Syntax Key](Command-Line-Syntax-Key.md)  
  
[Using the add-AllDriverPackages subcommand]()  
  
