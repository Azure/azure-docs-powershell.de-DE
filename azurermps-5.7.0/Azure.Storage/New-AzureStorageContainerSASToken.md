---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
ms.openlocfilehash: 0e8ad44ebbd8a5585626de27317caa14b408f87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500662"
---
# New-AzureStorageContainerSASToken

## Synopsis
Generiert ein SAS-Token für einen Azure-Speichercontainer.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SasPolicy
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageContainerSASToken** generiert ein SAS-Token (Shared Access Signature) für einen Azure-Speichercontainer.

## Beispiele

### Beispiel 1: Generieren eines Container-SAS-Tokens mit der Berechtigung "vollständiger Container"
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

In diesem Beispiel wird ein Container-SAS-Token mit vollständiger Container Berechtigung generiert.

### Beispiel 2: generieren mehrerer Container-SAS-Tokens nach Pipeline
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

In diesem Beispiel werden mehrere Container-SAS-Token mithilfe der Pipeline generiert.

### Beispiel 3: Erstellen eines Container-SAS-Tokens mit Shared Access-Richtlinie
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

In diesem Beispiel wird ein Container-SAS-Token mit einer gemeinsamen Zugriffsrichtlinie generiert.

## Parameter

### -Context
Gibt einen Azure-Speicherkontext an.
Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.

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

### -ExpiryTime
Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.

Wenn der Benutzer die Startzeit, aber nicht die Ablaufzeit festlegt, wird die Ablaufzeit auf die Startzeit plus eine Stunde festgelegt.
Wenn weder die Startzeit noch die Ablaufzeit angegeben ist, wird die Verfallszeit auf die aktuelle Uhrzeit plus eine Stunde festgelegt.

```yaml
Type: DateTime
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
Type: SwitchParameter
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen eines Azure-Speichercontainers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Berechtigung
Gibt Berechtigungen für einen Speichercontainer an.

```yaml
Type: String
Parameter Sets: SasPermission
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
Type: String
Parameter Sets: SasPolicy
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
* HttpsOrHttp

Der Standardwert ist HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
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
Type: DateTime
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

### Zeichenfolge

Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Neu – AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)
