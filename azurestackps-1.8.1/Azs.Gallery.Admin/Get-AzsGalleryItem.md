---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840876"
---
# Get-AzsGalleryItem

## Synopsis
Listet Katalogelemente auf.

## Syntax

### Liste (Standard)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Erhalten
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## Beschreibung
Abrufen einer Liste der im Azure Stack Marketplace verfügbaren Katalogelemente

## Beispiele

### Beispiel 1
```
Get-AzsGalleryItem
```

Katalogelemente auflisten.

### Beispiel 2
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Besorgen Sie sich ein Katalogelement mit dem Namen.

## Parameter

### -Name
Die Identität des Katalogelements.
Enthält den Namen des Herausgebers, den Elementnamen und kann die durch das Perioden Zeichen getrennte Version enthalten.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem

## Notizen

## Verwandte Links
