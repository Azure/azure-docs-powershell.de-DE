---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827483"
---
# New-OfferObject

## Synopsis
Stellt ein Angebot von Diensten dar, für die ein Abonnement erstellt werden kann.

## Syntax

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## Beschreibung
Stellt ein Angebot von Diensten dar, für die ein Abonnement erstellt werden kann.

## Beispiele

### Beispiel 1
```
PS C:\> {{ Add example code here }}
```

{{Add Example Description here}}

## Parameter

### -AddonPlanDefinition
Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
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
Position: 5
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
Position: 7
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

Required: False
Position: 6
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
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Der URI der Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Ort, an dem sich die Ressource befindet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
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
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bundesland
Barrierefreien Status anbieten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
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
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tags
Liste der Schlüssel-Wert-Paare

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Typ
Der Typ der Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

