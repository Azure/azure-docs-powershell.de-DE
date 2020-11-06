---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497729"
---
# Get-AzureRmSnapshot

## Synopsis
Ruft die Eigenschaften eines Snapshots ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSnapshot** " Ruft die Eigenschaften eines Snapshots ab.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmSnapshot
```

Dieser Befehl ruft die Eigenschaften aller Snapshots des Abonnements ab.

### Beispiel 2
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

Dieser Befehl ruft die Eigenschaften aller Schnappschüsse in der Ressourcengruppe mit dem Namen "ResourceGroupName1" ab.

### Beispiel 3
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

Mit diesem Befehl werden die Eigenschaften des Snapshots mit dem Namen "SnapshotName1" in der Ressourcengruppe "ResourceGroupName1" abgerufen.

## Parameter

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

### -Snapshotname
Gibt den Namen eines Schnappschusses an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### System. Object

## Notizen

## Verwandte Links

