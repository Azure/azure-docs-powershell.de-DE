---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005882"
---
# Get-AzureAccount

## Synopsis
Ruft Azure-Konten ab, die für Azure PowerShell verfügbar sind.

## Syntax

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureAccount** " Ruft die Azure-Konten ab, die für Windows PowerShell verfügbar sind.
Wenn Sie Ihre Konten für Windows PowerShell verfügbar machen möchten, verwenden Sie die Cmdlets **Add-AzureAccount** oder **Import-PublishSettingsFile** .

## Beispiele

### Beispiel 1: Abrufen aller Konten
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

Dieser Befehl ruft alle Konten ab, die dem angegebenen Benutzer zugeordnet sind.

### Beispiel 2: Abrufen eines Kontos nach Name
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

Dieser Befehl ruft das ContosoAdmin-Konto ab.

## Parameter

### -Name
Ruft nur das angegebene Konto ab.
Der Standardwert ist alle Konten, die für Windows PowerShell verfügbar sind.
Geben Sie den Kontonamen ein.
Bei dem Wert für **Name** wird die Groß-/Kleinschreibung beachtet.
Platzhalter sind nicht zulässig.

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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Sie können keine Eingabe an dieses Cmdlet übergeben.

## Ausgaben

### Keine
Dieses Cmdlet gibt keine Ausgabe zurück.

## Notizen

## Verwandte Links

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Importieren-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


