---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 2aa49f01b16547987604a7ee978018596c7d9647
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664597"
---
# <span data-ttu-id="838fc-101">Get-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="838fc-101">Get-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="838fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="838fc-102">SYNOPSIS</span></span>
<span data-ttu-id="838fc-103">Abrufen von Informationen zu allen Endpunkten für Ihren viel Hub</span><span class="sxs-lookup"><span data-stu-id="838fc-103">Get information on all the endpoints for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="838fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="838fc-104">SYNTAX</span></span>

### <span data-ttu-id="838fc-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="838fc-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String>
 [-EndpointType <PSEndpointType>] [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="838fc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="838fc-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838fc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="838fc-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="838fc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="838fc-108">DESCRIPTION</span></span>
<span data-ttu-id="838fc-109">Abrufen von Informationen über den Endpunkt</span><span class="sxs-lookup"><span data-stu-id="838fc-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="838fc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="838fc-110">EXAMPLES</span></span>

### <span data-ttu-id="838fc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="838fc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="838fc-112">Rufen Sie alle Endpunkte vom "myiothub"-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="838fc-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="838fc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="838fc-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="838fc-114">Rufen Sie alle Endpunkte des Typs EventHub aus "myiothub" (viel Hub) ab.</span><span class="sxs-lookup"><span data-stu-id="838fc-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="838fc-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="838fc-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="838fc-116">Rufen Sie alle Endpunkte des Typs EventHub aus "myiothub" (viel Hub) ab.</span><span class="sxs-lookup"><span data-stu-id="838fc-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="838fc-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="838fc-117">Example 4</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="838fc-118">Rufen Sie eine Endpunkt Information vom "myiothub"-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="838fc-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="838fc-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="838fc-119">PARAMETERS</span></span>

### <span data-ttu-id="838fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838fc-120">-DefaultProfile</span></span>
<span data-ttu-id="838fc-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="838fc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="838fc-122">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="838fc-122">-EndpointName</span></span>
<span data-ttu-id="838fc-123">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="838fc-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="838fc-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="838fc-124">-EndpointType</span></span>
<span data-ttu-id="838fc-125">Typ des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="838fc-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838fc-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="838fc-126">-InputObject</span></span>
<span data-ttu-id="838fc-127">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="838fc-127">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="838fc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="838fc-128">-Name</span></span>
<span data-ttu-id="838fc-129">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="838fc-129">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838fc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="838fc-130">-ResourceGroupName</span></span>
<span data-ttu-id="838fc-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="838fc-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838fc-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="838fc-132">-ResourceId</span></span>
<span data-ttu-id="838fc-133">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="838fc-133">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838fc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838fc-134">CommonParameters</span></span>
<span data-ttu-id="838fc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838fc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838fc-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838fc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838fc-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="838fc-137">INPUTS</span></span>

### <span data-ttu-id="838fc-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="838fc-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="838fc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="838fc-139">System.String</span></span>

## <span data-ttu-id="838fc-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="838fc-140">OUTPUTS</span></span>

### <span data-ttu-id="838fc-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="838fc-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="838fc-142">System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. IotHub. Models. PSRoutingCustomEndpoint, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="838fc-142">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="838fc-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="838fc-143">NOTES</span></span>

## <span data-ttu-id="838fc-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="838fc-144">RELATED LINKS</span></span>
