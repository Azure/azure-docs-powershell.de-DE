---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006480"
---
# Get-AzureWebsite

## Synopsis
Ruft Azure-Websites im aktuellen Abonnement ab.

## Syntax

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureWebsite** " Ruft Informationen zu Azure-Websites im aktuellen Abonnement ab.

Standardmäßig ruft **Get-AzureWebsite** alle Azure-Websites im aktuellen Abonnement ab und gibt ein Objekt zurück, das grundlegende Informationen zu den Websites bereitstellt.
Wenn Sie den Parameter *Name* verwenden, gibt **Get-AzureWebsite** ein Objekt mit umfangreichen Informationen zurück, einschließlich Konfigurationsdetails.

Das aktuelle Abonnement ist das Abonnement, das als "aktuell" festgelegt ist. Um das aktuelle Abonnement zu finden, verwenden Sie den *aktuellen* Parameter des Cmdlets [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .
Wenn Sie das aktuelle Abonnement ändern möchten, verwenden Sie das Cmdlet [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Abrufen aller Websites im Abonnement
```
PS C:\> Get-AzureWebsite
```

Dieser Befehl ruft alle Azure-Websites im aktuellen Abonnement ab.

### Beispiel 2: Abrufen einer Website nach Namen
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Dieser Befehl Ruft detaillierte Informationen zur ContosoWeb Azure-Website einschließlich Konfigurationsinformationen ab.
Wenn Sie den Parameter *Name* verwenden, gibt **Get-AzureWebsite** ein **SiteWithConfig** -Objekt mit erweiterten Informationen zur Website zurück.

### Beispiel 3: Abrufen detaillierter Informationen zu allen Websites
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Dieser Befehl Ruft detaillierte Informationen zu allen Websites des Abonnements ab.
Sie verwendet einen Befehl " **Get-AzureWebsite** ", um alle Websites abzurufen, und verwendet dann das **ForEach-Object-** Cmdlet, um jede Website nach Namen abzurufen.

### Beispiel 4: Abrufen von Informationen zu einem Bereitstellungs Steckplatz
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Dieser Befehl ruft den Staging-Bereitstellungs Steckplatz der ContosoWeb-Website ab.
Mit Bereitstellungs Steckplätzen können Sie verschiedene Versionen ihrer Azure-Website testen, ohne Sie für die Öffentlichkeit freizugeben.

### Beispiel 5: Abrufen von Website Instanzen
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

In den Befehlen in diesem Beispiel wird die Instances-Eigenschaft einer Azure-Website verwendet, um Informationen zu aktuell ausgeführten Website Instanzen abzurufen.
Die **Instances** -Eigenschaft wurde dem **SiteWithConfig** -Objekt in Version 0.8.3 des Azure-Moduls hinzugefügt.

Der erste Befehl ruft die Instanz-IDs aller derzeit ausgeführten Instanzen einer Website ab.
Mit dem zweiten Befehl wird die Anzahl der ausgeführten Instanzen der Website abgerufen.
Sie können die **count** -Eigenschaft für ein beliebiges Array verwenden.

## Parameter

### -Name
Ruft detaillierte Konfigurationsinformationen zur angegebenen Website ab.
Geben Sie den Namen einer Website im Abonnement ein.
Standardmäßig ruft **Get-AzureWebsite** alle Websites im aktuellen Abonnement ab.
Der *Name* -Wert unterstützt keine Platzhalterzeichen.

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
Ruft den angegebenen Bereitstellungs Steckplatz der Website ab.
Geben Sie den Namen des Steckplatzes ein, beispielsweise "Staging" oder "Production".
Weitere Informationen zu Bereitstellungs Steckplätzen finden Sie unter Bereitstellung auf Microsoft Azure-Websites https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Verwenden Sie das Cmdlet Set-AzureWebsite, um einen Bereitstellungs Steckplatz zu einer vorhandenen Azure-Website hinzuzufügen.

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

### Keine
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### Microsoft. WindowsAzure. Commands. Utilities. Websites. Services. webentities. Website
Standardmäßig gibt **Get-AzureWebsite** ein Array von **Website** Objekten zurück.

### Microsoft. WindowsAzure. Commands. Utilities. Websites. Services. webentities. SiteWithConfig
Wenn Sie den Parameter *Name* verwenden, gibt **Get-AzureWebsite** ein **SiteWithConfig** -Objekt zurück.

## Notizen

## Verwandte Links

[Neu – AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Anfang-AzureWebsite](./Start-AzureWebsite.md)

[Stopp-AzureWebsite](./Stop-AzureWebsite.md)

[Anzeigen-AzureWebsite](./Show-AzureWebsite.md)


