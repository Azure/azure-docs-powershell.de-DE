---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006429"
---
# New-AzureAutomationModule

## Synopsis

Importiert ein Modul in die Automatisierung.

## Syntax

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Mit dem Cmdlet **New-AzureAutomationModule** wird ein Modul in die Azure-Automatisierung importiert.
Bei einem Modul handelt es sich um eine komprimierte Datei mit der Erweiterung ZIP, die einen Ordner enthält, der einen der folgenden Dateitypen enthält:

- Ein Windows PowerShell-Modul (psm1-Datei). 

- Ein Windows PowerShell-Modul Manifest (psd1-Datei). 

- Eine Assembly (DLL-Datei).

Die Namen der ZIP-Datei, der Ordner in der ZIP-Datei und die Datei im Ordner (psm1, PSD. 1 oder dll) müssen übereinstimmen.

## Beispiele

### Beispiel 1: Importieren eines Moduls
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

Dieser Befehl importiert ein Modul mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.
Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, in dem das Modul gespeichert werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLink
Öffentliche URL, beispielsweise eine Website oder ein Azure BLOB-Speicher, der den Pfad zur Moduldatei angibt.
Dieser Speicherort muss öffentlich zugänglich sein.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für das Modul an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -Tags
Gibt einen oder mehrere Tags an, die mit dem Modul verknüpft sind.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

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

### Microsoft. Azure. Commands. Automation. Model. Module

## Notizen

## Verwandte Links

[Get-AzureAutomationModule](./Get-AzureAutomationModule.md)

[Remove-AzureAutomationModule](./Remove-AzureAutomationModule.md)

[Satz-AzureAutomationModule](./Set-AzureAutomationModule.md)


