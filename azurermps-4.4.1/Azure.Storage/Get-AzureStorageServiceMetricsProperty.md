---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477517"
---
# Get-AzureStorageServiceMetricsProperty

## Synopsis
Ruft Metrik-Eigenschaften für den Azure-Speicherdienst ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageServiceMetricsProperty** " ruft Metrics-Eigenschaften für den Azure-Speicherdienst ab.

## Beispiele

### Beispiel 1: Abrufen von Metriken Eigenschaften für den BLOB-Dienst
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Dieser Befehl ruft Metrik-Eigenschaften für den BLOB-Speicher für den Typ der Stunden Metrik ab.

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

### -MetricsType
Gibt einen Metriktyp an.
Mit diesem Cmdlet werden die Eigenschaften des Azure Storage Service-Metriken für den Metriktyp abgerufen, den dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Gibt den Typ des Speicher Diensts an.
Dieses Cmdlet ruft die Metrik-Eigenschaften für den Typ ab, den dieser Parameter angibt.
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

### IStorageContext

Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.

## Ausgaben

### Microsoft. WindowsAzure. Storage. shared. Protocol. MetricsProperties

## Notizen

## Verwandte Links

[Neu – AzureStorageContext](./New-AzureStorageContext.md)

[Satz-AzureStorageServiceMetricsProperty](./Set-AzureStorageServiceMetricsProperty.md)


