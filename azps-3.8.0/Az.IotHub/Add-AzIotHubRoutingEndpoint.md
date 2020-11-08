---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995157"
---
# <span data-ttu-id="573d1-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="573d1-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="573d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="573d1-102">SYNOPSIS</span></span>
<span data-ttu-id="573d1-103">Hinzufügen eines Endpunkts zu Ihrem viel-Hub</span><span class="sxs-lookup"><span data-stu-id="573d1-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="573d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="573d1-104">SYNTAX</span></span>

### <span data-ttu-id="573d1-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="573d1-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="573d1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="573d1-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="573d1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="573d1-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="573d1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="573d1-108">DESCRIPTION</span></span>
<span data-ttu-id="573d1-109">Fügen Sie einen neuen Endpunkt in Ihrem viel-Hub hinzu.</span><span class="sxs-lookup"><span data-stu-id="573d1-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="573d1-110">Informationen zu den unterstützten Endpunkten finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="573d1-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="573d1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="573d1-111">EXAMPLES</span></span>

### <span data-ttu-id="573d1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="573d1-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="573d1-113">Fügen Sie einen neuen Endpunkt "E2" vom Typ EventHub zu einem "myiothub"-Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="573d1-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="573d1-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="573d1-114">Example 2</span></span>
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

<span data-ttu-id="573d1-115">Fügen Sie einen neuen Endpunkt "S1" vom Typ AzureStorageContainer zu einem "myiothub"-Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="573d1-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="573d1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="573d1-116">PARAMETERS</span></span>

### <span data-ttu-id="573d1-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="573d1-117">-ConnectionString</span></span>
<span data-ttu-id="573d1-118">Verbindungszeichenfolge des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="573d1-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="573d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573d1-119">-DefaultProfile</span></span>
<span data-ttu-id="573d1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="573d1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="573d1-121">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="573d1-121">-EndpointName</span></span>
<span data-ttu-id="573d1-122">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="573d1-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="573d1-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="573d1-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="573d1-124">Ressourcengruppe der Endpunkt Ressource</span><span class="sxs-lookup"><span data-stu-id="573d1-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="573d1-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="573d1-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="573d1-126">Abonnement-Nr der Endpunkt Ressource</span><span class="sxs-lookup"><span data-stu-id="573d1-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="573d1-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="573d1-127">-EndpointType</span></span>
<span data-ttu-id="573d1-128">Typ des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="573d1-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="573d1-129">-Containername</span><span class="sxs-lookup"><span data-stu-id="573d1-129">-ContainerName</span></span>
<span data-ttu-id="573d1-130">Name des Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="573d1-130">Name of the storage container</span></span>

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

### <span data-ttu-id="573d1-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="573d1-131">-Encoding</span></span>
<span data-ttu-id="573d1-132">Wählen Sie das Format aus, in dem Sie Ihre Daten weiterleiten möchten.</span><span class="sxs-lookup"><span data-stu-id="573d1-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="573d1-133">Sie können JSON oder Avro auswählen.</span><span class="sxs-lookup"><span data-stu-id="573d1-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="573d1-134">Die Standardeinstellung ist auf Avro eingestellt.</span><span class="sxs-lookup"><span data-stu-id="573d1-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="573d1-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="573d1-135">-InputObject</span></span>
<span data-ttu-id="573d1-136">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="573d1-136">IotHub Object</span></span>

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

### <span data-ttu-id="573d1-137">-Name</span><span class="sxs-lookup"><span data-stu-id="573d1-137">-Name</span></span>
<span data-ttu-id="573d1-138">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="573d1-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="573d1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573d1-139">-ResourceGroupName</span></span>
<span data-ttu-id="573d1-140">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="573d1-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="573d1-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="573d1-141">-ResourceId</span></span>
<span data-ttu-id="573d1-142">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="573d1-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="573d1-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="573d1-143">-Confirm</span></span>
<span data-ttu-id="573d1-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="573d1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="573d1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573d1-145">-WhatIf</span></span>
<span data-ttu-id="573d1-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="573d1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573d1-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="573d1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="573d1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573d1-148">CommonParameters</span></span>
<span data-ttu-id="573d1-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573d1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573d1-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573d1-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573d1-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="573d1-151">INPUTS</span></span>

### <span data-ttu-id="573d1-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="573d1-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="573d1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="573d1-153">System.String</span></span>

## <span data-ttu-id="573d1-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="573d1-154">OUTPUTS</span></span>

### <span data-ttu-id="573d1-155">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="573d1-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="573d1-156">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="573d1-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="573d1-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="573d1-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="573d1-158">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="573d1-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="573d1-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="573d1-159">NOTES</span></span>

## <span data-ttu-id="573d1-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="573d1-160">RELATED LINKS</span></span>
