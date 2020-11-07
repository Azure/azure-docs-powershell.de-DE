---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 1cc1bb46909260bd23cfa3f72e675251a011072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819752"
---
# <span data-ttu-id="f23ab-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="f23ab-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="f23ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f23ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f23ab-103">Abrufen von Informationen über die Route in "viel Hub"</span><span class="sxs-lookup"><span data-stu-id="f23ab-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="f23ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f23ab-104">SYNTAX</span></span>

### <span data-ttu-id="f23ab-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f23ab-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f23ab-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f23ab-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f23ab-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f23ab-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f23ab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f23ab-108">DESCRIPTION</span></span>
<span data-ttu-id="f23ab-109">Informieren Sie sich über die Route. Sie können alle Routen von einem viel Hub abrufen, Routen zu einem Endpunkttyp abrufen oder Routen zu einem bestimmten Endpunkt abrufen.</span><span class="sxs-lookup"><span data-stu-id="f23ab-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="f23ab-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f23ab-110">EXAMPLES</span></span>

### <span data-ttu-id="f23ab-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f23ab-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="f23ab-112">Holen Sie sich alle Route von "myiothub" viel Hub.</span><span class="sxs-lookup"><span data-stu-id="f23ab-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="f23ab-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f23ab-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="f23ab-114">Routeninformationen finden Sie im "myiothub"-Hub.</span><span class="sxs-lookup"><span data-stu-id="f23ab-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="f23ab-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f23ab-115">PARAMETERS</span></span>

### <span data-ttu-id="f23ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23ab-116">-DefaultProfile</span></span>
<span data-ttu-id="f23ab-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f23ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f23ab-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f23ab-118">-InputObject</span></span>
<span data-ttu-id="f23ab-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="f23ab-119">IotHub Object</span></span>

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

### <span data-ttu-id="f23ab-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f23ab-120">-Name</span></span>
<span data-ttu-id="f23ab-121">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="f23ab-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f23ab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23ab-122">-ResourceGroupName</span></span>
<span data-ttu-id="f23ab-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f23ab-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f23ab-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f23ab-124">-ResourceId</span></span>
<span data-ttu-id="f23ab-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f23ab-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f23ab-126">-Routename</span><span class="sxs-lookup"><span data-stu-id="f23ab-126">-RouteName</span></span>
<span data-ttu-id="f23ab-127">Name der Route</span><span class="sxs-lookup"><span data-stu-id="f23ab-127">Name of the Route</span></span>

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

### <span data-ttu-id="f23ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23ab-128">CommonParameters</span></span>
<span data-ttu-id="f23ab-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f23ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23ab-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23ab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23ab-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f23ab-131">INPUTS</span></span>

### <span data-ttu-id="f23ab-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f23ab-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f23ab-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f23ab-133">System.String</span></span>

## <span data-ttu-id="f23ab-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f23ab-134">OUTPUTS</span></span>

### <span data-ttu-id="f23ab-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="f23ab-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="f23ab-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="f23ab-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="f23ab-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f23ab-137">NOTES</span></span>

## <span data-ttu-id="f23ab-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f23ab-138">RELATED LINKS</span></span>
