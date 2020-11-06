---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475781"
---
# Set-AzureStorageServiceLoggingProperty

## Synopsis
Ändert die Protokollierung für Azure Storage Services.

## Syntax

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureStorageServiceLoggingProperty** " ändert die Protokollierung für Azure Storage-Dienste.

## Beispiele

### Beispiel 1: Ändern der Protokollierungseigenschaften für den BLOB-Dienst
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

Mit diesem Befehl wird die Version 1,0-Protokollierung für den BLOB-Speicher geändert, um Lese-und Schreibvorgänge einzubeziehen.
Die Azure-Speicherdienst Protokollierung speichert Einträge für 10 Tage.
Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Protokollierungseigenschaften an.

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

### -LoggingOperations
Gibt ein Array von Azure-Speicherdienst Vorgängen an.
Azure Storage Services protokolliert die Vorgänge, die dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Keine
- Lesen
- Schreiben
- Löschen
- Alle

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet die aktualisierten Protokollierungseigenschaften zurückgibt.
Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionDays
Gibt die Anzahl der Tage an, die der Azure-Speicherdienst protokollierte Informationen beibehält.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Gibt den Typ des Speicher Diensts an.
Mit diesem Cmdlet werden die Protokollierungseigenschaften des Diensttyps geändert, den dieser Parameter angibt.
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

### -Version
Gibt die Version der Azure-Speicherdienst Protokollierung an.
Der Standardwert ist 1,0.

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Get-AzureStorageServiceLoggingProperty](./Get-AzureStorageServiceLoggingProperty.md)

[Neu – AzureStorageContext](./New-AzureStorageContext.md)


