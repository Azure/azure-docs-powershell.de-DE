---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110477"
---
# New-AzureWebsite

## SYNOPSIS
Erstellen Sie eine neue Website, die in Azure ausgeführt werden soll.

## SYNTAX

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## BESCHREIBUNG
In diesem Thema wird das Cmdlet in der Version 0.8.10 des Microsoft Azure -PowerShell-Moduls beschrieben.
Um die Version des verwendeten Moduls zu erhalten, geben Sie in der Azure PowerShell-Konsole " `(Get-Module -Name Azure).Version` ein.

Das Cmdlet erstellt eine neue Website, die in Azure ausgeführt werden kann, und bereitet sich auf die Bereitstellung über GitHub vor.

## BEISPIELE

### Beispiel 1: Erstellen einer neuen Website mit Git
```
PS C:\> New-AzureWebsite mySite -Git
```

In diesem Beispiel werden eine neue Website in Azure und ein lokales Git-Repository erstellt, das zum Bereitstellen von Dateien auf der neuen Website verwendet wird.

### Beispiel 2: Erstellen einer in GitHub integrierten Website
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

In diesem Beispiel wird eine neue Website erstellt, die mit einem GitHub-Repository namens "myaccount/myrepo" verknüpft ist.
Commits für das GitHub-Repository werden an die Website in Azure übertragen.

## PARAMETERS

### -Git
Richtet ein lokales Git-Repository ein und verknüpft es mit der Website.
Falls angegeben, richtet dieser Parameter ein Git-Repository im lokalen Verzeichnis ein und fügt ein Remoterepository mit dem Namen "azure" hinzu, das mit der Website in Azure verknüpft ist.

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
Commits für das Repository "Giuthub" werden auf die Website in Azure übertragen.

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

### -GitHubCredentials
Gibt den Benutzernamen und das Kennwort als Anmeldeinformationen an, um eine Verbindung mit GitHub herzustellen.

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

### -GitHubRepository
Gibt den vollständigen Namen des GitHub-Repositorys an, das mit dieser Website zu verknüpfen ist.
Beispiel: `myaccount/myrepo` "

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

### -Location
Gibt den Speicherort des Rechenzentrums an, in dem Sie die Website bereitstellen möchten.

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

### -Profile
Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.
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
Gibt den Benutzernamen an, den Sie im Azure-Portal für die Bereitstellung von Git angegeben haben.

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
Gibt einen Slotnamen für die Website an.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

## AUSGABEN

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Set-AzureWebsite](./Set-AzureWebsite.md)


