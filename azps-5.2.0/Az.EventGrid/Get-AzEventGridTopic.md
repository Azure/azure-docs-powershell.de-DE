---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292552"
---
# Get-AzEventGridTopic

## SYNOPSIS
Ruft die Details eines Themas "Veranstaltungsraster" ab oder ruft eine Liste aller Themen zum Veranstaltungsraster im aktuellen Abonnement von Azure ab.

## SYNTAX

### ResourceGroupNameParameterSet (Standard)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das Get-AzEventGridTopic-Cmdlet ruft entweder die Details eines angegebenen "Veranstaltungsrasterthemas" oder eine Liste aller Themen zum Veranstaltungsraster im aktuellen Abonnement von Azure ab.
Wenn der Themaname angegeben wird, werden die Details eines einzelnen Ereignisrasterthemas zurückgegeben.
Wenn der Name des Themas nicht angegeben wird, wird eine Liste der Themen zurückgegeben. Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Parameter "Top" gesteuert. Wenn der Oberste Wert nicht angegeben oder nicht $null, enthält die Liste alle Themenelemente. Andernfalls gibt "Top" die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.
Wenn noch weitere Themen verfügbar sind, sollte der Wert in "NextLink" im nächsten Aufruf verwendet werden, um die nächste Seite mit Themen zu erhalten.
Schließlich wird der Parameter "ODataQuery" zum Filtern der Suchergebnisse verwendet. Die Filterabfrage folgt der #A0 nur mit der Eigenschaft "Name". Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Ruft die Details des Themas "Veranstaltungsraster" \` in \` der Ressourcengruppe \` "MyResourceGroupName" \` ab.

### Beispiel 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Ruft die Details des Themas "Veranstaltungsraster" \` in \` der Ressourcengruppe \` "MyResourceGroupName" \` ab.

### Beispiel 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Listet alle Themen zum Veranstaltungsraster in der Ressourcengruppe \` "MyResourceGroupName" \` ohne Paginierung auf.

### Beispiel 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Listen Sie die ersten 10 Themen zum Veranstaltungsraster (sofern vorhanden) in der Ressourcengruppe \` "MyResourceGroupName" auf, die den Anforderungen $odataFilter \` entsprechen. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Themen zu erhalten, wird erwartet, dass der Benutzer die Seite(n) erneut aufruft Get-AzEventGridTopic ergebnisse verwendet. NextLink, der aus dem vorherigen Anruf erhalten wurde. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

### Beispiel 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Listen Sie alle Themen des Veranstaltungsrasters im Abonnement ohne Paginierung auf.

### Beispiel 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Listen Sie die ersten 10 Themen zum Veranstaltungsraster (sofern vorhanden) im Abonnement auf, die den Anforderungen $odataFilter entsprechen. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Themen zu erhalten, wird erwartet, dass der Benutzer die Seite(n) erneut aufruft Get-AzEventGridTopic ergebnisse verwendet. NextLink, der aus dem vorherigen Anruf erhalten wurde. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Name
Name des EventGrid-Themas.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Der Link zur nächsten Seite der zu erhaltende Ressourcen. Dieser Wert wird mit dem ersten Aufruf des Get-AzEventGrid-Cmdlet-Aufrufs ermittelt, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.

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
Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird. Filtern ist derzeit nur für die Eigenschaft "Name" zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppenname.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Ressourcenbezeichner, der das Thema "Veranstaltungsraster" darstellt.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Die maximale Anzahl zu erhaltende Ressourcen. Gültiger Wert zwischen 1 und 100. Wenn der oberste Wert angegeben wird und weitere Ergebnisse weiterhin verfügbar sind, enthält das Ergebnis einen Link zur nächsten Seite, die in "NextLink" abgefragt werden soll. Wenn der Oberste Wert nicht angegeben wird, wird die vollständige Liste der Ressourcen auf einmal zurückgegeben.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## AUSGABEN

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
