---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 83480321e58d4dbd21d0a13dd6139c2f2d905c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826683"
---
# New-AzStorageAccountSASToken

## Synopsis
Erstellt ein SAS-Token auf Kontoebene.

## Syntax

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzStorageSASToken** erstellt ein SAS-Token (Shared Access Signature) auf Kontoebene für ein Azure Storage-Konto.
Sie können das SAS-Token verwenden, um Berechtigungen für mehrere Dienste zu delegieren oder um Berechtigungen für Dienste zu delegieren, die nicht mit einem SAS-Token auf Objektebene verfügbar sind.

## Beispiele

### Beispiel 1: Erstellen eines SAS-Tokens auf Kontoebene mit der vollständigen Berechtigung
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Mit diesem Befehl wird ein SAS-Token auf Kontoebene mit der vollständigen Berechtigung erstellt.

### Beispiel 2: Erstellen eines SAS-Tokens auf Kontoebene für einen Bereich von IP-Adressen
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Mit diesem Befehl wird ein SAS-Token auf Kontoebene für reine HTTPS-Anforderungen aus dem angegebenen Bereich von IP-Adressen erstellt.

## Parameter

### -Context
Gibt den Azure-Speicherkontext an.
Sie können das New-AzStorageContext-Cmdlet verwenden, um ein **AzureStorageContext** -Objekt abzurufen.

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
Gibt die Berechtigungen für das Speicherkonto an.
Berechtigungen sind nur gültig, wenn Sie dem angegebenen Ressourcentyp entsprechen.
Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.
Weitere Informationen zu akzeptablen Berechtigungs Werten finden Sie unter Erstellen einer Konto-SAS. https://go.microsoft.com/fwlink/?LinkId=799514

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

### -Protokoll
Gibt das Protokoll an, das für eine Anforderung mit dem Konto SAS zulässig ist.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- HttpsOnly
- HttpsOrHttp der Standardwert ist HttpsOrHttp.

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

### -
Gibt die Ressourcentypen an, die mit dem SAS-Token verfügbar sind.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Keine
- Dienst
- Container
- Objekt

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
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
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
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

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Neu – AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)

[Neu – AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)

[Neu – AzStorageFileSASToken](./New-AzStorageFileSASToken.md)

[Neu – AzStorageQueueSASToken](./New-AzStorageQueueSASToken.md)

[Neu – AzStorageShareSASToken](./New-AzStorageShareSASToken.md)

[Neu – AzStorageTableSASToken](./New-AzStorageTableSASToken.md)


