---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170502"
---
# <span data-ttu-id="e8034-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e8034-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="e8034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8034-102">SYNOPSIS</span></span>
<span data-ttu-id="e8034-103">Informationen zur Route in IoT Hub</span><span class="sxs-lookup"><span data-stu-id="e8034-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="e8034-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8034-104">SYNTAX</span></span>

### <span data-ttu-id="e8034-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8034-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8034-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e8034-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8034-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e8034-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8034-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8034-108">DESCRIPTION</span></span>
<span data-ttu-id="e8034-109">Hier erhalten Sie Informationen zur Route. Sie können alle Routen von einem IoT Hub, Routen zu einem Endpunkttyp oder Routen zu einem bestimmten Endpunkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="e8034-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="e8034-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8034-110">EXAMPLES</span></span>

### <span data-ttu-id="e8034-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8034-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="e8034-112">Holen Sie sich die route von "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e8034-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e8034-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e8034-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="e8034-114">Abrufen von Routeninformationen aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e8034-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="e8034-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8034-115">PARAMETERS</span></span>

### <span data-ttu-id="e8034-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8034-116">-DefaultProfile</span></span>
<span data-ttu-id="e8034-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8034-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8034-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8034-118">-InputObject</span></span>
<span data-ttu-id="e8034-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e8034-119">IotHub Object</span></span>

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

### <span data-ttu-id="e8034-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e8034-120">-Name</span></span>
<span data-ttu-id="e8034-121">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="e8034-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e8034-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8034-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8034-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e8034-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e8034-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8034-124">-ResourceId</span></span>
<span data-ttu-id="e8034-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e8034-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e8034-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e8034-126">-RouteName</span></span>
<span data-ttu-id="e8034-127">Name der Route</span><span class="sxs-lookup"><span data-stu-id="e8034-127">Name of the Route</span></span>

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

### <span data-ttu-id="e8034-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8034-128">CommonParameters</span></span>
<span data-ttu-id="e8034-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8034-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8034-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8034-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8034-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8034-131">INPUTS</span></span>

### <span data-ttu-id="e8034-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e8034-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e8034-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e8034-133">System.String</span></span>

## <span data-ttu-id="e8034-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8034-134">OUTPUTS</span></span>

### <span data-ttu-id="e8034-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="e8034-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="e8034-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="e8034-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="e8034-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e8034-137">NOTES</span></span>

## <span data-ttu-id="e8034-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e8034-138">RELATED LINKS</span></span>
