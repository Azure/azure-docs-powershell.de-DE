---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 053c9a503b6cb7d3833d214208ae7fe6bd60fe45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934963"
---
# Get-AzEventGridDomainTopic

## SYNOPSIS
Ruft die Details eines Themas zu einer Event Grid-Domäne ab, oder ruft eine Liste aller Themen für Ereignisrasterdomänen unter einer bestimmten Event Grid-Domäne im aktuellen Azure-Abonnement ab.

## SYNTAX

### DomainTopicNameParameterSet (Standard)
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdDomainTopicParameterSet
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das Get-AzEventGridDomainTopic-Cmdlet ruft entweder die Details eines angegebenen Themas "Ereignisrasterdomäne" oder eine Liste aller Themen der Ereignisrasterdomäne unter einer bestimmten Domäne im aktuellen Azure-Abonnement ab.
Wenn der Domänenthemaname angegeben wird, werden die Details eines einzelnen Themas "Ereignisrasterdomäne" zurückgegeben.
Wenn der Domänenthemaname nicht angegeben wird, wird eine Liste der Domänenthemen unter dem angegebenen Domänennamen zurückgegeben. Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Parameter Top gesteuert. Wenn der Oberste Wert nicht angegeben oder nicht $null, enthält die Liste alle Domänenthemenelemente. Andernfalls gibt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.
Wenn noch weitere Domänenthemen verfügbar sind, sollte der Wert in NextLink im nächsten Aufruf verwendet werden, um die nächste Seite mit Domänenthemen zu erhalten.
Schließlich wird der Parameter ODataQuery zum Filtern der Suchergebnisse verwendet. Die Filterabfrage folgt der #A0 nur mit der Name-Eigenschaft. Zu den unterstützten Vorgängen gehören: CONTAINS, Eq (für gleich), ne (für nicht gleich), UND, ODER und NICHT.

## BEISPIELE

### Beispiel 1

Ruft in der Ressourcengruppe MyResourceGroupName die Details des Themas \` "Ereignisrasterdomäne" DomainTopic1 unter \` Ereignisrasterdomäne \` Domäne1 \` \` \` ab.

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Beispiel 2

Ruft die Details des Themas "Ereignisrasterdomäne" \` DomainTopic1 unter \` Ereignisrasterdomäne Domäne1 in der Ressourcengruppe \` \` \` MyResourceGroupName mit \` der Option ResourceId ab.

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Beispiel 3

Listen Sie alle Themen der Ereignisrasterdomäne unter Ereignisrasterdomäne Domäne1 in der Ressourcengruppe \` \` \` MyResourceGroupName ohne Paginierung auf (alle Ergebnisse werden in einem \` Einzigen Schuss zurückgegeben).

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Beispiel 4

Listen Sie alle Themen der Ereignisrasterdomäne unter Ereignisrasterdomäne Domäne1 in der Ressourcengruppe \` \` \` MyResourceGroupName ohne Paginierung auf (alle Ergebnisse werden auf einen Schlag zurückgegeben) mithilfe der Option \` ResourceId

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Beispiel 5

Listen Sie die Domänenthemen des Ereignisrasters (falls vorhanden) unter Domäne1 in der Ressourcengruppe \` \` MyResourceGroupName auf, die die Themen $odataFilter Abfrage \` 10 Domänen gleichzeitig \` erfüllen. Wenn weitere Ergebnisse verfügbar sind, wird $result. NextLink wird nicht $null. Um die nächsten Seite(n) mit Domänenthemen zu erhalten, wird erwartet, dass der Benutzer erneut Get-AzEventGridDomainTopic aufruft und das Ergebnis verwendet. NextLink, der aus dem vorherigen Aufruf ermittelt wurde. Der Anrufer sollte beim Ergebnis beenden. NextLink wird $null.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName
Name der EventGrid-Domäne.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Name des Themas "EventGrid-Domäne".

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Der Link für die nächste Seite der zu erhaltende Ressourcen. Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf ermittelt, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
Die zum Filtern der Listenergebnisse verwendete OData-Abfrage. Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, Eq (für gleich), ne (für nicht gleich), UND, ODER und NICHT.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Ressourcenbezeichner, der das Thema "Event Grid Domain" oder "Grid Domain Topic" darstellt.

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Die zum Filtern der Listenergebnisse verwendete OData-Abfrage. Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, Eq (für gleich), ne (für nicht gleich), UND, ODER und NICHT.

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Int32

## AUSGABEN

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance

## NOTIZEN

## VERWANDTE LINKS
