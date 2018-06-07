---
title: Formatieren von Abfrageergebnissen | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie in Azure Ressourcenabfragen ausführen und die Ergebnisse formatieren.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9cef703f302651a48381dba70c0be23d4d24df0b
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821767"
---
# <a name="formatting-query-results"></a>Formatieren von Abfrageergebnissen

Zur besseren Lesbarkeit der Ausgabe verfügt jedes PowerShell-Cmdlet standardmäßig über eine vordefinierte Formatierung.  Mit PowerShell ist es jedoch auch möglich, die Ausgabe anzupassen oder die Cmdlet-Ausgabe in ein anderes Format zu konvertieren. Hierzu stehen folgende Cmdlets zur Verfügung:

| Formatierung      | Konvertierung       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a>Formatierungsbeispiele

In diesem Beispiel rufen wir eine Liste mit virtuellen Azure-Computern in unserem Standardabonnement ab.  Bei dem Befehl „Get-AzureRmVM“ erfolgt die Ausgabe standardmäßig in einem Tabellenformat.

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Mit dem Cmdlet `Format-Table` können Sie die zurückgegebenen Spalten begrenzen. Im folgenden Beispiel rufen wir die gleiche Liste mit virtuellen Computern ab, beschränken die Ausgabe aber auf den Namen des virtuellen Computers, die Ressourcengruppe und den Standort des virtuellen Computers.  Der Parameter `-Autosize` passt die Größe der Spalten an die Größe der Daten an.

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

Informationen können bei Bedarf auch in einem Listenformat angezeigt werden. Das wird im folgenden Beispiel mit dem Cmdlet `Format-List` veranschaulicht.

```powershell
Get-AzureVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a>Konvertieren in andere Datentypen

PowerShell bietet außerdem mehrere Ausgabeformate für verschiedenste Anforderungen.  Im folgenden Beispiel rufen wir mithilfe des Cmdlets `Select-Object` Attribute der virtuellen Computer in unserem Abonnement ab und konvertieren die Ausgabe in das CSV-Format, um sie problemlos in eine Datenbank oder in eine Tabelle importieren zu können.

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

Die Ausgabe kann auch in das JSON-Format konvertiert werden.  Im folgenden Beispiel wird die gleiche Liste mit virtuellen Computern erstellt, die Ausgabe erfolgt jedoch im JSON-Format.

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
