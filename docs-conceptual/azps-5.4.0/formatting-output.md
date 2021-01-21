---
title: Formatieren der Ausgabe von Azure PowerShell-Cmdlets
description: Anleitung zum Formatieren der Cmdlet-Ausgabe für Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 44016cc9546869b05693276293119c21ca02e4b0
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573687"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="fb4cd-103">Formatieren der Ausgabe von Azure PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb4cd-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="fb4cd-104">Standardmäßig wird die Ausgabe für jedes Azure PowerShell-Cmdlet so formatiert, dass sie leicht zu lesen ist.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="fb4cd-105">Mit PowerShell können Sie die Ausgabe von Cmdlets konvertieren oder formatieren, indem Sie sie per Pipezeichen mit einem der folgenden Cmdlets verknüpfen:</span><span class="sxs-lookup"><span data-stu-id="fb4cd-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="fb4cd-106">Formatierung</span><span class="sxs-lookup"><span data-stu-id="fb4cd-106">Formatting</span></span>      | <span data-ttu-id="fb4cd-107">Konvertierung</span><span class="sxs-lookup"><span data-stu-id="fb4cd-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="fb4cd-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="fb4cd-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="fb4cd-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="fb4cd-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="fb4cd-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="fb4cd-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="fb4cd-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="fb4cd-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="fb4cd-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="fb4cd-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="fb4cd-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="fb4cd-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="fb4cd-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="fb4cd-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="fb4cd-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="fb4cd-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="fb4cd-116">Die Formatierung wird zum Anzeigen in einem PowerShell-Terminal verwendet, und die Konvertierung wird zum Generieren von Daten eingesetzt, damit diese von anderen Skripts oder Programmen genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="fb4cd-117">Tabellenausgabeformat</span><span class="sxs-lookup"><span data-stu-id="fb4cd-117">Table output format</span></span>

<span data-ttu-id="fb4cd-118">Die Ausgabe von Azure PowerShell-Cmdlets erfolgt standardmäßig im Tabellenformat.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="fb4cd-119">In diesem Format werden nicht alle Informationen der angeforderten Ressource angezeigt:</span><span class="sxs-lookup"><span data-stu-id="fb4cd-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="fb4cd-120">Die Breite Ihres Fensters mit der PowerShell-Sitzung kann sich darauf auswirken, welche Datenmenge für `Format-Table` angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="fb4cd-121">Um die Ausgabe auf bestimmte Eigenschaften zu beschränken und zu sortieren, können Eigenschaftennamen als Argumente für `Format-Table` bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="fb4cd-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="fb4cd-122">Ausgabeformat „List“</span><span class="sxs-lookup"><span data-stu-id="fb4cd-122">List output format</span></span>

<span data-ttu-id="fb4cd-123">Beim Ausgabeformat „List“ (Liste) werden zwei Spalten erstellt, die den Eigenschaftennamen bzw. den zugehörigen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="fb4cd-124">Für komplexe Objekte wird stattdessen der Typ des Objekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="fb4cd-125">In der folgenden Ausgabe wurden einige Felder entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="fb4cd-126">Wie bei `Format-Table` auch, können Eigenschaftennamen angegeben werden, um die Ausgabe zu sortieren und zu beschränken:</span><span class="sxs-lookup"><span data-stu-id="fb4cd-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="fb4cd-127">Ausgabeformat „Wide“</span><span class="sxs-lookup"><span data-stu-id="fb4cd-127">Wide output format</span></span>

<span data-ttu-id="fb4cd-128">Beim Ausgabeformat „Wide“ (Breit) wird nur ein Eigenschaftenname pro Abfrage erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="fb4cd-129">Indem eine Eigenschaft als Argument angegeben wird, kann gesteuert werden, welche Eigenschaft angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="fb4cd-130">Ausgabeformat „Custom“</span><span class="sxs-lookup"><span data-stu-id="fb4cd-130">Custom output format</span></span>

<span data-ttu-id="fb4cd-131">Der Ausgabetyp `Custom-Format` dient zum Formatieren von benutzerdefinierten Objekten.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="fb4cd-132">Ohne Argumente entspricht das Verhalten `Format-List`, aber es werden die Eigenschaftennamen von benutzerdefinierten Klassen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="fb4cd-133">In der folgenden Ausgabe wurden einige Felder entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="fb4cd-134">Wenn Eigenschaftennamen als Argumente für `Custom-Format` angegeben werden, werden die Eigenschaft/Wert-Paare für den Satz mit benutzerdefinierten Objekten als Werte angezeigt:</span><span class="sxs-lookup"><span data-stu-id="fb4cd-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="fb4cd-135">In der folgenden Ausgabe wurden einige Felder entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="fb4cd-136">Konvertierung in andere Datenformate</span><span class="sxs-lookup"><span data-stu-id="fb4cd-136">Conversion to other data formats</span></span>

<span data-ttu-id="fb4cd-137">Die Cmdlet-Familie `ConvertTo-*` ermöglicht das Konvertieren der Ergebnisse von Azure PowerShell-Cmdlets in computerlesbare Formate.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="fb4cd-138">Verwenden Sie den Befehl `Select-Object` mit einem Pipezeichen, bevor Sie die Konvertierung durchführen, um nur einige Eigenschaften aus den Azure PowerShell-Ergebnissen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="fb4cd-139">In den folgenden Beispielen werden die unterschiedlichen Ausgabearten veranschaulicht, die bei der Konvertierung jeweils erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="fb4cd-140">Konvertierung in CSV</span><span class="sxs-lookup"><span data-stu-id="fb4cd-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="fb4cd-141">Konvertierung in JSON</span><span class="sxs-lookup"><span data-stu-id="fb4cd-141">Conversion to JSON</span></span>

<span data-ttu-id="fb4cd-142">In der JSON-Ausgabe werden standardmäßig nicht alle Eigenschaften erweitert.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="fb4cd-143">Verwenden Sie das Argument `-Depth`, um die Tiefe für die Erweiterung der Eigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="fb4cd-144">Standardmäßig wird die Erweiterungstiefe `2` verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="fb4cd-145">In der folgenden Ausgabe wurden einige Felder entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="fb4cd-146">Konvertierung in XML</span><span class="sxs-lookup"><span data-stu-id="fb4cd-146">Conversion to XML</span></span>

<span data-ttu-id="fb4cd-147">Mit dem Cmdlet `ConvertTo-XML` wird das Azure PowerShell-Antwortobjekt in ein reines XML-Objekt konvertiert, das wie jedes andere XML-Objekt in PowerShell verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="fb4cd-148">Konvertierung in HTML</span><span class="sxs-lookup"><span data-stu-id="fb4cd-148">Conversion to HTML</span></span>

<span data-ttu-id="fb4cd-149">Beim Konvertieren eines Objekts in HTML wird eine Ausgabe erzeugt, die als HTML-Tabelle gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="fb4cd-150">Das Rendern der HTML-Daten richtet sich danach, wie Ihr Browser Tabellen rendert, die keine Informationen zur Breite enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="fb4cd-151">Es werden keine Objekte erweitert, bei denen es sich um benutzerdefinierte Klassen handelt.</span><span class="sxs-lookup"><span data-stu-id="fb4cd-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```
