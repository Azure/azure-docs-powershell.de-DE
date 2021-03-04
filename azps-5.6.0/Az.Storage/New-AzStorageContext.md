---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944519"
---
# New-AzStorageContext

## SYNOPSIS
Erstellt einen Azure Storage-Kontext.

## SYNTAX

### OAuthAccount (Standard)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzStorageContext** erstellt einen Azure Storage-Kontext.
Die Standardauthentifizierung eines Speicherkontexts ist OAuth (Azure AD), sofern nur der Name des Speicherkontos eingegeben wird.
Details zur Authentifizierung des Speicherdiensts finden Sie in https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services .

## BEISPIELE

### Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkontonamens und -schlüssels
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Mit diesem Befehl wird ein Kontext für das Konto namens ContosoGeneral erstellt, das den angegebenen Schlüssel verwendet.

### Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Mit diesem Befehl wird ein Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral erstellt.

### Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Mit diesem Befehl wird ein Kontext für die anonyme Verwendung für das Konto namens ContosoGeneral erstellt.
Der Befehl gibt HTTP als Verbindungsprotokoll an.

### Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen Entwicklungsspeicherkontos
```
PS C:\>New-AzStorageContext -Local
```

Mit diesem Befehl wird mithilfe des lokalen Entwicklungsspeicherkontos ein Kontext erstellt.
Der Befehl gibt den Parameter *Local* an.

### Beispiel 5: Container für das lokale Entwicklerspeicherkonto
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

Dieser Befehl erstellt mithilfe des lokalen Entwicklungsspeicherkontos einen Kontext und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das **Get-AzStorageContainer-Cmdlet.**
Der Befehl ruft den Azure Storage-Container für das lokale Entwicklerspeicherkonto ab.

### Beispiel 6: Mehrere Container erhalten
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Der erste Befehl erstellt einen Kontext mithilfe des lokalen Entwicklungsspeicherkontos und speichert diesen Kontext dann in der $Context 01.
Der zweite Befehl erstellt einen Kontext für das Konto namens ContosoGeneral, das den angegebenen Schlüssel verwendet, und speichert diesen Kontext dann in der $Context 02-Variable.
Der letzte Befehl ruft die Container für die Kontexte ab, die in $Context 01 und $Context 02 gespeichert sind, indem **Get-AzStorageContainer verwendet wird.**

### Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Mit diesem Befehl wird ein Azure Storage-Kontext erstellt, der den angegebenen Speicherendpunkt hat.
Der Befehl erstellt den Kontext für das Konto namens ContosoGeneral, das den angegebenen Schlüssel verwendet.

### Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.
Der Befehl erstellt den Kontext für das Konto namens ContosoGeneral, das den angegebenen Schlüssel verwendet.

### Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Der erste Befehl generiert ein SAS-Token mithilfe des **Cmdlets New-AzStorageContainerSASToken** für den Container namens ContosoMain und speichert dieses Token dann in der variablen $SasToken.
Dieses Token ist zum Lesen, Hinzufügen, Aktualisieren und Löschen von Berechtigungen.
Der zweite Befehl erstellt einen Kontext für das Konto namens ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet und diesen Kontext dann in der $Context speichert.
Der letzte Befehl listet alle blobs auf, die dem Container "ContosoMain" zugeordnet sind, indem der kontextbezogene Kontext verwendet wird, der in $Context.

### Beispiel 10: Erstellen eines Kontexts mithilfe der OAuth-Authentifizierung
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Mit diesem Befehl wird mithilfe der OAuth (Azure AD)-Authentifizierung ein Kontext erstellt.

## PARAMETER

### -Anonym
Gibt an, dass mit diesem Cmdlet ein Azure Storage-Kontext für die anonyme Anmeldung erstellt wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Gibt eine Verbindungszeichenfolge für den Azure Storage-Kontext an.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpunkt
Gibt den Endpunkt für den Azure Storage-Kontext an.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Umgebung
Gibt die Azure-Umgebung an.
Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.
Weitere Informationen finden Sie unter `Get-Help Get-AzEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Gibt an, dass dieses Cmdlet mithilfe des lokalen Entwicklungsspeicherkontos einen Kontext erstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Transfer Protocol (https/http).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Gibt ein SAS-Token (Shared Access Signature) für den Kontext an.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Gibt einen Azure Storage-Kontoschlüssel an.
Dieses Cmdlet erstellt einen Kontext für den Schlüssel, den dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Gibt einen Azure Storage-Kontonamen an.
Dieses Cmdlet erstellt einen Kontext für das Konto, das dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Gibt an, dass mit diesem Cmdlet ein Azure Storage-Kontext mit der OAuth (Azure AD)-Authentifizierung erstellt wird.
Das Cmdlet verwendet standardmäßig die OAuth-Authentifizierung, wenn keine andere Authentifizierung angegeben ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
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

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## NOTIZEN

## VERWANDTE LINKS

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


