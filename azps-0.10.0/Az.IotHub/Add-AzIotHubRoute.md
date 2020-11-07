---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: 3828b6ef95c629362ce0082d6bb97e2af1ccb687
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843967"
---
# <span data-ttu-id="48d9d-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="48d9d-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="48d9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="48d9d-103">Erstellen einer Route im viel Hub</span><span class="sxs-lookup"><span data-stu-id="48d9d-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="48d9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48d9d-104">SYNTAX</span></span>

### <span data-ttu-id="48d9d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="48d9d-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d9d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="48d9d-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d9d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="48d9d-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48d9d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48d9d-108">DESCRIPTION</span></span>
<span data-ttu-id="48d9d-109">Erstellen Sie eine Route, um bestimmte Datenquelle und-Bedingung an einen gewünschten Endpunkt zu senden.</span><span class="sxs-lookup"><span data-stu-id="48d9d-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="48d9d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48d9d-110">EXAMPLES</span></span>

### <span data-ttu-id="48d9d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48d9d-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="48d9d-112">Erstellen Sie eine neue Route "R1".</span><span class="sxs-lookup"><span data-stu-id="48d9d-112">Create a new route "R1".</span></span>

## <span data-ttu-id="48d9d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="48d9d-113">PARAMETERS</span></span>

### <span data-ttu-id="48d9d-114">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="48d9d-114">-Condition</span></span>
<span data-ttu-id="48d9d-115">Bedingung, die ausgewertet wird, um die Routingregel anzuwenden</span><span class="sxs-lookup"><span data-stu-id="48d9d-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="48d9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d9d-116">-DefaultProfile</span></span>
<span data-ttu-id="48d9d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48d9d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d9d-118">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="48d9d-118">-Enabled</span></span>
<span data-ttu-id="48d9d-119">Route aktivieren</span><span class="sxs-lookup"><span data-stu-id="48d9d-119">Enable route</span></span>

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

### <span data-ttu-id="48d9d-120">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="48d9d-120">-EndpointName</span></span>
<span data-ttu-id="48d9d-121">Name des Routing Endpunkts</span><span class="sxs-lookup"><span data-stu-id="48d9d-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="48d9d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48d9d-122">-InputObject</span></span>
<span data-ttu-id="48d9d-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="48d9d-123">IotHub Object</span></span>

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

### <span data-ttu-id="48d9d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="48d9d-124">-Name</span></span>
<span data-ttu-id="48d9d-125">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="48d9d-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="48d9d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d9d-126">-ResourceGroupName</span></span>
<span data-ttu-id="48d9d-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="48d9d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="48d9d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="48d9d-128">-ResourceId</span></span>
<span data-ttu-id="48d9d-129">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="48d9d-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="48d9d-130">-Routename</span><span class="sxs-lookup"><span data-stu-id="48d9d-130">-RouteName</span></span>
<span data-ttu-id="48d9d-131">Name der Route</span><span class="sxs-lookup"><span data-stu-id="48d9d-131">Name of the Route</span></span>

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

### <span data-ttu-id="48d9d-132">-Source</span><span class="sxs-lookup"><span data-stu-id="48d9d-132">-Source</span></span>
<span data-ttu-id="48d9d-133">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="48d9d-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d9d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48d9d-134">-Confirm</span></span>
<span data-ttu-id="48d9d-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48d9d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d9d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d9d-136">-WhatIf</span></span>
<span data-ttu-id="48d9d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48d9d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48d9d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48d9d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d9d-139">CommonParameters</span></span>
<span data-ttu-id="48d9d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d9d-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d9d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d9d-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48d9d-142">INPUTS</span></span>

### <span data-ttu-id="48d9d-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="48d9d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="48d9d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="48d9d-144">System.String</span></span>

## <span data-ttu-id="48d9d-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48d9d-145">OUTPUTS</span></span>

### <span data-ttu-id="48d9d-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="48d9d-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="48d9d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="48d9d-147">NOTES</span></span>

## <span data-ttu-id="48d9d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48d9d-148">RELATED LINKS</span></span>
