---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 7bca28da7b4729a414fafc5268bc4e0e02ee3c72
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843056"
---
# Get-AzStorageServiceMetricsProperty

## Synopsis
Ruft Metrik-Eigenschaften für den Azure-Speicherdienst ab.

## Syntax

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStorageServiceMetricsProperty** " ruft Metrics-Eigenschaften für den Azure-Speicherdienst ab.

## Beispiele

### Beispiel 1: Abrufen von Metriken Eigenschaften für den BLOB-Dienst
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Dieser Befehl ruft Metrik-Eigenschaften für den BLOB-Speicher für den Typ der Stunden Metrik ab.

## Parameter

### -Context
Gibt einen Azure-Speicherkontext an.
Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricsType
Gibt einen Metriktyp an.
Mit diesem Cmdlet werden die Eigenschaften des Azure Storage Service-Metriken für den Metriktyp abgerufen, den dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter lauten: Stunde und Minute.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
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
- Datei der Wert der Datei wird derzeit nicht unterstützt.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAz. Storage. shared. Protocol. MetricsProperties

## Notizen

## Verwandte Links

[Neu – AzStorageContext](./New-AzStorageContext.md)

[Satz-AzStorageServiceMetricsProperty](./Set-AzStorageServiceMetricsProperty.md)


