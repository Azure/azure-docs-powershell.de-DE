---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475666"
---
# Get-AzureStorageServiceLoggingProperty

## Synopsis
Ruft Protokollierungseigenschaften für Azure Storage Services ab.

## Syntax

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageServiceLoggingProperty** " Ruft die Protokollierungseigenschaften für Azure Storage Services ab.

## Beispiele

### Beispiel 1: Abrufen von Protokollierungseigenschaften für den BLOB-Dienst
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

Dieser Befehl ruft die Protokollierungseigenschaften für den BLOB-Speicher ab.

## Parameter

### -Context
Gibt einen Azure-Speicherkontext an.
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

### -ServiceType
Gibt den Typ des Speicher Diensts an.
Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- BLOB 
- Tabelle
- Warteschlange
- Datei

Der Wert der Datei wird derzeit nicht unterstützt.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureStorageContext](./New-AzureStorageContext.md)

[Satz-AzureStorageServiceLoggingProperty](./Set-AzureStorageServiceLoggingProperty.md)


