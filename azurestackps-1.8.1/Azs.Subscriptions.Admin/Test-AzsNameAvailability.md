---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840831"
---
# Test-AzsNameAvailability

## Synopsis
Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.

## Syntax

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## Beschreibung
Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.

## Parameter

### -Name
Der zu überprüfende Ressourcenname.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -
Der zu überprüfende Ressourcentyp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. CheckNameAvailabilityResponse

## Notizen

## Verwandte Links

