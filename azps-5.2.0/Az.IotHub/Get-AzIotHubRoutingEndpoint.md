---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371131"
---
# <span data-ttu-id="e88a6-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="e88a6-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="e88a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e88a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e88a6-103">Informationen zu allen Endpunkten für Ihren IoT Hub erhalten</span><span class="sxs-lookup"><span data-stu-id="e88a6-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="e88a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e88a6-104">SYNTAX</span></span>

### <span data-ttu-id="e88a6-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e88a6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e88a6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e88a6-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e88a6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e88a6-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e88a6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e88a6-108">DESCRIPTION</span></span>
<span data-ttu-id="e88a6-109">Informationen zum Endpunkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="e88a6-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="e88a6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e88a6-110">EXAMPLES</span></span>

### <span data-ttu-id="e88a6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e88a6-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="e88a6-112">Abrufen aller Endpunkte aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e88a6-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e88a6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e88a6-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="e88a6-114">Abrufen aller Endpunkte vom Typ "EventHub" aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e88a6-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="e88a6-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e88a6-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="e88a6-116">Abrufen aller Endpunkte vom Typ "EventHub" aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e88a6-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e88a6-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e88a6-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="e88a6-118">Abrufen von Endpunktinformationen aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e88a6-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="e88a6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e88a6-119">PARAMETERS</span></span>

### <span data-ttu-id="e88a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88a6-120">-DefaultProfile</span></span>
<span data-ttu-id="e88a6-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e88a6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88a6-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e88a6-122">-EndpointName</span></span>
<span data-ttu-id="e88a6-123">Name des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="e88a6-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="e88a6-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="e88a6-124">-EndpointType</span></span>
<span data-ttu-id="e88a6-125">Typ des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="e88a6-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="e88a6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e88a6-126">-InputObject</span></span>
<span data-ttu-id="e88a6-127">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e88a6-127">IotHub Object</span></span>

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

### <span data-ttu-id="e88a6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e88a6-128">-Name</span></span>
<span data-ttu-id="e88a6-129">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="e88a6-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e88a6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88a6-130">-ResourceGroupName</span></span>
<span data-ttu-id="e88a6-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e88a6-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e88a6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e88a6-132">-ResourceId</span></span>
<span data-ttu-id="e88a6-133">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e88a6-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e88a6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88a6-134">CommonParameters</span></span>
<span data-ttu-id="e88a6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88a6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88a6-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88a6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88a6-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e88a6-137">INPUTS</span></span>

### <span data-ttu-id="e88a6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e88a6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e88a6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e88a6-139">System.String</span></span>

## <span data-ttu-id="e88a6-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e88a6-140">OUTPUTS</span></span>

### <span data-ttu-id="e88a6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="e88a6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="e88a6-142">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e88a6-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e88a6-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="e88a6-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="e88a6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="e88a6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="e88a6-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="e88a6-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="e88a6-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="e88a6-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="e88a6-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e88a6-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="e88a6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="e88a6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="e88a6-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="e88a6-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="e88a6-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e88a6-150">NOTES</span></span>

## <span data-ttu-id="e88a6-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e88a6-151">RELATED LINKS</span></span>
