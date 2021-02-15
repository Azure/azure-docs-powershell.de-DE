---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147969"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Ruft die Details eines Ereignisabonnements ab oder eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement.

## SYNTAX

### EventSubscriptionTopicNameParameterSet (Standard)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das Get-AzEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Event Grid-Abonnements oder eine Liste aller Event Grid-Abonnements im aktuellen Abonnement oder der Ressourcengruppe ab.
Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Event Grid-Abonnements zurückgegeben.
Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben. Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Parameter "Top" gesteuert. Wenn der Spitzenwert nicht angegeben oder nicht $null, enthält die Liste alle Ereignisabonnementelemente. Andernfalls gibt "Top" die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.
Wenn noch weitere Ereignisabonnements verfügbar sind, sollte der Wert in "NextLink" beim nächsten Aufruf verwendet werden, um die nächste Seite mit Ereignisabonnements zu erhalten.
Schließlich wird der Parameter "ODataQuery" zum Filtern der Suchergebnisse verwendet. Die Filterabfrage folgt der #A0 nur mit der Eigenschaft "Name". Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Ruft die Details des Ereignisabonnements "EventSubscription1" ab, das für \` \` \` Thema1 in \` der Ressourcengruppe \` "MyResourceGroupName" erstellt \` wurde.

### Beispiel 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Ruft die Details des Ereignisabonnements "EventSubscription1" ab, das für Thema1 in der Ressourcengruppe \` \` \` \` "MyResourceGroupName" erstellt wurde, einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein \` \` webhookbasiertes Ereignisabonnement handelt.

### Beispiel 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Hier erhalten Sie eine Liste aller Ereignisabonnements, die für "Topic1" in der Ressourcengruppe \` \` \` "MyResourceGroupName" ohne \` Paginierung erstellt wurden.

### Beispiel 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 10 Ereignisabonnements (sofern vorhanden) auf, die für Thema1 in der Ressourcengruppe \` \` \` "MyResourceGroupName" erstellt wurden, die die $odataFilter \` erfüllen. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Abonnement erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

### Beispiel 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Ruft die Details des Ereignisabonnements \` "EventSubscription1" ab, \` das für die Ressourcengruppe \` "MyResourceGroupName" erstellt \` wurde.

### Beispiel 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Ruft die Details des Ereignisabonnements \` "EventSubscription1" ab, das \` für das aktuell ausgewählte Azure-Abonnement erstellt wurde.

### Beispiel 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe \` "MyResourceGroupName" ohne \` Paginierung erstellt wurden.

### Beispiel 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 5 Ereignisabonnements (sofern vorhanden) auf, die unter der Ressourcengruppe \` "MyResourceGroupName" erstellt wurden und den Anforderungen der \` $odataFilter entsprechen. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Abonnement erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

### Beispiel 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Abonnement ohne Paginierung erstellt wurden.

### Beispiel 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 15 globalen Ereignisabonnements (sofern vorhanden) auf, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden, das die Anforderungen $odataFilter erfüllt. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Abonnement erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

### Beispiel 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Ruft die Liste aller regionalen Ereignisabonnements ab, die unter der Ressourcengruppe "MyResourceGroupName" am angegebenen Speicherort \` "westus2" erstellt wurden, ohne \` \` \` Paginierung.

### Beispiel 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 15 regionalen Ereignisabonnements (sofern vorhanden) auf, die unter der Ressourcengruppe "MyResourceGroupName" erstellt wurden, am angegebenen Speicherort \` \` \` "westus2", der die $odataFilter \` erfüllt. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Abonnement erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

### Beispiel 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen EventHub-Namespace ohne Paginierung erstellt wurden.

### Beispiel 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listet die ersten 25 Ereignisabonnements (sofern vorhanden) auf, die für den angegebenen EventHub-Namespace erstellt wurden, der den Anforderungen $odataFilter entspricht. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Abonnement erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

### Beispiel 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Thementyp (EventHub-Namespaces) am angegebenen Speicherort ohne Paginierung erstellt wurden.

### Beispiel 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listet die ersten 15 Ereignisabonnements (sofern vorhanden) auf, die für den angegebenen Thementyp (EventHub-Namespaces) erstellt wurden, am angegebenen Speicherort, der die $odataFilter erfüllt. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Abonnement erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

### Beispiel 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Ruft die Liste aller Ereignisabonnements ab, die für die spezifische Ressourcengruppe ohne Paginierung erstellt wurden.

### Beispiel 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 100 Ereignisabonnements (sofern vorhanden) für die bestimmte Ressourcengruppe auf, die die $odataFilter erfüllt. Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null. Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Abonnement erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf. Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.

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

### -DomainInputObject
EventGrid Domain-Objekt.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
Name der EventGrid-Domäne.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
EventGrid Domain Topic-Objekt.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
Name des Themas "EventGrid".

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Der Name des Ereignisabonnements

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Geben Sie die vollständige Endpunkt-URL des Ziels des Ereignisabonnements an.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid Topic-Objekt.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Position

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Der Link zur nächsten Seite der zu erhaltende Ressourcen. Dieser Wert wird mit dem ersten Aufruf des Get-AzEventGrid-Cmdlet-Aufrufs ermittelt, wenn noch weitere Ressourcen zur Abfrage verfügbar sind.

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
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Bezeichner der Ressource, für die Ereignisabonnements erstellt wurden.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird. Filtern ist derzeit nur für die Eigenschaft "Name" zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
Name des EventGrid-Themas.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType name

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
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

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## AUSGABEN

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
