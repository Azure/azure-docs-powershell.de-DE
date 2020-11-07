---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 4df4b5415a0fffc2f2482540088b36964cfa89ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842176"
---
# <span data-ttu-id="2b04b-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="2b04b-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="2b04b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b04b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b04b-103">Aktualisieren einer Route im viel Hub</span><span class="sxs-lookup"><span data-stu-id="2b04b-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="2b04b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b04b-104">SYNTAX</span></span>

### <span data-ttu-id="2b04b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b04b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b04b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b04b-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b04b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b04b-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b04b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b04b-108">DESCRIPTION</span></span>
<span data-ttu-id="2b04b-109">Bearbeiten einer Route</span><span class="sxs-lookup"><span data-stu-id="2b04b-109">Edit a route.</span></span> <span data-ttu-id="2b04b-110">Sie können alle Felder in einer Route aktualisieren, einschließlich Datenquelle, Endpunkt, Routing Abfrage und auch aktivieren oder Deaktivieren der Route.</span><span class="sxs-lookup"><span data-stu-id="2b04b-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="2b04b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b04b-111">EXAMPLES</span></span>

### <span data-ttu-id="2b04b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2b04b-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="2b04b-113">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="2b04b-113">Updating the route information.</span></span>

### <span data-ttu-id="2b04b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2b04b-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="2b04b-115">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="2b04b-115">Updating the route information.</span></span>

### <span data-ttu-id="2b04b-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2b04b-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="2b04b-117">Aktualisieren der Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="2b04b-117">Updating the route information.</span></span>

## <span data-ttu-id="2b04b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b04b-118">PARAMETERS</span></span>

### <span data-ttu-id="2b04b-119">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="2b04b-119">-Condition</span></span>
<span data-ttu-id="2b04b-120">Bedingung, die ausgewertet wird, um die Routingregel anzuwenden</span><span class="sxs-lookup"><span data-stu-id="2b04b-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="2b04b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b04b-121">-DefaultProfile</span></span>
<span data-ttu-id="2b04b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b04b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b04b-123">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2b04b-123">-Enabled</span></span>
<span data-ttu-id="2b04b-124">Route aktivieren</span><span class="sxs-lookup"><span data-stu-id="2b04b-124">Enable route</span></span>

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

### <span data-ttu-id="2b04b-125">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="2b04b-125">-EndpointName</span></span>
<span data-ttu-id="2b04b-126">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="2b04b-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="2b04b-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2b04b-127">-InputObject</span></span>
<span data-ttu-id="2b04b-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="2b04b-128">IotHub Object</span></span>

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

### <span data-ttu-id="2b04b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2b04b-129">-Name</span></span>
<span data-ttu-id="2b04b-130">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="2b04b-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2b04b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b04b-131">-ResourceGroupName</span></span>
<span data-ttu-id="2b04b-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2b04b-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2b04b-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2b04b-133">-ResourceId</span></span>
<span data-ttu-id="2b04b-134">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2b04b-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2b04b-135">-Routename</span><span class="sxs-lookup"><span data-stu-id="2b04b-135">-RouteName</span></span>
<span data-ttu-id="2b04b-136">Name der Route</span><span class="sxs-lookup"><span data-stu-id="2b04b-136">Name of the Route</span></span>

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

### <span data-ttu-id="2b04b-137">-Source</span><span class="sxs-lookup"><span data-stu-id="2b04b-137">-Source</span></span>
<span data-ttu-id="2b04b-138">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="2b04b-138">Source of the route</span></span>

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

### <span data-ttu-id="2b04b-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b04b-139">-Confirm</span></span>
<span data-ttu-id="2b04b-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b04b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b04b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b04b-141">-WhatIf</span></span>
<span data-ttu-id="2b04b-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b04b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b04b-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b04b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b04b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b04b-144">CommonParameters</span></span>
<span data-ttu-id="2b04b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b04b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b04b-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b04b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b04b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b04b-147">INPUTS</span></span>

### <span data-ttu-id="2b04b-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2b04b-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2b04b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2b04b-149">System.String</span></span>

## <span data-ttu-id="2b04b-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b04b-150">OUTPUTS</span></span>

### <span data-ttu-id="2b04b-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="2b04b-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="2b04b-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b04b-152">NOTES</span></span>

## <span data-ttu-id="2b04b-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b04b-153">RELATED LINKS</span></span>
