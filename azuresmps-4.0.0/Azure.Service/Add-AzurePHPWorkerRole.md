---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006593"
---
# Add-AzurePHPWorkerRole

## Synopsis
Erstellt die erforderlichen Dateien und die Konfiguration für eine PHP-Anwendung, die in Azure über php.exe gehostet wird.

## Syntax

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Erstellt die erforderlichen Dateien und Konfigurationen, manchmal auch als Gerüst bezeichnet, für eine PHP-Anwendung, die in Azure über php.exe gehostet wird.

## Beispiele

### Beispiel 1: Erstellen einer Worker-Rolle mit einer einzelnen Instanz
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für eine einzelne Worker-Rolle mit dem Namen "MyWorkerRole" zur aktuellen Anwendung hinzugefügt.

### Beispiel 2: Erstellen einer Worker-Rolle mit mehreren Instanzen
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für eine neue Worker-Rolle zur aktuellen Anwendung hinzugefügt, wobei der Name MyWorkerRole mit der Anzahl der Rolleninstanzen von 2 verwendet wird.

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
Der Name bestimmt den Ordnernamen, der die erforderlichen Dateien und die Konfiguration für den in der Worker-Rolle gehosteten php-Dienst enthält.
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

[Neu – AzureServiceProject](./New-AzureServiceProject.md)

[Add-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


