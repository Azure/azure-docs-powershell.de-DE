---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006390"
---
# New-AzureWebsite

## Synopsis
Erstellen Sie eine neue Website, die in Azure ausgeführt werden soll.

## Syntax

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet erstellt eine neue Website, die in Azure ausgeführt werden soll, und bereitet sich auf die Bereitstellung über GitHub vor.

## Beispiele

### Beispiel 1: Erstellen einer neuen Website mit git
```
PS C:\> New-AzureWebsite mySite -Git
```

In diesem Beispiel wird eine neue Website in Azure und ein lokales git-Repository erstellt, das zum Bereitstellen von Dateien auf der neuen Website verwendet wird.

### Beispiel 2: Erstellen einer in GitHub integrierten Website
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

In diesem Beispiel wird eine neue Website erstellt, die mit einem GitHub-Repository namens "MyAccount/myrepo" verknüpft ist.
Commits für das GitHub-Repository werden in Azure auf die Website verschoben.

## Parameter

### -Git
Richtet ein lokales git-Repository ein und verknüpft es mit der Website.
Falls angegeben, richtet dieser Parameter ein git-Repository im lokalen Verzeichnis ein und fügt ein Remote-Repository mit dem Namen "Azure" hinzu, das mit der Website in Azure verknüpft ist.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
Gibt an, dass dieses Cmdlet die neue Website mit einem vorhandenen GitHub-Repository verknüpft.
Commits für das Giuthub-Repository werden in Azure auf die Website verschoben.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GithubCredentials
Gibt den Benutzernamen und das Kennwort für das Herstellen einer Verbindung mit GitHub an.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GithubRepository
Gibt den vollständigen Namen des GitHub-Repositorys an, das mit dieser Website verknüpft werden soll.
Beispiel: `myaccount/myrepo` .

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

### -Hostname
Gibt einen alternativen Hostnamen für die neue Website an.

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

### -Standort
Gibt den Speicherort des Rechenzentrums an, in dem die Website bereitgestellt werden soll.

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
Gibt einen Namen für die Website an.

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

### -PublishingUsername
Gibt den Benutzernamen an, den Sie im Azure-Portal für die git-Bereitstellung angegeben haben.

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

### -Slot
Gibt einen Steckplatznamen für die Website an.

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

[Satz-AzureWebsite](./Set-AzureWebsite.md)


