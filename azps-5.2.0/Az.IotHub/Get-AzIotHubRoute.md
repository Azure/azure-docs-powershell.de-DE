---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303176"
---
# <span data-ttu-id="b8da0-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="b8da0-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="b8da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8da0-102">SYNOPSIS</span></span>
<span data-ttu-id="b8da0-103">Informationen zur Route in IoT Hub</span><span class="sxs-lookup"><span data-stu-id="b8da0-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="b8da0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8da0-104">SYNTAX</span></span>

### <span data-ttu-id="b8da0-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8da0-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8da0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8da0-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8da0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8da0-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8da0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8da0-108">DESCRIPTION</span></span>
<span data-ttu-id="b8da0-109">Hier erhalten Sie Informationen zur Route. Sie können alle Routen von einem IoT Hub, Routen zu einem Endpunkttyp oder Routen zu einem bestimmten Endpunkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8da0-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="b8da0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8da0-110">EXAMPLES</span></span>

### <span data-ttu-id="b8da0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8da0-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="b8da0-112">Holen Sie sich die route von "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="b8da0-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="b8da0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b8da0-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="b8da0-114">Abrufen von Routeninformationen aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="b8da0-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b8da0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8da0-115">PARAMETERS</span></span>

### <span data-ttu-id="b8da0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8da0-116">-DefaultProfile</span></span>
<span data-ttu-id="b8da0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8da0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8da0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8da0-118">-InputObject</span></span>
<span data-ttu-id="b8da0-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b8da0-119">IotHub Object</span></span>

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

### <span data-ttu-id="b8da0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b8da0-120">-Name</span></span>
<span data-ttu-id="b8da0-121">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="b8da0-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b8da0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8da0-122">-ResourceGroupName</span></span>
<span data-ttu-id="b8da0-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b8da0-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b8da0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8da0-124">-ResourceId</span></span>
<span data-ttu-id="b8da0-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b8da0-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b8da0-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="b8da0-126">-RouteName</span></span>
<span data-ttu-id="b8da0-127">Name der Route</span><span class="sxs-lookup"><span data-stu-id="b8da0-127">Name of the Route</span></span>

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

### <span data-ttu-id="b8da0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8da0-128">CommonParameters</span></span>
<span data-ttu-id="b8da0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8da0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8da0-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8da0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8da0-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8da0-131">INPUTS</span></span>

### <span data-ttu-id="b8da0-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b8da0-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b8da0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b8da0-133">System.String</span></span>

## <span data-ttu-id="b8da0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8da0-134">OUTPUTS</span></span>

### <span data-ttu-id="b8da0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="b8da0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="b8da0-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="b8da0-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="b8da0-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8da0-137">NOTES</span></span>

## <span data-ttu-id="b8da0-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8da0-138">RELATED LINKS</span></span>
