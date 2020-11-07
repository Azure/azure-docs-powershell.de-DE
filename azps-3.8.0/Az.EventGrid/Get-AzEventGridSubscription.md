---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 5adc6e203166903b0c76d906ce03cd72cb73c3d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846087"
---
# Get-AzEventGridSubscription

## Synopsis
Ruft die Details eines Ereignisabonnements ab oder ruft eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement ab.

## Syntax

### EventSubscriptionTopicNameParameterSet (Standard)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
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

## Beschreibung
Das Get-AzEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Abonnements oder eine Liste aller Ereignis Raster Abonnements im aktuellen Azure-Abonnement oder in der Ressourcengruppe ab.
Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Ereignis Raster-Abonnements zurückgegeben.
Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben. Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Top-Parameter gesteuert. Wenn der obere Wert nicht angegeben oder $NULL ist, enthält die Liste alle Ereignisabonnement Elemente. Andernfalls zeigt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.
Wenn noch weitere Ereignisabonnements verfügbar sind, sollte der Wert in Nextlink beim nächsten Aufruf verwendet werden, um die nächste Seite der Ereignisabonnements abzurufen.
Schließlich wird ODataQuery-Parameter verwendet, um die Filterung für die Suchergebnisse durchzuführen. Die Filterabfrage folgt der OData-Syntax, wobei nur die Name-Eigenschaft verwendet wird. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das Thema \` THEMA1 hat in der \` Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .

### Beispiel 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für \` das Thema THEMA1 hat in der \` Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` , einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein webhook-basiertes Ereignisabonnement handelt.

### Beispiel 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Abrufen einer Liste aller Ereignisabonnements, die für Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` ohne Paginierung erstellt wurden.

### Beispiel 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 10 Ereignisabonnements (sofern vorhanden) auf, die für \` die Themen THEMA1 hat \` in der Ressourcengruppen-MyResourceGroupName erstellt wurden \` \` , die der $odataFilter Abfrage entspricht. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

### Beispiel 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für die Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` .

### Beispiel 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das aktuell ausgewählte Azure-Abonnement erstellt wurden.

### Beispiel 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe \` MyResourceGroupName \` ohne Paginierung erstellt wurden.

### Beispiel 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten fünf Ereignisabonnements (sofern vorhanden) auf, die unter Ressourcengruppen-MyResourceGroupName erstellt wurden \` \` , die der $odataFilter Abfrage entsprechen. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

### Beispiel 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Azure-Abonnement ohne Paginierung erstellt wurden.

### Beispiel 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 15 globalen Ereignisabonnements (sofern vorhanden) auf, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden, das die $odataFilter Abfrage erfüllt. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

### Beispiel 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Ruft die Liste aller regionalen Ereignisabonnements ab, die unter Ressourcen \` Gruppen \` -MyResourceGroupName an der angegebenen Position \` westus2 \` ohne Paginierung erstellt wurden.

### Beispiel 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 15 regionalen Ereignisabonnements (sofern vorhanden) auf, die unter Ressourcengruppen- \` MyResourceGroupName \` in der angegebenen Speicherort-westus2 erstellt wurden \` , die \` die $odataFilter Abfrage erfüllt. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

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

Listen Sie die ersten 25 Ereignisabonnements (falls vorhanden) auf, die für den angegebenen EventHub-Namespace erstellt wurden, der die $odataFilter Abfrage erfüllt. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

### Beispiel 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Topic-Typ (EventHub-Namespaces) an der angegebenen Position ohne Paginierung erstellt wurden.

### Beispiel 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 15 Ereignisabonnements (sofern vorhanden) für den angegebenen Thementyp (EventHub-Namespaces) an der angegebenen Position auf, die die $odataFilter Abfrage erfüllt. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

### Beispiel 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Ruft die Liste aller Ereignisabonnements ab, die für die jeweilige Ressourcengruppe ohne Paginierung erstellt wurden.

### Beispiel 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Listen Sie die ersten 100-Ereignisabonnements (sofern vorhanden) auf, die für die bestimmte Ressourcengruppe erstellt wurden, die der $odataFilter Abfrage entspricht. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
EventGrid-Domänenobjekt.

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

### -Domänenname
EventGrid-Domänenname.

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
Topic-Objekt der EventGrid-Domäne

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
EventGrid Domain Topic Name.

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
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Schließen Sie die vollständige Endpunkt-URL des Ereignisabonnement Ziels ein.

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

### -Inputobject
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

### -Standort
Lage

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nextlink
Der Link für die nächste Seite der Ressourcen, die abgerufen werden sollen. Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf abgerufen, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.

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
Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird. Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.

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
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Der Bezeichner der Ressource, für die Ereignisabonnements erstellt wurden.

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
Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird. Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.

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

### -Topicname
EventGrid-Themen Name

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType-Name

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. EventGrid. Models. PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## Ausgaben

### Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription

## Notizen

## Verwandte Links
