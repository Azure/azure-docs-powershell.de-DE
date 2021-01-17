---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361750"
---
# <span data-ttu-id="e2d33-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e2d33-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="e2d33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d33-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d33-103">Testen von Routen in IoT Hub</span><span class="sxs-lookup"><span data-stu-id="e2d33-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="e2d33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2d33-104">SYNTAX</span></span>

### <span data-ttu-id="e2d33-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e2d33-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d33-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e2d33-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d33-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e2d33-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2d33-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e2d33-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d33-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e2d33-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2d33-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e2d33-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d33-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e2d33-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2d33-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2d33-112">DESCRIPTION</span></span>
<span data-ttu-id="e2d33-113">Testen Sie eine bestimmte Route.</span><span class="sxs-lookup"><span data-stu-id="e2d33-113">Test a specific route.</span></span>

## <span data-ttu-id="e2d33-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2d33-114">EXAMPLES</span></span>

### <span data-ttu-id="e2d33-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2d33-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="e2d33-116">Testen Sie die route mit der Quelle "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="e2d33-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="e2d33-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2d33-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="e2d33-118">Testen Sie eine bestimmte Route.</span><span class="sxs-lookup"><span data-stu-id="e2d33-118">Test a specific route.</span></span>

### <span data-ttu-id="e2d33-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e2d33-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="e2d33-120">Testen Sie eine bestimmte Route, und zeigen Sie den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="e2d33-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="e2d33-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e2d33-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="e2d33-122">Testen Sie eine bestimmte Route mit "AppProperty" und "SystemProperty".</span><span class="sxs-lookup"><span data-stu-id="e2d33-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="e2d33-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2d33-123">PARAMETERS</span></span>

### <span data-ttu-id="e2d33-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="e2d33-124">-AppProperty</span></span>
<span data-ttu-id="e2d33-125">Eigenschaften der Route</span><span class="sxs-lookup"><span data-stu-id="e2d33-125">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-126">-Body</span><span class="sxs-lookup"><span data-stu-id="e2d33-126">-Body</span></span>
<span data-ttu-id="e2d33-127">Textkörper der Routenachricht</span><span class="sxs-lookup"><span data-stu-id="e2d33-127">Body of the route message</span></span>

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

### <span data-ttu-id="e2d33-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d33-128">-DefaultProfile</span></span>
<span data-ttu-id="e2d33-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2d33-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2d33-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2d33-130">-InputObject</span></span>
<span data-ttu-id="e2d33-131">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e2d33-131">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e2d33-132">-Name</span></span>
<span data-ttu-id="e2d33-133">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="e2d33-133">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d33-134">-ResourceGroupName</span></span>
<span data-ttu-id="e2d33-135">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e2d33-135">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2d33-136">-ResourceId</span></span>
<span data-ttu-id="e2d33-137">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e2d33-137">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e2d33-138">-RouteName</span></span>
<span data-ttu-id="e2d33-139">Name der Route</span><span class="sxs-lookup"><span data-stu-id="e2d33-139">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="e2d33-140">-ShowError</span></span>
<span data-ttu-id="e2d33-141">Detaillierter Fehler anzeigen (falls vorhanden)</span><span class="sxs-lookup"><span data-stu-id="e2d33-141">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-142">-Source</span><span class="sxs-lookup"><span data-stu-id="e2d33-142">-Source</span></span>
<span data-ttu-id="e2d33-143">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="e2d33-143">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="e2d33-144">-SystemProperty</span></span>
<span data-ttu-id="e2d33-145">Systemeigenschaften der Routenmeldung</span><span class="sxs-lookup"><span data-stu-id="e2d33-145">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d33-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d33-146">CommonParameters</span></span>
<span data-ttu-id="e2d33-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d33-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d33-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d33-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d33-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2d33-149">INPUTS</span></span>

### <span data-ttu-id="e2d33-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2d33-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e2d33-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e2d33-151">System.String</span></span>

## <span data-ttu-id="e2d33-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2d33-152">OUTPUTS</span></span>

### <span data-ttu-id="e2d33-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="e2d33-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="e2d33-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="e2d33-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="e2d33-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="e2d33-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="e2d33-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e2d33-156">NOTES</span></span>

## <span data-ttu-id="e2d33-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e2d33-157">RELATED LINKS</span></span>
