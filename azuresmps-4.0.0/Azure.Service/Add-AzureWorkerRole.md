---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005916"
---
# Add-AzureWorkerRole

## Synopsis
Erstellt erforderliche Dateien und Konfiguration für eine benutzerdefinierte Worker-Rolle.

## Syntax

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet **Add-AzureWorkerRole** erstellt erforderliche Dateien und Konfigurationen, manchmal auch als Gerüst bezeichnet, für eine benutzerdefinierte Worker-Rolle.

## Beispiele

### Beispiel 1: Erstellen einer einzelnen Instanzen-Worker-Rolle
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

In diesem Beispiel wird der aktuellen Anwendung Gerüstbau für eine einzelne Worker-Rolle mit dem Namen MyWorkerRole hinzugefügt.

### Beispiel 2: Erstellen einer Worker-Rolle für mehrere Instanzen
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

In diesem Beispiel wird der aktuellen Anwendung ein Gerüst für eine neue Worker-Rolle mit dem Namen MyWorkerRole hinzugefügt, wobei die Anzahl der Rolleninstanzen 2 beträgt.

### Beispiel 3: Erstellen einer Worker-Rolle mit benutzerdefiniertem Gerüst
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

In diesem Beispiel wird eine Worker-Rolle mit benutzerdefiniertem Gerüst erstellt.

## Parameter

### -Instanzen
Gibt die Anzahl der Rolleninstanzen für diese Worker-Rolle an.
Der Standardwert ist 1.

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
Gibt den Namen der Worker-Rolle an.
Dieser Wert bestimmt den Ordnernamen, der das Gerüst für die benutzerdefinierte Anwendung enthält, die in der Worker-Rolle gehostet wird.
Der Standardwert ist "WorkerRolenumber", wobei "Zahl" die Anzahl der Worker-Rollen im Dienst ist.

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
Gibt den Gerüst Vorlagenordner an, der zum Erstellen der Worker-Rolle verwendet werden soll.

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

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Neu – AzureRoleTemplate](./New-AzureRoleTemplate.md)


