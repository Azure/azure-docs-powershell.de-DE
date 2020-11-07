---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8852139cfcedc5ff0ee42c234c44b1505042ef1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650969"
---
# <span data-ttu-id="d5bf4-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5bf4-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="d5bf4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bf4-103">Abrufen von Informationen zu allen Endpunkten für Ihren viel Hub</span><span class="sxs-lookup"><span data-stu-id="d5bf4-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="d5bf4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5bf4-104">SYNTAX</span></span>

### <span data-ttu-id="d5bf4-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5bf4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5bf4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5bf4-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5bf4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5bf4-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5bf4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5bf4-108">DESCRIPTION</span></span>
<span data-ttu-id="d5bf4-109">Abrufen von Informationen über den Endpunkt</span><span class="sxs-lookup"><span data-stu-id="d5bf4-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="d5bf4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5bf4-110">EXAMPLES</span></span>

### <span data-ttu-id="d5bf4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5bf4-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="d5bf4-112">Rufen Sie alle Endpunkte vom "myiothub"-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="d5bf4-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d5bf4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5bf4-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="d5bf4-114">Rufen Sie alle Endpunkte des Typs EventHub aus "myiothub" (viel Hub) ab.</span><span class="sxs-lookup"><span data-stu-id="d5bf4-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="d5bf4-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d5bf4-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="d5bf4-116">Rufen Sie alle Endpunkte des Typs EventHub aus "myiothub" (viel Hub) ab.</span><span class="sxs-lookup"><span data-stu-id="d5bf4-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d5bf4-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d5bf4-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="d5bf4-118">Rufen Sie eine Endpunkt Information vom "myiothub"-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="d5bf4-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="d5bf4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5bf4-119">PARAMETERS</span></span>

### <span data-ttu-id="d5bf4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bf4-120">-DefaultProfile</span></span>
<span data-ttu-id="d5bf4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5bf4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5bf4-122">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="d5bf4-122">-EndpointName</span></span>
<span data-ttu-id="d5bf4-123">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="d5bf4-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="d5bf4-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="d5bf4-124">-EndpointType</span></span>
<span data-ttu-id="d5bf4-125">Typ des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="d5bf4-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="d5bf4-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5bf4-126">-InputObject</span></span>
<span data-ttu-id="d5bf4-127">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="d5bf4-127">IotHub Object</span></span>

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

### <span data-ttu-id="d5bf4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d5bf4-128">-Name</span></span>
<span data-ttu-id="d5bf4-129">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="d5bf4-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d5bf4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5bf4-130">-ResourceGroupName</span></span>
<span data-ttu-id="d5bf4-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d5bf4-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d5bf4-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d5bf4-132">-ResourceId</span></span>
<span data-ttu-id="d5bf4-133">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d5bf4-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d5bf4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bf4-134">CommonParameters</span></span>
<span data-ttu-id="d5bf4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bf4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bf4-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5bf4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bf4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5bf4-137">INPUTS</span></span>

### <span data-ttu-id="d5bf4-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d5bf4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d5bf4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d5bf4-139">System.String</span></span>

## <span data-ttu-id="d5bf4-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5bf4-140">OUTPUTS</span></span>

### <span data-ttu-id="d5bf4-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5bf4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="d5bf4-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. Cmdlets. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d5bf4-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d5bf4-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5bf4-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="d5bf4-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="d5bf4-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="d5bf4-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5bf4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="d5bf4-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="d5bf4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="d5bf4-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5bf4-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="d5bf4-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="d5bf4-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="d5bf4-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="d5bf4-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="d5bf4-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5bf4-150">NOTES</span></span>

## <span data-ttu-id="d5bf4-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5bf4-151">RELATED LINKS</span></span>
