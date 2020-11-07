---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 678453cc050ae31158f4f08e1efcda00338aca98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662876"
---
# New-AzureStorageContext

## Synopsis
Erstellt einen Azure-Speicherkontext.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### AccountNameAndKey (Standard)
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### ConnectionString
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageContext** erstellt einen Azure-Speicherkontext.

## Beispiele

### Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkonto namens und-Schlüssels
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.

### Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Dieser Befehl erstellt einen Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral.

### Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Dieser Befehl erstellt einen Kontext für die anonyme Verwendung für das Konto mit dem Namen ContosoGeneral.
Der Befehl gibt HTTP als Verbindungsprotokoll an.

### Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen entwicklungsspeicher Kontos
```
C:\PS>New-AzureStorageContext -Local
```

Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos.
Der Befehl gibt den *lokalen* Parameter an.

### Beispiel 5: Abrufen des Containers für das lokale Entwickler Speicherkonto
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das Cmdlet " **Get-AzureStorageContainer** ".
Der Befehl ruft den Azure-Speichercontainer für das lokale Entwickler Speicherkonto ab.

### Beispiel 6: Abrufen mehrerer Container
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

Der erste Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und speichert diesen Kontext dann in der $Context 01-Variablen.

Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird, und speichert diesen Kontext dann in der Variablen $Context 02.

Der endgültige Befehl ruft die Container für die in $context 01 und $Context 02 gespeicherten Kontexte ab, indem **Sie Get-AzureStorageContainer** verwenden.

### Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Dieser Befehl erstellt einen Azure-Speicherkontext mit dem angegebenen Speicher Endpunkt.
Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.

### Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.
Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.

### Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

Der erste Befehl generiert ein SAS-Token mithilfe des Cmdlets **New-AzureStorageContainerSASToken** für den Container mit dem Namen ContosoMain und speichert dieses Token dann in der $SasToken-Variablen.
Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.

Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variablen.

Der endgültige Befehl listet alle BLOBs auf, die dem Container mit dem Namen ContosoMain zugeordnet sind, indem Sie den in $context gespeicherten Kontext verwenden.

## Parameter

### -Anonymous
Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext für die anonyme Anmeldung erstellt wird.

```yaml
Type: SwitchParameter
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
Type: String
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
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
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
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-AzureEnvironment` .

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
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
Type: SwitchParameter
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
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
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
Type: String
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
Type: String
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
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### AzureStorageContext

## Notizen

## Verwandte Links

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[Neu – AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


