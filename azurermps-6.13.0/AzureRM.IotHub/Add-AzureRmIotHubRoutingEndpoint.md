---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482422"
---
# <span data-ttu-id="1774e-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="1774e-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="1774e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1774e-102">SYNOPSIS</span></span>
<span data-ttu-id="1774e-103">Hinzufügen eines Endpunkts zu Ihrem viel-Hub</span><span class="sxs-lookup"><span data-stu-id="1774e-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1774e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1774e-104">SYNTAX</span></span>

### <span data-ttu-id="1774e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1774e-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1774e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1774e-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1774e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1774e-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1774e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1774e-108">DESCRIPTION</span></span>
<span data-ttu-id="1774e-109">Fügen Sie einen neuen Endpunkt in Ihrem viel-Hub hinzu.</span><span class="sxs-lookup"><span data-stu-id="1774e-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="1774e-110">Informationen zu den unterstützten Endpunkten finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="1774e-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="1774e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1774e-111">EXAMPLES</span></span>

### <span data-ttu-id="1774e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1774e-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="1774e-113">Fügen Sie einen neuen Endpunkt "E2" vom Typ EventHub zu einem "myiothub"-Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="1774e-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="1774e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1774e-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="1774e-115">Fügen Sie einen neuen Endpunkt "S1" vom Typ AzureStorageContainer zu einem "myiothub"-Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="1774e-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="1774e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="1774e-116">PARAMETERS</span></span>

### <span data-ttu-id="1774e-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1774e-117">-ConnectionString</span></span>
<span data-ttu-id="1774e-118">Verbindungszeichenfolge des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="1774e-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1774e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1774e-119">-DefaultProfile</span></span>
<span data-ttu-id="1774e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1774e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1774e-121">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="1774e-121">-EndpointName</span></span>
<span data-ttu-id="1774e-122">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="1774e-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="1774e-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1774e-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="1774e-124">Ressourcengruppe der Endpunkt Resoure</span><span class="sxs-lookup"><span data-stu-id="1774e-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1774e-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1774e-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="1774e-126">Abonnement-Nr der Endpunkt Ressource</span><span class="sxs-lookup"><span data-stu-id="1774e-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1774e-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="1774e-127">-EndpointType</span></span>
<span data-ttu-id="1774e-128">Typ des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="1774e-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1774e-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1774e-129">-InputObject</span></span>
<span data-ttu-id="1774e-130">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="1774e-130">IotHub Object</span></span>

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

### <span data-ttu-id="1774e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1774e-131">-Name</span></span>
<span data-ttu-id="1774e-132">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="1774e-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1774e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1774e-133">-ResourceGroupName</span></span>
<span data-ttu-id="1774e-134">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1774e-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1774e-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1774e-135">-ResourceId</span></span>
<span data-ttu-id="1774e-136">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1774e-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1774e-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1774e-137">-Confirm</span></span>
<span data-ttu-id="1774e-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1774e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1774e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1774e-139">-WhatIf</span></span>
<span data-ttu-id="1774e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1774e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1774e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1774e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1774e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1774e-142">CommonParameters</span></span>
<span data-ttu-id="1774e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1774e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1774e-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1774e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1774e-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1774e-145">INPUTS</span></span>

### <span data-ttu-id="1774e-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1774e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="1774e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1774e-147">System.String</span></span>

## <span data-ttu-id="1774e-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1774e-148">OUTPUTS</span></span>

### <span data-ttu-id="1774e-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="1774e-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="1774e-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1774e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="1774e-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="1774e-151">NOTES</span></span>

## <span data-ttu-id="1774e-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1774e-152">RELATED LINKS</span></span>
