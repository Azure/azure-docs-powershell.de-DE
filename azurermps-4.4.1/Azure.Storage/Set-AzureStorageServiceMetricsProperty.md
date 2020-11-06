---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503330"
---
# Set-AzureStorageServiceMetricsProperty

## Synopsis
Ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureStorageServiceMetricsProperty** " ändert die Metrik-Eigenschaften für den Azure-Speicherdienst.

## Beispiele

### Beispiel 1: Ändern von Metriken Eigenschaften für den BLOB-Dienst
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

Mit diesem Befehl werden die Metriken der Version 1,0 für den BLOB-Speicher auf eine Dienstebene geändert.
Für Azure Storage Service-Metriken werden die Einträge 10 Tage lang aufbewahrt.
Da dieser Befehl den *passthru* -Parameter angibt, zeigt der Befehl die geänderten Metrik-Eigenschaften an.

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

### -MetricsLevel
Gibt die metrikebene an, die der Azure-Speicher für den Dienst verwendet.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Keine
- Dienst
- ServiceAndApi

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricsType
Gibt einen Metriktyp an.
Mit diesem cmldet wird der Typ des Azure Storage Service-Metriken auf den Wert festgelegt, den dieser Parameter angibt.
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

### -PassThru
Gibt an, dass diese Cmdlets die aktualisierten Metriken-Eigenschaften zurückgeben.
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
Gibt die Anzahl der Tage an, für die der Azure-Speicherdienst metrikinformationen speichert.

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
Mit diesem Cmdlet werden die Metriken-Eigenschaften für den Diensttyp geändert, den dieser Parameter angibt.
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
Gibt die Version der Azure Storage-Metriken an.
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

### IStorageContext

Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.

## Ausgaben

### Microsoft. WindowsAzure. Storage. shared. Protocol. MetricsProperties

## Notizen

## Verwandte Links

[Get-AzureStorageServiceMetricsProperty](./Get-AzureStorageServiceMetricsProperty.md)

[Neu – AzureStorageContext](./New-AzureStorageContext.md)


