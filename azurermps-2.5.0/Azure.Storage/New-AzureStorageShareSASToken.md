---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharesastoken
schema: 2.0.0
ms.openlocfilehash: dbfee49f6e6fcd083350a5ab818ac33309e4b672
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849804"
---
# New-AzureStorageShareSASToken

## Synopsis
Generieren des Shared Access-Signaturtokens für die Azure-Speicherfreigabe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageShareSASToken** generiert ein freigegebenes zugriffssignatur Token für eine Azure-Speicherfreigabe.

## Beispiele

### Beispiel 1: Generieren eines freigegebenen zugriffssignatur Tokens für eine Freigabe
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

Dieser Befehl erstellt ein freigegebenes zugriffssignatur Token für die Freigabe mit dem Namen ContosoShare.

### Beispiel 2: generieren mehrerer freigegebener zugriffssignatur Token mithilfe der Pipeline
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

Dieser Befehl ruft alle Speicherfreigaben ab, die dem Präfix Test entsprechen.
Der Befehl übergibt Sie mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet erstellt ein freigegebenes Zugriffstoken für jede Speicherfreigabe, die über die angegebenen Berechtigungen verfügt.

### Beispiel 3: Generieren eines freigegebenen zugriffssignatur Tokens, das eine freigegebene Zugriffsrichtlinie verwendet
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

Dieser Befehl erstellt ein freigegebenes zugriffssignatur Token für die Speicherfreigabe mit dem Namen ContosoShare, die die Richtlinie mit dem Namen ContosoPolicy03 hat.

## Parameter

### -Context
Gibt einen Azure-Speicherkontext an.
Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.

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

### -ExpiryTime
Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur ungültig wird.

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
Gibt die Berechtigungen im Token an, um auf die Freigabe und die Dateien unter der Freigabe zuzugreifen.
Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.

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

### – Richtlinien
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

### -Freigabename
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### System. String

## Notizen
* Schlüsselwörter: Common, Azure, Dienste, Daten, Speicher, BLOB, Warteschlange, Tabelle

## Verwandte Links

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[Neu – AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
