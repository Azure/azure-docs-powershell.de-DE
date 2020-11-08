---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174715"
---
# <span data-ttu-id="938ae-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="938ae-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="938ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="938ae-102">SYNOPSIS</span></span>
<span data-ttu-id="938ae-103">Aktualisieren einer Route im viel Hub</span><span class="sxs-lookup"><span data-stu-id="938ae-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="938ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="938ae-104">SYNTAX</span></span>

### <span data-ttu-id="938ae-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="938ae-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="938ae-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="938ae-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="938ae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="938ae-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="938ae-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="938ae-108">DESCRIPTION</span></span>
<span data-ttu-id="938ae-109">Bearbeiten einer Route</span><span class="sxs-lookup"><span data-stu-id="938ae-109">Edit a route.</span></span> <span data-ttu-id="938ae-110">Sie können alle Felder in einer Route aktualisieren, einschließlich Datenquelle, Endpunkt, Routing Abfrage und auch aktivieren oder Deaktivieren der Route.</span><span class="sxs-lookup"><span data-stu-id="938ae-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="938ae-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="938ae-111">EXAMPLES</span></span>

### <span data-ttu-id="938ae-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="938ae-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="938ae-113">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="938ae-113">Updating the route information.</span></span>

### <span data-ttu-id="938ae-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="938ae-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="938ae-115">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="938ae-115">Updating the route information.</span></span>

### <span data-ttu-id="938ae-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="938ae-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="938ae-117">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="938ae-117">Updating the route information.</span></span>

## <span data-ttu-id="938ae-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="938ae-118">PARAMETERS</span></span>

### <span data-ttu-id="938ae-119">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="938ae-119">-Condition</span></span>
<span data-ttu-id="938ae-120">Bedingung, die ausgewertet wird, um die Routingregel anzuwenden</span><span class="sxs-lookup"><span data-stu-id="938ae-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="938ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="938ae-121">-DefaultProfile</span></span>
<span data-ttu-id="938ae-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="938ae-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="938ae-123">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="938ae-123">-Enabled</span></span>
<span data-ttu-id="938ae-124">Route aktivieren</span><span class="sxs-lookup"><span data-stu-id="938ae-124">Enable route</span></span>

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

### <span data-ttu-id="938ae-125">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="938ae-125">-EndpointName</span></span>
<span data-ttu-id="938ae-126">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="938ae-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="938ae-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="938ae-127">-InputObject</span></span>
<span data-ttu-id="938ae-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="938ae-128">IotHub Object</span></span>

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

### <span data-ttu-id="938ae-129">-Name</span><span class="sxs-lookup"><span data-stu-id="938ae-129">-Name</span></span>
<span data-ttu-id="938ae-130">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="938ae-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="938ae-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="938ae-131">-ResourceGroupName</span></span>
<span data-ttu-id="938ae-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="938ae-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="938ae-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="938ae-133">-ResourceId</span></span>
<span data-ttu-id="938ae-134">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="938ae-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="938ae-135">-Routename</span><span class="sxs-lookup"><span data-stu-id="938ae-135">-RouteName</span></span>
<span data-ttu-id="938ae-136">Name der Route</span><span class="sxs-lookup"><span data-stu-id="938ae-136">Name of the Route</span></span>

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

### <span data-ttu-id="938ae-137">-Source</span><span class="sxs-lookup"><span data-stu-id="938ae-137">-Source</span></span>
<span data-ttu-id="938ae-138">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="938ae-138">Source of the route</span></span>

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

### <span data-ttu-id="938ae-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="938ae-139">-Confirm</span></span>
<span data-ttu-id="938ae-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="938ae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="938ae-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="938ae-141">-WhatIf</span></span>
<span data-ttu-id="938ae-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="938ae-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="938ae-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="938ae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="938ae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="938ae-144">CommonParameters</span></span>
<span data-ttu-id="938ae-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="938ae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="938ae-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="938ae-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="938ae-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="938ae-147">INPUTS</span></span>

### <span data-ttu-id="938ae-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="938ae-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="938ae-149">System. String</span><span class="sxs-lookup"><span data-stu-id="938ae-149">System.String</span></span>

## <span data-ttu-id="938ae-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="938ae-150">OUTPUTS</span></span>

### <span data-ttu-id="938ae-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="938ae-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="938ae-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="938ae-152">NOTES</span></span>

## <span data-ttu-id="938ae-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="938ae-153">RELATED LINKS</span></span>
