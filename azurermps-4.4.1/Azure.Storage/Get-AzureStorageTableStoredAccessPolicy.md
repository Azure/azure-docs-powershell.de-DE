---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662287"
---
# Get-AzureStorageTableStoredAccessPolicy

## Synopsis
Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageTableStoredAccessPolicy** " listet die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle auf.

## Beispiele

### Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy50 in der Speichertabelle mit dem Namen Table02 ab.

### Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einer Speichertabelle
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen Table02 ab.

## Parameter

### -Context
Gibt den Azure-Speicherkontext an.
Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Richtlinien
Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.

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

### -Tabelle
Gibt den Namen der Azure-Speichertabelle an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### IStorageContext

Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.

### Zeichenfolge

Der Parameter "Tabelle" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

### Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy

## Notizen

## Verwandte Links

[Neu – AzureStorageTableStoredAccessPolicy](./New-AzureStorageTableStoredAccessPolicy.md)

[Remove-AzureStorageTableStoredAccessPolicy](./Remove-AzureStorageTableStoredAccessPolicy.md)

[Satz-AzureStorageTableStoredAccessPolicy](./Set-AzureStorageTableStoredAccessPolicy.md)

[Neu – AzureStorageContext](./New-AzureStorageContext.md)


