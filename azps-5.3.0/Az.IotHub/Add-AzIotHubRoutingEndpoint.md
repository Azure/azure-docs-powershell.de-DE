---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472420"
---
# <span data-ttu-id="2b6e8-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b6e8-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="2b6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6e8-103">Hinzufügen eines Endpunkts zu Ihrem IoT Hub</span><span class="sxs-lookup"><span data-stu-id="2b6e8-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="2b6e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b6e8-104">SYNTAX</span></span>

### <span data-ttu-id="2b6e8-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b6e8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b6e8-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b6e8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b6e8-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b6e8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b6e8-108">DESCRIPTION</span></span>
<span data-ttu-id="2b6e8-109">Fügen Sie einen neuen Endpunkt in Ihrem IoT Hub hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="2b6e8-110">Weitere Informationen zu den unterstützten Endpunkten finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="2b6e8-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="2b6e8-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b6e8-111">EXAMPLES</span></span>

### <span data-ttu-id="2b6e8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2b6e8-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="2b6e8-113">Fügen Sie einen neuen Endpunkt vom Typ "E2" EventHub zu einem IoT Hub vom Typ "myiothub" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="2b6e8-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2b6e8-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="2b6e8-115">Fügen Sie einem "myiothub" IoT Hub einen neuen Endpunkt "S1" vom Typ "AzureStorageContainer" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="2b6e8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b6e8-116">PARAMETERS</span></span>

### <span data-ttu-id="2b6e8-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2b6e8-117">-ConnectionString</span></span>
<span data-ttu-id="2b6e8-118">Verbindungszeichenfolge des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="2b6e8-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6e8-119">-DefaultProfile</span></span>
<span data-ttu-id="2b6e8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b6e8-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2b6e8-121">-EndpointName</span></span>
<span data-ttu-id="2b6e8-122">Name des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="2b6e8-122">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b6e8-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="2b6e8-124">Ressourcengruppe der Endpunktressource</span><span class="sxs-lookup"><span data-stu-id="2b6e8-124">Resource group of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b6e8-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="2b6e8-126">SubscriptionId der Endpunktressource</span><span class="sxs-lookup"><span data-stu-id="2b6e8-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="2b6e8-127">-EndpointType</span></span>
<span data-ttu-id="2b6e8-128">Typ des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="2b6e8-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2b6e8-129">-ContainerName</span></span>
<span data-ttu-id="2b6e8-130">Name des Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="2b6e8-130">Name of the storage container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="2b6e8-131">-Encoding</span></span>
<span data-ttu-id="2b6e8-132">Wählen Sie das Format aus, in dem Sie Ihre Daten routen möchten.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="2b6e8-133">Sie können JSON oder AVRO auswählen.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="2b6e8-134">Der Standardwert ist AVRO.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b6e8-135">-InputObject</span></span>
<span data-ttu-id="2b6e8-136">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="2b6e8-136">IotHub Object</span></span>

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

### <span data-ttu-id="2b6e8-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2b6e8-137">-Name</span></span>
<span data-ttu-id="2b6e8-138">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="2b6e8-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2b6e8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b6e8-139">-ResourceGroupName</span></span>
<span data-ttu-id="2b6e8-140">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2b6e8-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2b6e8-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b6e8-141">-ResourceId</span></span>
<span data-ttu-id="2b6e8-142">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2b6e8-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2b6e8-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b6e8-143">-Confirm</span></span>
<span data-ttu-id="2b6e8-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2b6e8-145">-WhatIf</span></span>
<span data-ttu-id="2b6e8-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b6e8-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6e8-148">CommonParameters</span></span>
<span data-ttu-id="2b6e8-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6e8-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6e8-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b6e8-151">INPUTS</span></span>

### <span data-ttu-id="2b6e8-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2b6e8-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2b6e8-153">System.String</span><span class="sxs-lookup"><span data-stu-id="2b6e8-153">System.String</span></span>

## <span data-ttu-id="2b6e8-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b6e8-154">OUTPUTS</span></span>

### <span data-ttu-id="2b6e8-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b6e8-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="2b6e8-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b6e8-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="2b6e8-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b6e8-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="2b6e8-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b6e8-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="2b6e8-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2b6e8-159">NOTES</span></span>

## <span data-ttu-id="2b6e8-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2b6e8-160">RELATED LINKS</span></span>
