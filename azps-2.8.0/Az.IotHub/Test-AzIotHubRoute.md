---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 1015b49a65011ba42c916fa6c077d68992b5330a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650930"
---
# <span data-ttu-id="ff2bd-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="ff2bd-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="ff2bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2bd-103">Test Routen im viel Hub</span><span class="sxs-lookup"><span data-stu-id="ff2bd-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="ff2bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff2bd-104">SYNTAX</span></span>

### <span data-ttu-id="ff2bd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff2bd-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff2bd-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="ff2bd-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff2bd-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="ff2bd-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff2bd-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="ff2bd-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff2bd-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="ff2bd-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff2bd-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="ff2bd-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff2bd-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="ff2bd-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff2bd-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff2bd-112">DESCRIPTION</span></span>
<span data-ttu-id="ff2bd-113">Testen einer bestimmten Route</span><span class="sxs-lookup"><span data-stu-id="ff2bd-113">Test a specific route.</span></span>

## <span data-ttu-id="ff2bd-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff2bd-114">EXAMPLES</span></span>

### <span data-ttu-id="ff2bd-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff2bd-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="ff2bd-116">Testen Sie alle Routen mit der Quelle "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="ff2bd-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="ff2bd-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ff2bd-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="ff2bd-118">Testen einer bestimmten Route</span><span class="sxs-lookup"><span data-stu-id="ff2bd-118">Test a specific route.</span></span>

### <span data-ttu-id="ff2bd-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ff2bd-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="ff2bd-120">Testen Sie eine bestimmte Route, und zeigen Sie den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="ff2bd-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff2bd-121">PARAMETERS</span></span>

### <span data-ttu-id="ff2bd-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="ff2bd-122">-AppProperty</span></span>
<span data-ttu-id="ff2bd-123">App-Eigenschaften der Route-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ff2bd-123">App properties of the route message</span></span>

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

### <span data-ttu-id="ff2bd-124">-Body</span><span class="sxs-lookup"><span data-stu-id="ff2bd-124">-Body</span></span>
<span data-ttu-id="ff2bd-125">Text der Routen Nachricht</span><span class="sxs-lookup"><span data-stu-id="ff2bd-125">Body of the route message</span></span>

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

### <span data-ttu-id="ff2bd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2bd-126">-DefaultProfile</span></span>
<span data-ttu-id="ff2bd-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff2bd-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ff2bd-128">-InputObject</span></span>
<span data-ttu-id="ff2bd-129">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="ff2bd-129">IotHub Object</span></span>

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

### <span data-ttu-id="ff2bd-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ff2bd-130">-Name</span></span>
<span data-ttu-id="ff2bd-131">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="ff2bd-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ff2bd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2bd-132">-ResourceGroupName</span></span>
<span data-ttu-id="ff2bd-133">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ff2bd-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ff2bd-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ff2bd-134">-ResourceId</span></span>
<span data-ttu-id="ff2bd-135">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ff2bd-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ff2bd-136">-Routename</span><span class="sxs-lookup"><span data-stu-id="ff2bd-136">-RouteName</span></span>
<span data-ttu-id="ff2bd-137">Name der Route</span><span class="sxs-lookup"><span data-stu-id="ff2bd-137">Name of the Route</span></span>

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

### <span data-ttu-id="ff2bd-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="ff2bd-138">-ShowError</span></span>
<span data-ttu-id="ff2bd-139">Detaillierte Fehlermeldung anzeigen, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="ff2bd-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="ff2bd-140">-Source</span><span class="sxs-lookup"><span data-stu-id="ff2bd-140">-Source</span></span>
<span data-ttu-id="ff2bd-141">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="ff2bd-141">Source of the route</span></span>

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

### <span data-ttu-id="ff2bd-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="ff2bd-142">-SystemProperty</span></span>
<span data-ttu-id="ff2bd-143">System Eigenschaften der Routing Nachricht</span><span class="sxs-lookup"><span data-stu-id="ff2bd-143">System properties of the route message</span></span>

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

### <span data-ttu-id="ff2bd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2bd-144">CommonParameters</span></span>
<span data-ttu-id="ff2bd-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2bd-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2bd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2bd-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff2bd-147">INPUTS</span></span>

### <span data-ttu-id="ff2bd-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ff2bd-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ff2bd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ff2bd-149">System.String</span></span>

## <span data-ttu-id="ff2bd-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff2bd-150">OUTPUTS</span></span>

### <span data-ttu-id="ff2bd-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="ff2bd-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="ff2bd-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="ff2bd-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="ff2bd-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="ff2bd-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="ff2bd-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff2bd-154">NOTES</span></span>

## <span data-ttu-id="ff2bd-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff2bd-155">RELATED LINKS</span></span>
