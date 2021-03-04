---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1b14ce37d03e1840336696792493e30701a09bfe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942491"
---
# <span data-ttu-id="b8646-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8646-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="b8646-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8646-102">SYNOPSIS</span></span>
<span data-ttu-id="b8646-103">Löschen eines Endpunkts für Ihren IoT Hub</span><span class="sxs-lookup"><span data-stu-id="b8646-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="b8646-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8646-104">SYNTAX</span></span>

### <span data-ttu-id="b8646-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8646-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8646-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8646-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8646-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8646-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8646-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8646-108">DESCRIPTION</span></span>
<span data-ttu-id="b8646-109">Löschen Sie einen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b8646-109">Delete an endpoint.</span></span> <span data-ttu-id="b8646-110">Denken Sie daran, alle Routen zu löschen, die diesen Endpunkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8646-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="b8646-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8646-111">EXAMPLES</span></span>

### <span data-ttu-id="b8646-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8646-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="b8646-113">Löschen Sie endpunkt "E2" aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="b8646-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b8646-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b8646-114">PARAMETERS</span></span>

### <span data-ttu-id="b8646-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8646-115">-DefaultProfile</span></span>
<span data-ttu-id="b8646-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8646-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8646-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b8646-117">-EndpointName</span></span>
<span data-ttu-id="b8646-118">Name des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="b8646-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="b8646-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="b8646-119">-EndpointType</span></span>
<span data-ttu-id="b8646-120">Typ des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="b8646-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="b8646-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8646-121">-InputObject</span></span>
<span data-ttu-id="b8646-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b8646-122">IotHub Object</span></span>

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

### <span data-ttu-id="b8646-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b8646-123">-Name</span></span>
<span data-ttu-id="b8646-124">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="b8646-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b8646-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8646-125">-PassThru</span></span>
<span data-ttu-id="b8646-126">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="b8646-126">Allows to return the boolean object.</span></span> <span data-ttu-id="b8646-127">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b8646-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8646-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8646-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8646-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b8646-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b8646-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8646-130">-ResourceId</span></span>
<span data-ttu-id="b8646-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b8646-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b8646-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8646-132">-Confirm</span></span>
<span data-ttu-id="b8646-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8646-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8646-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8646-134">-WhatIf</span></span>
<span data-ttu-id="b8646-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8646-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8646-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8646-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8646-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8646-137">CommonParameters</span></span>
<span data-ttu-id="b8646-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8646-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8646-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8646-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8646-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8646-140">INPUTS</span></span>

### <span data-ttu-id="b8646-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b8646-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b8646-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b8646-142">System.String</span></span>

## <span data-ttu-id="b8646-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8646-143">OUTPUTS</span></span>

### <span data-ttu-id="b8646-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8646-144">System.Boolean</span></span>

## <span data-ttu-id="b8646-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b8646-145">NOTES</span></span>

## <span data-ttu-id="b8646-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b8646-146">RELATED LINKS</span></span>
