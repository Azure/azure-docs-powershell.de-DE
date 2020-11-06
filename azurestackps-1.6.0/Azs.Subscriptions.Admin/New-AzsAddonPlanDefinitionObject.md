---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474754"
---
# New-AzsAddonPlanDefinitionObject

## Synopsis
Enthält den Namen des gewünschten Plans, mit dem ein Angebot verknüpft oder dessen Verknüpfung aufgehoben werden soll.

## Syntax

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## Beschreibung
Enthält den Namen des gewünschten Plans, mit dem ein Angebot verknüpft oder dessen Verknüpfung aufgehoben werden soll.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

Erstellen Sie ein neues Plan Definitionsobjekt für den angegebenen Plan mit dem Erfassungs Grenzwert von 500.

## Parameter

### -MaxAcquisitionCount
Die maximale Anzahl von Instanzen, die von einem einzelnen Abonnement abgerufen werden können.
Wenn keine Angabe erfolgt, lautet der angenommene Wert 1.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plan-Nr.
Plan-ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

