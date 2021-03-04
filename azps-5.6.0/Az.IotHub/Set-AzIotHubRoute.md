---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 2cac00b1510c658b01d815d281ef16cef02b1dc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945125"
---
# <span data-ttu-id="c808f-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c808f-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="c808f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c808f-102">SYNOPSIS</span></span>
<span data-ttu-id="c808f-103">Aktualisieren einer Route in IoT Hub</span><span class="sxs-lookup"><span data-stu-id="c808f-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="c808f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c808f-104">SYNTAX</span></span>

### <span data-ttu-id="c808f-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c808f-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c808f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c808f-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c808f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c808f-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c808f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c808f-108">DESCRIPTION</span></span>
<span data-ttu-id="c808f-109">Bearbeiten einer Route</span><span class="sxs-lookup"><span data-stu-id="c808f-109">Edit a route.</span></span> <span data-ttu-id="c808f-110">Sie können alle Felder in einer Route aktualisieren, einschließlich Datenquelle, Endpunkt, Routingabfrage, sowie die Route aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c808f-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="c808f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c808f-111">EXAMPLES</span></span>

### <span data-ttu-id="c808f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c808f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="c808f-113">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="c808f-113">Updating the route information.</span></span>

### <span data-ttu-id="c808f-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c808f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="c808f-115">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="c808f-115">Updating the route information.</span></span>

### <span data-ttu-id="c808f-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c808f-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="c808f-117">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="c808f-117">Updating the route information.</span></span>

## <span data-ttu-id="c808f-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c808f-118">PARAMETERS</span></span>

### <span data-ttu-id="c808f-119">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="c808f-119">-Condition</span></span>
<span data-ttu-id="c808f-120">Bedingung, die ausgewertet wird, um die Routingregel anzuwenden</span><span class="sxs-lookup"><span data-stu-id="c808f-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="c808f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c808f-121">-DefaultProfile</span></span>
<span data-ttu-id="c808f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c808f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c808f-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c808f-123">-Enabled</span></span>
<span data-ttu-id="c808f-124">Route aktivieren</span><span class="sxs-lookup"><span data-stu-id="c808f-124">Enable route</span></span>

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

### <span data-ttu-id="c808f-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c808f-125">-EndpointName</span></span>
<span data-ttu-id="c808f-126">Name des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="c808f-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="c808f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c808f-127">-InputObject</span></span>
<span data-ttu-id="c808f-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="c808f-128">IotHub Object</span></span>

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

### <span data-ttu-id="c808f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c808f-129">-Name</span></span>
<span data-ttu-id="c808f-130">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="c808f-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c808f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c808f-131">-ResourceGroupName</span></span>
<span data-ttu-id="c808f-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c808f-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c808f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c808f-133">-ResourceId</span></span>
<span data-ttu-id="c808f-134">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c808f-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c808f-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c808f-135">-RouteName</span></span>
<span data-ttu-id="c808f-136">Name der Route</span><span class="sxs-lookup"><span data-stu-id="c808f-136">Name of the Route</span></span>

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

### <span data-ttu-id="c808f-137">-Source</span><span class="sxs-lookup"><span data-stu-id="c808f-137">-Source</span></span>
<span data-ttu-id="c808f-138">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="c808f-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c808f-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c808f-139">-Confirm</span></span>
<span data-ttu-id="c808f-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c808f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c808f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c808f-141">-WhatIf</span></span>
<span data-ttu-id="c808f-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c808f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c808f-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c808f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c808f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c808f-144">CommonParameters</span></span>
<span data-ttu-id="c808f-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c808f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c808f-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c808f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c808f-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c808f-147">INPUTS</span></span>

### <span data-ttu-id="c808f-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c808f-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c808f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c808f-149">System.String</span></span>

## <span data-ttu-id="c808f-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c808f-150">OUTPUTS</span></span>

### <span data-ttu-id="c808f-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="c808f-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="c808f-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c808f-152">NOTES</span></span>

## <span data-ttu-id="c808f-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c808f-153">RELATED LINKS</span></span>
