---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: 0c5c0f0f9739a2f9481989a69ece9aa29f0c67e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499861"
---
# New-AzureRmEventGridSubscription

## Synopsis
Erstellt ein neues Azure-Ereignis Raster-Ereignisabonnement für ein Thema, eine Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ResourceGroupNameParameterSet (Standard)
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EventSubscriptionInputObjectSet
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CustomTopicEventSubscriptionParameterSet
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Erstellen Sie ein neues Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine unterstützte Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.
Wenn Sie ein Ereignisabonnement für das aktuell ausgewählte Azure-Abonnement erstellen möchten, geben Sie den Namen des Ereignisabonnements und den Zielendpunkt an.
Wenn Sie ein Ereignisabonnement für eine Ressourcengruppe erstellen möchten, geben Sie neben dem Namen des Ereignisabonnements und dem Zielendpunkt den Namen der Ressourcengruppe an.
Wenn Sie ein Ereignisabonnement für ein Azure-Ereignis Raster Thema erstellen möchten, geben Sie den Themen Namen ebenfalls an.
Wenn Sie ein Ereignisabonnement für eine unterstützte Azure-Ressource erstellen möchten, geben Sie die vollständige Ressourcen-ID der Ressource an. Führen Sie das Get-AzureRmEventGridTopicType-Cmdlet aus, um die Liste der unterstützten Typen anzuzeigen.

## Beispiele

### Beispiel 1
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` zu einem Azure-Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` mit dem Zielendpunkt des webhooks https://requestb.in/19qlscd1 . Dieses Ereignisabonnement verwendet Standardfilter.

### Beispiel 2
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einer Ressourcengruppe \` MyResourceGroupName \` mit dem Zielweb-Zielendpunkt https://requestb.in/19qlscd1 . Dieses Ereignisabonnement verwendet Standardfilter.

### Beispiel 3
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 . Dieses Ereignisabonnement verwendet Standardfilter.

### Beispiel 4
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 . Dieses Ereignisabonnement gibt die zusätzlichen Filter für Ereignistypen und Betreff an, und nur Ereignisse, die diesen Filtern entsprechen, werden an den Zielendpunkt übermittelt.

### Beispiel 5
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` des aktuell ausgewählten Azure-Abonnements mit dem angegebenen Ereignis-Hub als Ziel für Ereignisse. Dieses Ereignisabonnement verwendet Standardfilter.

### Beispiel 6
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einem EventHub-Namespace mit dem angegebenen webhhok https://requestb.in/19qlscd1 -Zielendpunkt. Dieses Ereignisabonnement verwendet Standardfilter.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpunkt
Zielendpunkt des Ereignisabonnements
Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID eines EventHub.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndpointType
Endpunkttyp.
Dies kann webhook oder eventhub sein.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Der Name des Ereignisabonnements

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludedEventType
Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inputobject
EventGrid Topic-Objekt.

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Label
Beschriftungen für das Ereignisabonnement

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe des Themas.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt werden soll.

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubjectBeginsWith
Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.
Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubjectCaseSensitive
Filter, der angibt, dass das Feld Betreff in einer Groß-/Kleinschreibung verglichen werden soll.
Wenn keine Angabe erfolgt, wird der Betreff in einem Fall unempfindlich verglichen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubjectEndsWith
Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.
Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Topicname
Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String
Microsoft. Azure. Commands. EventGrid. Models. PSTopic System. Management. Automation. Switchparameter System. String []

## Ausgaben

### Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription

## Notizen

## Verwandte Links

