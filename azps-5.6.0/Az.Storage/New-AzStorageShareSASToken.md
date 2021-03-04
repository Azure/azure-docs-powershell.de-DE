---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: b55ab1d87fa63523b35077243d8b9b4f00ba5d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944470"
---
# New-AzStorageShareSASToken

## SYNOPSIS
Generieren eines Tokens für die Gemeinsame Zugriffssignatur für azure storage share.

## SYNTAX

### SasPolicy
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SasPermission
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzStorageShareSASToken** generiert ein Token für die Signatur für den freigegebenen Zugriff für eine Azure Storage-Freigabe.

## BEISPIELE

### Beispiel 1: Generieren eines Signaturtokens für den freigegebenen Zugriff für eine Freigabe
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

Mit diesem Befehl wird ein Signaturtoken für den freigegebenen Zugriff für die Freigabe namens ContosoShare erstellt.

### Beispiel 2: Generieren eines Signaturtokens für mehrere freigegebene Zugriffe mithilfe der Pipeline
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

Dieser Befehl ruft alle Speicherfreigaben ab, die dem Präfixtest entsprechen.
Der Befehl übergibt sie mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet erstellt ein freigegebenes Zugriffstoken für jede Speicherfreigabe, die über die angegebenen Berechtigungen verfügt.

### Beispiel 3: Generieren eines Signaturtokens für den freigegebenen Zugriff, das eine Richtlinie für den freigegebenen Zugriff verwendet
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

Mit diesem Befehl wird ein Signaturtoken für den freigegebenen Zugriff für die Speicherfreigabe namens ContosoShare mit der Richtlinie "ContosoPolicy03" erstellt.

## PARAMETER

### -Context
Gibt einen Azure Storage-Kontext an.
Verwenden Sie das cmdlet New-AzStorageContext, um einen Kontext zu erhalten.

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

### -ExpiryTime
Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff ungültig wird.

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
Gibt an, dass dieses Cmdlet den vollständigen Blob-URI und das Signaturtoken für den freigegebenen Zugriff zurückgibt.

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
Gibt die IP-Adresse oder den Bereich der IP-Adressen an, über die Anforderungen akzeptiert werden können, z. B. 168.1.5.65 oder 168.1.5.60-168.1.5.70.
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

### -Permission
Gibt die Berechtigungen im Token für den Zugriff auf die Freigabe und die Dateien unter der Freigabe an.
Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für Lesen, Schreiben und Löschen) handelt.

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Richtlinie
Gibt die gespeicherte Zugriffsrichtlinie für eine Freigabe an.

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Gibt das Protokoll an, das für eine Anforderung zulässig ist.
Die zulässigen Werte für diesen Parameter sind:
* HttpsOnly
* HttpsOrhttp Der Standardwert ist HttpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
Gibt den Namen der Speicherfreigabe an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StartTime
Gibt den Zeitpunkt an, zu dem die Signatur für den freigegebenen Zugriff gültig wird.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### System.String

## NOTIZEN
* Schlüsselwörter: common, azure, services, data, storage, blob, queue, table

## VERWANDTE LINKS

[Get-AzStorageShare](./Get-AzStorageShare.md)

[New-AzStorageFileSASToken](./New-AzStorageFileSASToken.md)
