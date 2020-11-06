---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502589"
---
# Get-AzureRmEventHubConsumerGroup

## Synopsis
Ruft die Details einer angegebenen Event Hubs-Verbrauchergruppe ab oder ruft eine Liste von Verbrauchergruppen in einem Ereignis-Hub ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -EventHub
EventHub Name

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Consumergroup-Name

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Namespace Name

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppen Name

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.
Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String


## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]


## Notizen

## Verwandte Links
