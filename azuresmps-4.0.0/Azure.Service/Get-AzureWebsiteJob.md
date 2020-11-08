---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006479"
---
# Get-AzureWebsiteJob

## Synopsis
Ruft die Web-Aufträge ab, die einer Website zugeordnet sind.

## Syntax

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Ruft die Web-Aufträge ab, die einer Website zugeordnet sind.

## Beispiele

### Beispiel 1: Abrufen bestimmter Informationen zum Web-Job
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

Ruft einen Webauftrag mit dem Namen "MyWebJob" aus dem Produktions Steckplatz der Website ab.

### Beispiel 2: Abrufen aller Web-Aufträge für eine Website
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

Ruft alle Web-Jobs ab, die dem Produktions Steckplatz von mywebsite zugeordnet sind.

### Beispiel 3: Abrufen aller ausgelösten Web-Aufträge
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

Ruft alle ausgelösten Webaufträge aus dem Staging-Slot der mywebsite ab.

## Parameter

### -Jobname
Der Name des Webdiensts

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobType
Der Web-Auftragstyp.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Ausgelöst
- Fortlaufender

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name der Azure-Website.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Slot
Der Steckplatzname der Azure-Website.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Neu – AzureWebsiteJob](./New-AzureWebsiteJob.md)

[Remove-AzureWebsiteJob](./Remove-AzureWebsiteJob.md)

[Anfang-AzureWebsiteJob](./Start-AzureWebsiteJob.md)

[Stopp-AzureWebsiteJob](./Stop-AzureWebsiteJob.md)


