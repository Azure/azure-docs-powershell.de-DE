---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356920"
---
# <span data-ttu-id="6820a-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="6820a-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="6820a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6820a-102">SYNOPSIS</span></span>
<span data-ttu-id="6820a-103">Löschen eines Endpunkts für Ihren IoT Hub</span><span class="sxs-lookup"><span data-stu-id="6820a-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="6820a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6820a-104">SYNTAX</span></span>

### <span data-ttu-id="6820a-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6820a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6820a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6820a-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6820a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6820a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6820a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6820a-108">DESCRIPTION</span></span>
<span data-ttu-id="6820a-109">Löschen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="6820a-109">Delete an endpoint.</span></span> <span data-ttu-id="6820a-110">Denken Sie daran, alle Routen zu löschen, die diesen Endpunkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="6820a-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="6820a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6820a-111">EXAMPLES</span></span>

### <span data-ttu-id="6820a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6820a-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="6820a-113">Löschen Sie den Endpunkt "E2" aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="6820a-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="6820a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6820a-114">PARAMETERS</span></span>

### <span data-ttu-id="6820a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6820a-115">-DefaultProfile</span></span>
<span data-ttu-id="6820a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6820a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6820a-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6820a-117">-EndpointName</span></span>
<span data-ttu-id="6820a-118">Name des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="6820a-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="6820a-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="6820a-119">-EndpointType</span></span>
<span data-ttu-id="6820a-120">Typ des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="6820a-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="6820a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6820a-121">-InputObject</span></span>
<span data-ttu-id="6820a-122">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="6820a-122">IotHub Object</span></span>

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

### <span data-ttu-id="6820a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6820a-123">-Name</span></span>
<span data-ttu-id="6820a-124">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="6820a-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6820a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6820a-125">-PassThru</span></span>
<span data-ttu-id="6820a-126">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="6820a-126">Allows to return the boolean object.</span></span> <span data-ttu-id="6820a-127">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6820a-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6820a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6820a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6820a-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6820a-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6820a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6820a-130">-ResourceId</span></span>
<span data-ttu-id="6820a-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6820a-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6820a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6820a-132">-Confirm</span></span>
<span data-ttu-id="6820a-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6820a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6820a-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6820a-134">-WhatIf</span></span>
<span data-ttu-id="6820a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6820a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6820a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6820a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6820a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6820a-137">CommonParameters</span></span>
<span data-ttu-id="6820a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6820a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6820a-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6820a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6820a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6820a-140">INPUTS</span></span>

### <span data-ttu-id="6820a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6820a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6820a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6820a-142">System.String</span></span>

## <span data-ttu-id="6820a-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6820a-143">OUTPUTS</span></span>

### <span data-ttu-id="6820a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6820a-144">System.Boolean</span></span>

## <span data-ttu-id="6820a-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6820a-145">NOTES</span></span>

## <span data-ttu-id="6820a-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6820a-146">RELATED LINKS</span></span>
