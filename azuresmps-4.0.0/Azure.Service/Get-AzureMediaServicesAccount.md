---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006541"
---
# Get-AzureMediaServicesAccount

## Synopsis
Ruft die verfügbaren Azure Media Services-Konten ab.

**Hinweis:** Diese Version ist veraltet, bitte lesen Sie die [neuere Version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## Syntax

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Verwenden Sie das Cmdlet, um alle Konten aufzulisten `Get-AzureMediaServicesAccount` .
Verwenden Sie das Cmdlet, um ausführlichere Informationen zu einem bestimmten Konto zu erhalten `Get-AzureMediaServicesAccount -Name YourAccountName` .

## Beispiele

### Beispiel 1: Auflisten aller Media Services-Konten
```
PS C:\> Get-AzureMediaServicesAccount
```

Dieser Befehl listet alle verfügbaren Media Services-Konten auf.

### Beispiel 2: Abrufen detaillierter Informationen zu einem Media Services-Konto
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

Mit diesem Befehl werden die Eigenschaften eines Media Services-Kontos angezeigt.

## Parameter

### -Name
Der Name des Media Services-Kontos.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Verwenden von Azure PowerShell für Mediendienste](https://go.microsoft.com/fwlink/?LinkId=324179)


