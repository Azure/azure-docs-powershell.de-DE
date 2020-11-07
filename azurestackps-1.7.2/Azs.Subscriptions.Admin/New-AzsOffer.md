---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87ad48de1fa4ae05f90f067e8a0a2eac2c4fdd0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827368"
---
# New-AzsOffer

## Synopsis
Erstellt ein neues Angebot.

## Syntax

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Erstellen oder aktualisieren Sie das Angebot.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

Erstellt ein neues Angebot.

## Parameter

### -AddonPlanDefinition
Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BasePlanIds
Bezeichner der Basispläne, die dem Mandanten sofort zur Verfügung gestellt werden, wenn ein Mandant das Angebot abonniert hat.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Beschreibung
Angebotsbeschreibung.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Anzeigename des Angebots.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalReferenceId
Externer Verweisbezeichner.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Der Speicherort der Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSubscriptionsPerAccount
Maximale Abonnements pro Konto.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name eines Angebots.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe, unter der sich die Ressource befindet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bundesland
Barrierefreien Status anbieten.
Der Standardwert ist "Privat".
Dieser Parameter wird in einer zukünftigen Version als veraltet markiert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionCount
Aktuelle Abonnementanzahl.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. offer

## Notizen

## Verwandte Links

