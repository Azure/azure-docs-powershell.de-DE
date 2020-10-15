---
title: Abfragen der Ausgabe von Azure PowerShell-Cmdlets
description: Hier erfahren Sie, wie Sie in Azure Ressourcenabfragen ausführen und die Ergebnisse formatieren.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2754df5132ca9d528217fa5caad95b7f59cc8215
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002008"
---
# <a name="query-output-of-azure-powershell"></a>Abfrageausgabe von Azure PowerShell 

Das Ergebnis eines Azure PowerShell-Cmdlets ist ein Azure PowerShell-Objekt. Auch Cmdlets, die keine expliziten `Get-`-Vorgänge sind, können einen Wert zurückgeben, der überprüft werden kann, um Informationen zu einer erstellten oder geänderten Ressource zu erhalten. Die meisten Cmdlets geben ein einzelnes Objekt zurück. Manche Cmdlets geben jedoch ein Array zurück, das durchlaufen werden sollte.

In fast allen Fällen wird die Abfrageausgabe von Azure PowerShell mit dem Cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) zu `select` abgekürzt. Die Ausgabe kann mit [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) oder dem entsprechenden Alias `where` gefiltert werden.

## <a name="select-simple-properties"></a>Auswählen einfacher Eigenschaften

Im Standardtabellenformat zeigen Azure PowerShell-Cmdlets nicht alle verfügbaren Eigenschaften an. Sie können die vollständigen Eigenschaften mithilfe des Cmdlets [Format-List](/powershell/module/microsoft.powershell.utility/format-list) oder durch Weiterleiten der Ausgabe an `Select-Object *` abrufen:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

Wenn Ihnen die Namen der für Sie relevanten Eigenschaften bekannt sind, können Sie diese Eigenschaftennamen mit `Select-Object` verwenden, um sie direkt abzurufen:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

Die Ausgabe für `Select-Object` ist immer zur Anzeige der angeforderten Informationen formatiert. Informationen zur Verwendung der Formatierung beim Abfragen von Cmdlet-Ergebnissen finden Sie unter [Format Azure PowerShell cmdlet output](formatting-output.md) (Formatieren der Ausgabe von Azure PowerShell-Cmdlets).

## <a name="select-nested-properties"></a>Auswählen geschachtelter Eigenschaften

Einige Eigenschaften in der Ausgabe von Azure PowerShell-Cmdlets verwenden geschachtelte Objekte, z. B. die `StorageProfile`-Eigenschaft der Ausgabe von `Get-AzVM`. Um einen Wert aus einer geschachtelten Eigenschaft abzurufen, geben Sie einen Anzeigenamen und den vollständigen Pfad des Werts an, den Sie als Teil eines Wörterbucharguments für `Select-Object` überprüfen möchten:

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

Jedes Wörterbuchargument wählt eine Eigenschaft des Objekts aus. Die zu extrahierende Eigenschaft muss Teil eines Ausdrucks sein.

## <a name="filter-results"></a>Ergebnisse filtern 

Mit dem Cmdlet `Where-Object` können Sie das Ergebnis auf der Grundlage eines beliebigen Eigenschaftswerts filtern (einschließlich geschachtelter Eigenschaften). Das nächste Beispiel zeigt, wie Sie mit `Where-Object` nach den Linux-VMs in einer Ressourcengruppe suchen.

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

Die Ergebnisse von `Select-Object` und `Where-Object` können aneinander weitergeleitet werden. Aus Leistungsgründen wird empfohlen, den `Where-Object`-Vorgang immer vor `Select-Object` zu platzieren:

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
