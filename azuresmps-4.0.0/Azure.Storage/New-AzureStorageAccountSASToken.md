---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475642"
---
# New-AzureStorageAccountSASToken

## Synopsis
Erstellt ein SAS-Token.

## Syntax

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageSASToken** erstellt ein SAS-Token (Shared Access Signature) auf Kontoebene für ein Azure Storage-Konto.

Sie können das SAS-Token verwenden, um Berechtigungen für mehrere Dienste zu delegieren oder um Berechtigungen für Dienste zu delegieren, die nicht mit einem SAS-Token auf Objektebene verfügbar sind.

## Beispiele

### Beispiel 1: Erstellen eines SAS-Tokens
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Mit diesem Befehl wird ein SAS-Token auf Kontoebene mit der vollständigen Berechtigung erstellt.

### Beispiel 2: Erstellen eines SAS-Tokens für einen Bereich von IP-Adressen
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Mit diesem Befehl wird ein SAS-Token für nur-HTTPS-Anforderungen aus dem angegebenen IP-Adressbereich erstellt.

## Parameter

### -Context
Gibt den Azure-Speicherkontext an.
Sie können das New-AzureStorageContext-Cmdlet verwenden, um ein **AzureStorageContext** -Objekt abzurufen.

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

### -Berechtigung
Gibt die Berechtigungen für das Speicherkonto an.
Berechtigungen sind nur gültig, wenn Sie dem angegebenen Ressourcentyp entsprechen.
Weitere Informationen zu akzeptablen Berechtigungs Werten finden Sie unter Erstellen einer Konto-SAS.https://go.microsoft.com/fwlink/?LinkId=799514

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

### -Protokoll
Gibt das Protokoll an, das für eine Anforderung mit dem Konto SAS zulässig ist.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- HttpsOnly
- HttpsOrHttp

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

### -
Gibt die Ressourcentypen an, die mit dem SAS-Token verfügbar sind.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Keine
- Dienst
- Container
- Objekt

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
Gibt den Dienst an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Keine
- BLOB
- Datei
- Warteschlange
- Tabelle

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Startzeit
Gibt die Uhrzeit als **DateTime** -Objekt an, bei dem die SAS gültig wird.
Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.

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

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[Neu – AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[Neu – AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[Neu – AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[Neu – AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[Neu – AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


