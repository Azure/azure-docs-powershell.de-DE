---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497737"
---
# Get-AzureRmDisk

## Synopsis
Ruft die Eigenschaften eines Datenträgers ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDisk** " Ruft die Eigenschaften eines Datenträgers ab.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

Dieser Befehl ruft die Eigenschaften des Datenträgers mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" ab.

### Beispiel 2
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

Dieser Befehl ruft die Eigenschaften aller Datenträger in der Ressourcengruppe "ResourceGroup01" ab.

### Beispiel 3
```
PS C:\> Get-AzureRmDisk
```

Mit diesem Befehl werden die Eigenschaften aller Datenträger unter dem Abonnement abgerufen.

## Parameter

### -Daten Trägername
Gibt den Namen eines Datenträgers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList

## Notizen

## Verwandte Links

