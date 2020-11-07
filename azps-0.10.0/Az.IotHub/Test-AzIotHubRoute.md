---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 3d5252f30d8d4393d84f77e1ae1076c9c8054d91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843916"
---
# <span data-ttu-id="009f2-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="009f2-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="009f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="009f2-102">SYNOPSIS</span></span>
<span data-ttu-id="009f2-103">Test Routen im viel Hub</span><span class="sxs-lookup"><span data-stu-id="009f2-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="009f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="009f2-104">SYNTAX</span></span>

### <span data-ttu-id="009f2-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="009f2-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="009f2-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="009f2-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="009f2-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="009f2-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="009f2-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="009f2-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="009f2-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="009f2-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="009f2-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="009f2-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="009f2-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="009f2-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="009f2-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="009f2-112">DESCRIPTION</span></span>
<span data-ttu-id="009f2-113">Testen einer bestimmten Route</span><span class="sxs-lookup"><span data-stu-id="009f2-113">Test a specific route.</span></span>

## <span data-ttu-id="009f2-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="009f2-114">EXAMPLES</span></span>

### <span data-ttu-id="009f2-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="009f2-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="009f2-116">Testen Sie alle Routen mit der Quelle "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="009f2-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="009f2-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="009f2-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="009f2-118">Testen einer bestimmten Route</span><span class="sxs-lookup"><span data-stu-id="009f2-118">Test a specific route.</span></span>

### <span data-ttu-id="009f2-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="009f2-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="009f2-120">Testen Sie eine bestimmte Route, und zeigen Sie den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="009f2-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="009f2-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="009f2-121">PARAMETERS</span></span>

### <span data-ttu-id="009f2-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="009f2-122">-AppProperty</span></span>
<span data-ttu-id="009f2-123">App-Eigenschaften der Route-Nachricht</span><span class="sxs-lookup"><span data-stu-id="009f2-123">App properties of the route message</span></span>

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

### <span data-ttu-id="009f2-124">-Body</span><span class="sxs-lookup"><span data-stu-id="009f2-124">-Body</span></span>
<span data-ttu-id="009f2-125">Text der Routen Nachricht</span><span class="sxs-lookup"><span data-stu-id="009f2-125">Body of the route message</span></span>

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

### <span data-ttu-id="009f2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="009f2-126">-DefaultProfile</span></span>
<span data-ttu-id="009f2-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="009f2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="009f2-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="009f2-128">-InputObject</span></span>
<span data-ttu-id="009f2-129">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="009f2-129">IotHub Object</span></span>

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

### <span data-ttu-id="009f2-130">-Name</span><span class="sxs-lookup"><span data-stu-id="009f2-130">-Name</span></span>
<span data-ttu-id="009f2-131">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="009f2-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="009f2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="009f2-132">-ResourceGroupName</span></span>
<span data-ttu-id="009f2-133">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="009f2-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="009f2-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="009f2-134">-ResourceId</span></span>
<span data-ttu-id="009f2-135">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="009f2-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="009f2-136">-Routename</span><span class="sxs-lookup"><span data-stu-id="009f2-136">-RouteName</span></span>
<span data-ttu-id="009f2-137">Name der Route</span><span class="sxs-lookup"><span data-stu-id="009f2-137">Name of the Route</span></span>

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

### <span data-ttu-id="009f2-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="009f2-138">-ShowError</span></span>
<span data-ttu-id="009f2-139">Detaillierte Fehlermeldung anzeigen, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="009f2-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="009f2-140">-Source</span><span class="sxs-lookup"><span data-stu-id="009f2-140">-Source</span></span>
<span data-ttu-id="009f2-141">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="009f2-141">Source of the route</span></span>

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

### <span data-ttu-id="009f2-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="009f2-142">-SystemProperty</span></span>
<span data-ttu-id="009f2-143">System Eigenschaften der Routing Nachricht</span><span class="sxs-lookup"><span data-stu-id="009f2-143">System properties of the route message</span></span>

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

### <span data-ttu-id="009f2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="009f2-144">CommonParameters</span></span>
<span data-ttu-id="009f2-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="009f2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="009f2-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="009f2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="009f2-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="009f2-147">INPUTS</span></span>

### <span data-ttu-id="009f2-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="009f2-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="009f2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="009f2-149">System.String</span></span>

## <span data-ttu-id="009f2-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="009f2-150">OUTPUTS</span></span>

### <span data-ttu-id="009f2-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="009f2-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="009f2-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="009f2-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="009f2-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="009f2-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="009f2-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="009f2-154">NOTES</span></span>

## <span data-ttu-id="009f2-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="009f2-155">RELATED LINKS</span></span>
