---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005755"
---
# Get-AzureStorageAccount

## Synopsis
Ruft die Speicherkonten für das aktuelle Azure-Abonnement ab.

## Syntax

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageAccount** " gibt ein Objekt zurück, das Informationen zu den Speicherkonten für das aktuelle Abonnement enthält.
Wenn der Parameter *StorageAccountName* angegeben wird, werden nur Informationen über das angegebene Speicherkonto zurückgegeben.

## Beispiele

### Beispiel 1: Zurückgeben aller Speicherkonten
```
PS C:\> Get-AzureStorageAccount
```

Dieser Befehl gibt ein Objekt mit allen Speicherkonten zurück, die dem aktuellen Abonnement zugeordnet sind.

### Beispiel 2: Zurückgeben von Kontoinformationen für ein angegebenes Konto
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

Dieser Befehl gibt ein Objekt zurück, das nur die ContosoStore01-Kontoinformationen hat.

### Beispiel 3: Anzeigen einer Tabelle mit Speicherkonten
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

Dieser Befehl gibt ein Objekt mit allen Speicherkonten zurück, die dem aktuellen Abonnement zugeordnet sind, und gibt diese als Tabelle mit dem Kontonamen, der Kontobezeichnung und dem Speicherort aus.

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
Gibt den Namen eines speicherkontos an.
Falls angegeben, gibt dieses Cmdlet nur das angegebene Speicherkonto Objekt zurück.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### ManagementOperationContext

## Notizen
* Geben Sie `help node-dev` an, um Hilfe zu Node.js entwicklungsbezogenen Cmdlets zu erhalten. Geben Sie `help php-dev` an, um Hilfe zu den PHP-entwicklungsbezogenen Cmdlets zu erhalten.

## Verwandte Links

[Neu – AzureStorageAccount](./New-AzureStorageAccount.md)

[Satz-AzureStorageAccount](./Set-AzureStorageAccount.md)


