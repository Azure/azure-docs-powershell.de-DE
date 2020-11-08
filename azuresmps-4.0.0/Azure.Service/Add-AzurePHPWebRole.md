---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006596"
---
# Add-AzurePHPWebRole

## Synopsis
Erstellt die erforderlichen Dateien und die Konfiguration für eine PHP-Anwendung.

## Syntax

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Mit dem Cmdlet **Add-AzurePHPWebRole** werden die Dateien und die Konfiguration, manchmal auch als Gerüst bezeichnet, für eine PHP-Anwendung erstellt, die in Azure über IIS gehostet wird.

## Beispiele

### Beispiel 1: Hinzufügen einer webrolle mit Standardwerten
```
PS C:\> Add-AzurePHPWebRole
```

In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für die neue webrolle unter Verwendung der Standardwerte für einen Dienst mit dem Namen "WebRole1" mit einer 1-Instanz hinzugefügt.

### Beispiel 2: Hinzufügen einer webrolle mit mehreren Instanzen
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für eine neue webrolle zur aktuellen Anwendung hinzugefügt, wobei der Name "MyWebRole" und die Anzahl der Rolleninstanzen von 2 verwendet werden.

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
Der Name bestimmt den Namen des Verzeichnisses, in dem die erforderlichen Dateien und die Konfiguration für die PHP-Anwendung enthalten sind.
Der Standardwert ist webrole #, wobei # die Anzahl der Webrollen im Dienst ist.

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

[Add-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[Neu – AzureServiceProject](./New-AzureServiceProject.md)


