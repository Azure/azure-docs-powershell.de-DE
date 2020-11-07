---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/test-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
ms.openlocfilehash: f51ba85215d252959b974a39ea864b1c98fce460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664587"
---
# <span data-ttu-id="42067-101">Test-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="42067-101">Test-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="42067-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42067-102">SYNOPSIS</span></span>
<span data-ttu-id="42067-103">Test Routen im viel Hub</span><span class="sxs-lookup"><span data-stu-id="42067-103">Test routes in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42067-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42067-104">SYNTAX</span></span>

### <span data-ttu-id="42067-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="42067-105">ResourceSet (Default)</span></span>
```
Test-AzureRmIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42067-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="42067-106">InputObjectTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42067-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="42067-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42067-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="42067-108">TestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42067-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="42067-109">TestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource>
 [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42067-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="42067-110">ResourceIdTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42067-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="42067-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42067-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42067-112">DESCRIPTION</span></span>
<span data-ttu-id="42067-113">Testen einer bestimmten Route</span><span class="sxs-lookup"><span data-stu-id="42067-113">Test a specific route.</span></span>

## <span data-ttu-id="42067-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42067-114">EXAMPLES</span></span>

### <span data-ttu-id="42067-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42067-115">Example 1</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="42067-116">Testen Sie alle Routen mit der Quelle "DeviceMessges".</span><span class="sxs-lookup"><span data-stu-id="42067-116">Test all route with source "DeviceMessges".</span></span>

### <span data-ttu-id="42067-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="42067-117">Example 2</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="42067-118">Testen einer bestimmten Route</span><span class="sxs-lookup"><span data-stu-id="42067-118">Test a specific route.</span></span>

### <span data-ttu-id="42067-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="42067-119">Example 3</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="42067-120">Testen Sie eine bestimmte Route, und zeigen Sie den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="42067-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="42067-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="42067-121">PARAMETERS</span></span>

### <span data-ttu-id="42067-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="42067-122">-AppProperty</span></span>
<span data-ttu-id="42067-123">App-Eigenschaften der Route-Nachricht</span><span class="sxs-lookup"><span data-stu-id="42067-123">App properties of the route message</span></span>

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

### <span data-ttu-id="42067-124">-Body</span><span class="sxs-lookup"><span data-stu-id="42067-124">-Body</span></span>
<span data-ttu-id="42067-125">Text der Routen Nachricht</span><span class="sxs-lookup"><span data-stu-id="42067-125">Body of the route message</span></span>

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

### <span data-ttu-id="42067-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42067-126">-DefaultProfile</span></span>
<span data-ttu-id="42067-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42067-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42067-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42067-128">-InputObject</span></span>
<span data-ttu-id="42067-129">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="42067-129">IotHub Object</span></span>

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

### <span data-ttu-id="42067-130">-Name</span><span class="sxs-lookup"><span data-stu-id="42067-130">-Name</span></span>
<span data-ttu-id="42067-131">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="42067-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="42067-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42067-132">-ResourceGroupName</span></span>
<span data-ttu-id="42067-133">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="42067-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="42067-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="42067-134">-ResourceId</span></span>
<span data-ttu-id="42067-135">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="42067-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="42067-136">-Routename</span><span class="sxs-lookup"><span data-stu-id="42067-136">-RouteName</span></span>
<span data-ttu-id="42067-137">Name der Route</span><span class="sxs-lookup"><span data-stu-id="42067-137">Name of the Route</span></span>

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

### <span data-ttu-id="42067-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="42067-138">-ShowError</span></span>
<span data-ttu-id="42067-139">Detaillierte Fehlermeldung anzeigen, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="42067-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="42067-140">-Source</span><span class="sxs-lookup"><span data-stu-id="42067-140">-Source</span></span>
<span data-ttu-id="42067-141">Quelle der Route</span><span class="sxs-lookup"><span data-stu-id="42067-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42067-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="42067-142">-SystemProperty</span></span>
<span data-ttu-id="42067-143">System Eigenschaften der Routing Nachricht</span><span class="sxs-lookup"><span data-stu-id="42067-143">System properties of the route message</span></span>

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

### <span data-ttu-id="42067-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42067-144">CommonParameters</span></span>
<span data-ttu-id="42067-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42067-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42067-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42067-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42067-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42067-147">INPUTS</span></span>

### <span data-ttu-id="42067-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="42067-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="42067-149">System. String</span><span class="sxs-lookup"><span data-stu-id="42067-149">System.String</span></span>

## <span data-ttu-id="42067-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42067-150">OUTPUTS</span></span>

### <span data-ttu-id="42067-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="42067-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>
<span data-ttu-id="42067-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. IotHub. Models. PSRouteProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="42067-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="42067-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="42067-153">NOTES</span></span>

## <span data-ttu-id="42067-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42067-154">RELATED LINKS</span></span>
