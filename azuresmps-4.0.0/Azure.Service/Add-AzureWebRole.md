---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005917"
---
# Add-AzureWebRole

## Synopsis
Fügt eine Web Worker-Rolle hinzu.

## Syntax

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das **Add-AzureWebRole-** Cmdlet fügt eine Web Worker-Rolle hinzu.

## Beispiele

### Beispiel 1: Hinzufügen einer Standardrolle
```
PS C:\> Add-AzureWebRole
```

Dieser Befehl Add Web Role mit der Standardkonfiguration von Webrole1 als Name und einer einzelnen Instanz.

### Beispiel 2: Hinzufügen einer Rolle mit einem Namen
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

Mit diesem Befehl wird der aktuellen Anwendung eine einzelne webrolle mit dem Namen "MyWebRole" hinzugefügt.

### Beispiel 3: Hinzufügen einer Rolle mit einem Namen und einer instanzenanzahl
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

Mit diesem Befehl wird der aktuellen Anwendung eine webrolle mit dem Namen "MyWebRole" hinzugefügt.
Das Cmdlet weist eine Rolleninstanzen Anzahl von 2 auf.

### Beispiel 4: Hinzufügen einer Rolle mit einem Namen und einer Vorlage
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

Mit diesem Befehl wird der aktuellen Anwendung eine einzelne webrolle mit dem Namen "MyWebRole" hinzugefügt.
Der Befehl gibt einen Ordner mit dem Namen "MyWebTemplateFolder" als Gerüst Vorlage an.

## Parameter

### -Instanzen
Gibt die Anzahl der Instanzen an.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der webrolle an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

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

### -TemplateFolder
Gibt den Vorlagenordner an.

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

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)

[Neu – AzureRoleTemplate](./New-AzureRoleTemplate.md)


