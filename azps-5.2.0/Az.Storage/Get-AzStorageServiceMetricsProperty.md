---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304192"
---
# Get-AzStorageServiceMetricsProperty

## SYNOPSIS
Ruft Metrikeigenschaften für den Azure Storage-Dienst ab.

## SYNTAX

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzStorageServiceMetricsProperty"** ruft Metrikeigenschaften für den Azure Storage Service ab.

## BEISPIELE

### Beispiel 1: Erhalten von Metrikeigenschaften für den Blob-Dienst
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Dieser Befehl ruft Metrikeigenschaften für den BLOB-Speicher für den Metriktyp "Stunde" ab.

## PARAMETERS

### -Context
Gibt einen Azure-Speicherkontext an.
Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
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
Dieses Cmdlet ruft die Metrikeigenschaften des Azure Storage Diensts für den von diesem Parameter angegebenen Metriktyp ab.
Die zulässigen Werte für diesen Parameter sind: "Hour" und "Minute".

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
Gibt den Speicherdiensttyp an.
Dieses Cmdlet ruft die Metrikeigenschaften für den Typ ab, den dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter sind:
- BLOB 
- Tabelle
- Warteschlange
- Datei Der Wert von "Datei" wird derzeit nicht unterstützt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzStorageContext](./New-AzStorageContext.md)

[Set-AzStorageServiceMetricsProperty](./Set-AzStorageServiceMetricsProperty.md)


