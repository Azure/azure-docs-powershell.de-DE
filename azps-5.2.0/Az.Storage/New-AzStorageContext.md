---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304091"
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

### Local Durch
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzStorageContext"** erstellt einen Azure Storage-Kontext.
Die Standardauthentifizierung eines Speicherkontexts ist OAuth (Azure AD), wenn nur der Name des Speicherkontos eingegeben wird.
Details zur Authentifizierung des Speicherdiensts finden Sie https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services in.

## BEISPIELE

### Beispiel 1: Erstellen eines Kontexts durch Angeben des Namens und Schlüssels eines Speicherkontos
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Mit diesem Befehl wird ein Kontext für das Konto "ContosoGeneral" erstellt, das den angegebenen Schlüssel verwendet.

### Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Mit diesem Befehl wird ein Kontext erstellt, der auf der angegebenen Verbindungszeichenfolge für das Konto "ContosoGeneral" basiert.

### Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Mit diesem Befehl wird ein Kontext für die anonyme Verwendung für das Konto "ContosoGeneral" erstellt.
Der Befehl gibt HTTP als Verbindungsprotokoll an.

### Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen Entwicklungsspeicherkontos
```
PS C:\>New-AzStorageContext -Local
```

Mit diesem Befehl wird ein Kontext mithilfe des lokalen Entwicklungsspeicherkontos erstellt.
Der Befehl gibt den Parameter *"Local"* an.

### Beispiel 5: Container für das lokale Entwicklerspeicherkonto erhalten
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

Der erste Befehl erstellt mithilfe des lokalen Entwicklungsspeicherkontos einen Kontext und speichert diesen Kontext dann in der $Context 01-Variable.
Der zweite Befehl erstellt einen Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet, und speichert diesen Kontext dann in der $Context 02-Variable.
Der letzte Befehl ruft die Container für die in $Context 01 und $Context 02 gespeicherten Kontexte mit **"Get-AzStorageContainer" ab.**

### Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Mit diesem Befehl wird ein Azure Storage-Kontext erstellt, der den angegebenen Speicherendpunkt hat.
Der Befehl erstellt den Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet.

### Beispiel 8: Erstellen eines Kontexts mit einer bestimmten Umgebung
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Mit diesem Befehl wird ein Azure-Speicherkontext erstellt, der über die angegebene Azure-Umgebung verfügt.
Der Befehl erstellt den Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet.

### Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Der erste Befehl generiert ein SAS-Token mithilfe des **Cmdlets "New-AzStorageContainerSASToken"** für den Container "ContosoMain" und speichert dieses Token dann in der $SasToken-Variable.
Dieses Token ist für Berechtigungen zum Lesen, Hinzufügen, Aktualisieren und Löschen verfügbar.
Der zweite Befehl erstellt einen Kontext für das Konto "ContosoGeneral", das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variable.
Der letzte Befehl listet alle blobs auf, die dem Container "ContosoMain" zugeordnet sind, indem der in der Datei gespeicherte Kontext $Context.

### Beispiel 10: Erstellen eines Kontexts mithilfe der OAuth-Authentifizierung
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Mit diesem Befehl wird mithilfe der OAuth (Azure AD)-Authentifizierung ein Kontext erstellt.

## PARAMETERS

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

### -Endpoint
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

### -Environment
Gibt die Azure-Umgebung an.
Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-AzEnvironment` eingeben" aus.

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
Gibt an, dass mit diesem Cmdlet ein Kontext mithilfe des lokalen Entwicklungsspeicherkontos erstellt wird.

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
Gibt ein Sasstoken (Shared Access Signature) für den Kontext an.

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
Gibt den Namen eines Azure Storage-Kontos an.
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
Gibt an, dass dieses Cmdlet einen Azure -Speicherkontext mit OAuth (Azure AD)-Authentifizierung erstellt.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


