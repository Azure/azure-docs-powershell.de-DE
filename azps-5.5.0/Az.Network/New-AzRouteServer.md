---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 15a613f4d2c695fe42df5b02012187bdeee615b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146857"
---
# <span data-ttu-id="c51b4-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="c51b4-101">New-AzRouteServer</span></span>

## <span data-ttu-id="c51b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c51b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c51b4-103">Erstellt einen Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="c51b4-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="c51b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c51b4-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c51b4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c51b4-105">DESCRIPTION</span></span>
<span data-ttu-id="c51b4-106">Das **Cmdlet "New-AzRouteServer"** erstellt einen Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="c51b4-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="c51b4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c51b4-107">EXAMPLES</span></span>

### <span data-ttu-id="c51b4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c51b4-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="c51b4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c51b4-109">PARAMETERS</span></span>

### <span data-ttu-id="c51b4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c51b4-110">-AsJob</span></span>
<span data-ttu-id="c51b4-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c51b4-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c51b4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51b4-112">-DefaultProfile</span></span>
<span data-ttu-id="c51b4-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c51b4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c51b4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c51b4-114">-Force</span></span>
<span data-ttu-id="c51b4-115">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="c51b4-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c51b4-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="c51b4-116">-HostedSubnet</span></span>
<span data-ttu-id="c51b4-117">Das Subnetz, in dem der Routenserver gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c51b4-117">The subnet where the route server is hosted.</span></span>

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

### <span data-ttu-id="c51b4-118">-Location</span><span class="sxs-lookup"><span data-stu-id="c51b4-118">-Location</span></span>
<span data-ttu-id="c51b4-119">Der Ort.</span><span class="sxs-lookup"><span data-stu-id="c51b4-119">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c51b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="c51b4-121">Der Ressourcengruppenname des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="c51b4-121">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51b4-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="c51b4-122">-RouteServerName</span></span>
<span data-ttu-id="c51b4-123">Der Name des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="c51b4-123">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51b4-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="c51b4-124">-Tag</span></span>
<span data-ttu-id="c51b4-125">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="c51b4-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51b4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c51b4-126">-Confirm</span></span>
<span data-ttu-id="c51b4-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c51b4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c51b4-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c51b4-128">-WhatIf</span></span>
<span data-ttu-id="c51b4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c51b4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c51b4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c51b4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c51b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51b4-131">CommonParameters</span></span>
<span data-ttu-id="c51b4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c51b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51b4-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c51b4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51b4-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c51b4-134">INPUTS</span></span>

### <span data-ttu-id="c51b4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c51b4-135">System.String</span></span>

### <span data-ttu-id="c51b4-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c51b4-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c51b4-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c51b4-137">OUTPUTS</span></span>

### <span data-ttu-id="c51b4-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="c51b4-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="c51b4-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c51b4-139">NOTES</span></span>

## <span data-ttu-id="c51b4-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c51b4-140">RELATED LINKS</span></span>
