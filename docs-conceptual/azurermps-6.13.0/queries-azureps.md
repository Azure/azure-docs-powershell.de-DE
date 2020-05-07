---
title: Abfragen der Ausgabe von Azure PowerShell-Cmdlets
description: Hier erfahren Sie, wie Sie in Azure Ressourcenabfragen ausführen und die Ergebnisse formatieren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: b6f0b01fa38ae4484fe9706e739b12b229b57661
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534499"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Abfragen der Ausgabe von Azure PowerShell-Cmdlets

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Abfragen können in PowerShell mithilfe integrierter Cmdlets ausgeführt werden. Cmdlet-Namen haben in PowerShell das Format **_Verb-Nomen_** . Die Abfrage-Cmdlets sind am Verb **_Get_** zu erkennen. Bei den Cmdlet-Nomen handelt es sich um die Arten von Azure-Ressourcen, für die eine dem Cmdlet-Verb entsprechende Aktion ausgeführt wird.

## <a name="select-simple-properties"></a>Auswählen einfacher Eigenschaften

In Azure PowerShell ist für jedes Cmdlet eine Standardformatierung definiert. Die am häufigsten verwendeten Eigenschaften für die einzelnen Ressourcentypen werden automatisch in einer Tabelle oder Liste angezeigt. Weitere Informationen zum Formatieren der Ausgabe finden Sie unter [Formatieren von Abfrageergebnissen](formatting-output.md).

Fragen Sie mithilfe des Cmdlets `Get-AzureRmVM` eine Liste mit virtuellen Computern in Ihrem Konto ab.

```azurepowershell-interactive
Get-AzureRmVM
```

Die Standardausgabe wird automatisch als Tabelle formatiert.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Mit dem Cmdlet `Select-Object` können Sie spezifische Eigenschaften auswählen, die für Sie von Interesse sind.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>Auswählen komplexer geschachtelter Eigenschaften

Wenn die gewünschte Eigenschaft in der JSON-Ausgabe verschachtelt ist, müssen Sie den vollständigen Pfad zur Eigenschaft angeben. Das folgende Beispiel zeigt, wie Sie den VM-Namen und den Betriebssystemtyp auf der Grundlage des Cmdlets `Get-AzureRmVM` auswählen.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Filtern von Ergebnissen mithilfe des Cmdlets „Where-Object“

Mit dem Cmdlet `Where-Object` können Sie das Ergebnis auf der Grundlage eines beliebigen Eigenschaftswerts filtern. Im folgenden Beispiel wählt der Filter nur virtuelle Computer aus, deren Name „RGD“ enthält.

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Im nächsten Beispiel werden die virtuellen Computer zurückgegeben, bei denen „vmSize“ den Wert „Standard_DS1_V2“ besitzt.

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```