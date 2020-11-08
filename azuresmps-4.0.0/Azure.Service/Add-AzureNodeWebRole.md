---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006598"
---
# Add-AzureNodeWebRole

## Synopsis
Erstellt erforderliche Dateien und Ordner für eine Node.js Anwendung.

## Syntax

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das **Add-AzureNodeWebRole** erstellt erforderliche Dateien und Ordner, manchmal auch als Gerüst bezeichnet, damit eine Node.js Anwendung in der Cloud über IIS gehostet werden kann.

## Beispiele

### Beispiel 1: webrolle einer einzelnen Instanz
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

In diesem Beispiel wird der aktuellen Anwendung Gerüstbau für eine einzelne webrolle mit dem Namen " **MyWebRole** " hinzugefügt.

### Beispiel 2: webrolle für mehrere Instanzen
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

In diesem Beispiel wird der aktuellen Anwendung ein Gerüst für eine neue webrolle mit dem Namen **MyWebRole** hinzugefügt, wobei die Anzahl der Rolleninstanzen 2 beträgt.

## Parameter

### -Instanzen
Gibt die Anzahl der Rolleninstanzen für diese webrolle an.
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
Gibt den Namen der webrolle an.
Außerdem wird der Name des Verzeichnisses bestimmt, das das Gerüst für die node.js-Anwendung enthält, die in der webrolle gehostet wird.
Der Standardwert ist webrole #, wobei # die Anzahl der Webrollen im Dienst angibt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[Neu – AzureServiceProject](./New-AzureServiceProject.md)


