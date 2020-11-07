---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663135"
---
# New-AzureRmFrontDoorMatchConditionObject

## Synopsis
Erstellen eines MatchCondition-Objekts für die WAF-Richtlinienerstellung

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Erstellen eines MatchCondition-Objekts für die WAF-Richtlinienerstellung

## Beispiele

### Beispiel 1
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

Erstellen eines MatchCondition-Objekts

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Matchwert
Übereinstimmungs Wert.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MatchVariable
Variable vergleichen.
Mögliche Werte sind: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' postargs ', ' RequestUri ', ' RequestHeader ', ' RequestBody '

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NegateCondition
Beschreibt, ob es sich um eine Negations Bedingung handelt oder ob der Standardwert falsch ist.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operatorproperty
Beschreibt den Operator, der zugeordnet werden soll.
Mögliche Werte sind: "Any", "IPMatch", "geomatch", "gleich", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "beginntmitder", "endsWith" "

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Auswahl
Der Name des Selektors in RequestHeader oder RequestBody, der zugeordnet werden soll.

```yaml
Type: System.String
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

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Haustür. Models. PSMatchCondition

## Notizen

## Verwandte Links

[Neu – AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorCustomRuleObject.md)
