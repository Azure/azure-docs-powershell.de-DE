---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006198"
---
# New-AzureRoleTemplate

## Synopsis
Erstellt Web-und worker-Rollenvorlagen.

## Syntax

### WebRole
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet **New-AzureRoleTemplate** erstellt Web-und worker-Rollenvorlagen.

## Beispiele

### Beispiel 1: Erstellen einer Webrollen Vorlage
```
PS C:\> New-AzureRoleTemplate -Web
```

In diesem Beispiel wird eine neue Webrollen Vorlage in einem Ordner namens "WebRoleTemplate" im aktuellen Verzeichnis erstellt.

### Beispiel 2: Erstellen einer Worker-Rollenvorlage
```
PS C:\> New-AzureRoleTemplate -Worker
```

In diesem Beispiel wird eine neue Worker-Rollenvorlage in einem Ordner namens WebRoleTemplate im aktuellen Verzeichnis erstellt.

### Beispiel 3: Erstellen einer Rollenvorlage in einem benutzerdefinierten Verzeichnis
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

In diesem Beispiel wird eine neue Webrollen Vorlage im Verzeichnis mit dem Namen MyWebRoleTemplate und nicht im aktuellen Verzeichnis erstellt.

## Parameter

### -Output
Gibt den Ausgabepfad der generierten Vorlage an.

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

### -Web
Gibt an, dass Sie eine Webrollen Vorlage erstellen möchten.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Worker
Gibt an, dass Sie eine Worker-Rollenvorlage erstellen möchten.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
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

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)


