---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006595"
---
# Add-AzureNodeWorkerRole

## Synopsis
Erstellt die erforderlichen Dateien und Ordner für eine Node.js-Anwendung, die in der Cloud gehostet werden soll, über node.exe

## Syntax

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet **Add-AzureNodeWorkerRole** erstellt die erforderlichen Dateien und Ordner, manchmal auch als Gerüst bezeichnet, damit eine Node.js Anwendung in der Cloud über node.exe gehostet werden kann.

## Beispiele

### Beispiel 1: worker-Rolle einer einzelnen Instanz
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

In diesem Beispiel wird der aktuellen Anwendung Gerüstbau für eine einzelne Worker-Rolle mit dem Namen **MyWorkerRole** hinzugefügt.

### Beispiel 2: worker-Rolle für mehrere Instanzen
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

In diesem Beispiel wird der aktuellen Anwendung ein Gerüst für eine einzelne Worker-Rolle mit dem Namen **MyWorkerRole** hinzugefügt, wobei die Anzahl der Rolleninstanzen 2 beträgt.

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
Der Wert bestimmt den Ordnernamen, der das Gerüst für den node.js Dienst enthält, der in der Worker-Rolle gehostet wird.
Der Standardwert ist WorkerRole1.

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

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[Neu – AzureServiceProject](./New-AzureServiceProject.md)


