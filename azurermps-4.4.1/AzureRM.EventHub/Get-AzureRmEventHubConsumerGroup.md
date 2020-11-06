---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505029"
---
# Get-AzureRmEventHubConsumerGroup

## Synopsis
Ruft die Details einer angegebenen Event Hubs-Verbrauchergruppe ab oder ruft eine Liste von Verbrauchergruppen in einem Ereignis-Hub ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## Beschreibung
Das Get-AzureRmEventHubConsumerGroup-Cmdlet ruft entweder die Details einer angegebenen Event Hubs-Verbrauchergruppe oder eine Liste von Verbrauchergruppen in einem bestimmten Ereignis-Hub ab.
Wenn der Name einer Consumer-Gruppe bereitgestellt wird, werden die Details einer einzelnen Consumer-Gruppe zurückgegeben.
Wenn der Name einer Consumer-Gruppe nicht angegeben wird, wird eine Liste der Verbrauchergruppen im angegebenen Ereignis-Hub zurückgegeben.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

Ruft die Gruppe der \` Consumer \` -MyConsumerGroupName im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .

### Beispiel 2
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Ruft eine Liste der Verbrauchergruppen im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .

## Parameter

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHub
EventHub-Name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Consumergroup-Name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Namespace Name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## Eingaben

### System. String

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## Notizen

## Verwandte Links

