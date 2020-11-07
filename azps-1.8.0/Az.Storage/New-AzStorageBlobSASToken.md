---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 562f9e4fac97421c53e07c4789d16b23d90a5ae3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658827"
---
# New-AzStorageBlobSASToken

## Synopsis
Generiert ein SAS-Token für ein Azure Storage-BLOB.

## Syntax

### BlobNameWithPermission (Standard)
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### BlobPipelineWithPolicy
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BlobPipelineWithPermission
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BlobNameWithPolicy
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzStorageBlobSASToken** generiert ein SAS-Token (Shared Access Signature) für ein Azure Storage-BLOB.

## Beispiele

### Beispiel 1: Generieren eines BLOB-SAS-Tokens mit vollständiger BLOB-Berechtigung
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

In diesem Beispiel wird ein BLOB-SAS-Token mit vollständiger BLOB-Berechtigung generiert.

### Beispiel 2: Generieren eines BLOB-SAS-Tokens mit Lebensdauer
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

In diesem Beispiel wird ein BLOB-SAS-Token mit Lebensdauer generiert.

## Parameter

### -BLOB
Gibt den Speicher-BLOB-Namen an.

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudBlob
Gibt das **CloudBlob** -Objekt an.
Verwenden Sie das Cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) , um ein **CloudBlob** -Objekt abzurufen.

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Container
Gibt den Namen des Speichercontainers an.

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Gibt den Speicherkontext an.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Gibt an, wann die freigegebene zugriffssignatur abläuft.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.
Der Bereich ist inklusive.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Berechtigung
Gibt die Berechtigungen für ein Speicher-BLOB an. Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt. 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Richtlinien
Gibt eine Azure stored Access-Richtlinie an.

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protokoll
Gibt das für eine Anforderung zugelassene Protokoll an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
* HttpsOnly
* HttpsOrHttp der Standardwert ist HttpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Startzeit
Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.

```yaml
Type: System.Nullable`1[System.DateTime]
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

### Microsoft. WindowsAzure. Storage. BLOB. CloudBlob

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[Neu – AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)
