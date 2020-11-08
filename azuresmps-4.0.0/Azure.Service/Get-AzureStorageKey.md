---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005754"
---
# Get-AzureStorageKey

## Synopsis
Gibt den primären und sekundären speicherkontoschlüssel für ein Azure Storage-Konto zurück.

## Syntax

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageKey** " gibt ein Objekt mit dem Namen des Azure-speicherkontos, dem primär Kontoschlüssel und dem sekundären Kontoschlüssel des angegebenen Azure-speicherkontos als Eigenschaften zurück.

## Beispiele

### Beispiel 1: Abrufen eines Objekts, das primäre und sekundäre Speicherschlüssel enthält
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

Dieser Befehl ruft ein Objekt mit den primären und sekundären Speicher Schlüsseln für das ContosoStore01-Speicherkonto ab.

### Beispiel 2: Abrufen des primären Speicherkonto Schlüssels und speichern in einer Variablen
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

Mit diesem Befehl wird der primäre speicherkontoschlüssel für das ContosoStore01-Speicherkonto in der $ContosoStoreKey Variablen eingefügt.

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Gibt den Namen des speicherkontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen
* Verwenden Sie den Befehl, um Hilfe zu Node.js zu erhalten `help node-dev` . Wenn Sie Hilfe zu PHP-Erweiterungen benötigen, verwenden Sie den `help php-dev` Befehl.

## Verwandte Links

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Neu – AzureStorageAccount](./New-AzureStorageAccount.md)

[Neu – AzureStorageKey](./New-AzureStorageKey.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)

[Satz-AzureStorageAccount](./Set-AzureStorageAccount.md)


