---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 26e306c80f18f3e7d14ca073cfdedfbdc9e6567b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663585"
---
# Get-AzureRmEventGridSubscription

## Synopsis
Ruft die Details eines Ereignisabonnements ab oder ruft eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### EventSubscriptionTopicNameParameterSet (Standard)
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionInputObjectSet
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Get-AzureRmEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Abonnements oder eine Liste aller Ereignis Raster Abonnements im aktuellen Azure-Abonnement oder in der Ressourcengruppe ab.
Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Ereignis Raster-Abonnements zurückgegeben.
Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das Thema \` THEMA1 hat in der \` Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .

### Beispiel 2
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für \` das Thema THEMA1 hat in der \` Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` , einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein webhook-basiertes Ereignisabonnement handelt.

### Beispiel 3
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Rufen Sie eine Liste aller Ereignisabonnements ab, die für Topic \` THEMA1 hat \` in der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .

### Beispiel 4
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für die Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` .

### Beispiel 5
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das aktuell ausgewählte Azure-Abonnement erstellt wurden.

### Beispiel 6
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .

### Beispiel 7
```
PS C:\> Get-AzureRmEventGridSubscription
```

Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden.

### Beispiel 8
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Ruft die Liste aller regionalen Ereignisabonnements ab, die unter Ressourcengruppen- \` MyResourceGroupName \` im angegebenen Speicherort westus2 erstellt wurden \` \` .

### Beispiel 9
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen EventHub-Namespace erstellt wurden.

### Beispiel 10
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Topic-Typ (EventHub-Namespaces) an der angegebenen Position erstellt wurden.

### Beispiel 11
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Ruft die Liste aller Ereignisabonnements ab, die für die jeweilige Ressourcengruppe erstellt wurden.

## Parameter

### -EventSubscriptionName
Der Name des Ereignisabonnements

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
EventGrid-Ereignisabonnement Objekt.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
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

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String
Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription
System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscriptionListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

## Notizen

## Verwandte Links

