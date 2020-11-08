---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165478"
---
# New-AzStorageContext

## Synopsis
Erstellt einen Azure-Speicherkontext.

## Syntax

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

## Beschreibung
Das Cmdlet **New-AzStorageContext** erstellt einen Azure-Speicherkontext.
Die Standardauthentifizierung eines Speicher Kontexts ist OAuth (Azure AD), wenn nur der Name des Eingabe speicherkontos.
Details zur Authentifizierung des Speicher Diensts finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .

## Beispiele

### Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkonto namens und-Schlüssels
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.

### Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Dieser Befehl erstellt einen Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral.

### Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Dieser Befehl erstellt einen Kontext für die anonyme Verwendung für das Konto mit dem Namen ContosoGeneral.
Der Befehl gibt HTTP als Verbindungsprotokoll an.

### Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen entwicklungsspeicher Kontos
```
PS C:\>New-AzStorageContext -Local
```

Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos.
Der Befehl gibt den *lokalen* Parameter an.

### Beispiel 5: Abrufen des Containers für das lokale Entwickler Speicherkonto
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das Cmdlet " **Get-AzStorageContainer** ".
Der Befehl ruft den Azure-Speichercontainer für das lokale Entwickler Speicherkonto ab.

### Beispiel 6: Abrufen mehrerer Container
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Der erste Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und speichert diesen Kontext dann in der $Context 01-Variablen.
Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird, und speichert diesen Kontext dann in der Variablen $Context 02.
Der endgültige Befehl ruft die Container für die in $context 01 und $Context 02 gespeicherten Kontexte ab, indem **Sie Get-AzStorageContainer** verwenden.

### Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Dieser Befehl erstellt einen Azure-Speicherkontext mit dem angegebenen Speicher Endpunkt.
Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.

### Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.
Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.

### Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Der erste Befehl generiert ein SAS-Token mithilfe des Cmdlets **New-AzStorageContainerSASToken** für den Container mit dem Namen ContosoMain und speichert dieses Token dann in der $SasToken-Variablen.
Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.
Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variablen.
Der endgültige Befehl listet alle BLOBs auf, die dem Container mit dem Namen ContosoMain zugeordnet sind, indem Sie den in $context gespeicherten Kontext verwenden.

### Beispiel 10: Erstellen eines Kontexts mithilfe der OAuth-Authentifizierung
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Dieser Befehl erstellt einen Kontext mithilfe der OAuth (Azure AD)-Authentifizierung.

## Parameter

### -Anonymous
Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext für die anonyme Anmeldung erstellt wird.

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
Gibt eine Verbindungszeichenfolge für den Azure-Speicherkontext an.

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
Gibt den Endpunkt für den Azure-Speicherkontext an.

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
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-AzEnvironment` .

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

### -Lokal
Gibt an, dass dieses Cmdlet einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos erstellt.

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

### -Protokoll
Übertragungsprotokoll (HTTPS/HTTP).

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
Gibt einen Azure-speicherkontoschlüssel an.
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
Gibt den Namen eines Azure-speicherkontos an.
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
Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext mit OAuth (Azure AD)-Authentifizierung erstellt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext

## Notizen

## Verwandte Links

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[Neu – AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


