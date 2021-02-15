---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152841"
---
# <span data-ttu-id="aef74-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="aef74-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="aef74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aef74-102">SYNOPSIS</span></span>
<span data-ttu-id="aef74-103">Aktualisieren einer Route in IoT Hub</span><span class="sxs-lookup"><span data-stu-id="aef74-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="aef74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aef74-104">SYNTAX</span></span>

### <span data-ttu-id="aef74-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aef74-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef74-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aef74-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef74-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aef74-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aef74-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aef74-108">DESCRIPTION</span></span>
<span data-ttu-id="aef74-109">Bearbeiten einer Route</span><span class="sxs-lookup"><span data-stu-id="aef74-109">Edit a route.</span></span> <span data-ttu-id="aef74-110">Sie können alle Felder einer Route aktualisieren, einschließlich Datenquelle, Endpunkt und Routingabfrage, und außerdem die Route aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="aef74-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="aef74-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aef74-111">EXAMPLES</span></span>

### <span data-ttu-id="aef74-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aef74-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="aef74-113">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="aef74-113">Updating the route information.</span></span>

### <span data-ttu-id="aef74-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aef74-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="aef74-115">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="aef74-115">Updating the route information.</span></span>

### <span data-ttu-id="aef74-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="aef74-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="aef74-117">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="aef74-117">Updating the route information.</span></span>

## <span data-ttu-id="aef74-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aef74-118">PARAMETERS</span></span>

### <span data-ttu-id="aef74-119">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="aef74-119">-Condition</span></span>
<span data-ttu-id="aef74-120">Bedingung, die ausgewertet wird, um die Routingregel anzuwenden</span><span class="sxs-lookup"><span data-stu-id="aef74-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="aef74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef74-121">-DefaultProfile</span></span>
<span data-ttu-id="aef74-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aef74-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aef74-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="aef74-123">-Enabled</span></span>
<span data-ttu-id="aef74-124">Route aktivieren</span><span class="sxs-lookup"><span data-stu-id="aef74-124">Enable route</span></span>

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

### <span data-ttu-id="aef74-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="aef74-125">-EndpointName</span></span>
<span data-ttu-id="aef74-126">Name des Routingendpunkts</span><span class="sxs-lookup"><span data-stu-id="aef74-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="aef74-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aef74-127">-InputObject</span></span>
<span data-ttu-id="aef74-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="aef74-128">IotHub Object</span></span>

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

### <span data-ttu-id="aef74-129">-Name</span><span class="sxs-lookup"><span data-stu-id="aef74-129">-Name</span></span>
<span data-ttu-id="aef74-130">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="aef74-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aef74-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef74-131">-ResourceGroupName</span></span>
<span data-ttu-id="aef74-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aef74-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aef74-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aef74-133">-ResourceId</span></span>
<span data-ttu-id="aef74-134">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="aef74-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aef74-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="aef74-135">-RouteName</span></span>
<span data-ttu-id="aef74-136">Name der Route</span><span class="sxs-lookup"><span data-stu-id="aef74-136">Name of the Route</span></span>

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

### <span data-ttu-id="aef74-137">-Source</span><span class="sxs-lookup"><span data-stu-id="aef74-137">-Source</span></span>
<span data-ttu-id="aef74-138">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="aef74-138">Source of the route</span></span>

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

### <span data-ttu-id="aef74-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aef74-139">-Confirm</span></span>
<span data-ttu-id="aef74-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aef74-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef74-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aef74-141">-WhatIf</span></span>
<span data-ttu-id="aef74-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aef74-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef74-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aef74-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef74-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef74-144">CommonParameters</span></span>
<span data-ttu-id="aef74-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef74-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef74-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef74-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef74-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aef74-147">INPUTS</span></span>

### <span data-ttu-id="aef74-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="aef74-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="aef74-149">System.String</span><span class="sxs-lookup"><span data-stu-id="aef74-149">System.String</span></span>

## <span data-ttu-id="aef74-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aef74-150">OUTPUTS</span></span>

### <span data-ttu-id="aef74-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="aef74-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="aef74-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aef74-152">NOTES</span></span>

## <span data-ttu-id="aef74-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aef74-153">RELATED LINKS</span></span>
