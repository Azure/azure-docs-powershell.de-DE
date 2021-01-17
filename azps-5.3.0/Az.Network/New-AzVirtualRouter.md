---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378985"
---
# <span data-ttu-id="6748a-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6748a-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="6748a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6748a-102">SYNOPSIS</span></span>
<span data-ttu-id="6748a-103">Erstellt ein Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="6748a-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="6748a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6748a-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6748a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6748a-105">DESCRIPTION</span></span>
<span data-ttu-id="6748a-106">Das **Cmdlet "New-AzVirtualRouter"** erstellt ein Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6748a-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="6748a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6748a-107">EXAMPLES</span></span>

### <span data-ttu-id="6748a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6748a-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="6748a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6748a-109">PARAMETERS</span></span>

### <span data-ttu-id="6748a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6748a-110">-AsJob</span></span>
<span data-ttu-id="6748a-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6748a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6748a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6748a-112">-DefaultProfile</span></span>
<span data-ttu-id="6748a-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6748a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6748a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6748a-114">-Force</span></span>
<span data-ttu-id="6748a-115">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="6748a-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6748a-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="6748a-116">-HostedSubnet</span></span>
<span data-ttu-id="6748a-117">Das Subnetz, in dem der virtuelle Router gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="6748a-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="6748a-118">-Location</span><span class="sxs-lookup"><span data-stu-id="6748a-118">-Location</span></span>
<span data-ttu-id="6748a-119">Der Speicherort.</span><span class="sxs-lookup"><span data-stu-id="6748a-119">The location.</span></span>

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

### <span data-ttu-id="6748a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6748a-120">-Name</span></span>
<span data-ttu-id="6748a-121">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="6748a-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="6748a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6748a-122">-ResourceGroupName</span></span>
<span data-ttu-id="6748a-123">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="6748a-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="6748a-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="6748a-124">-Tag</span></span>
<span data-ttu-id="6748a-125">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="6748a-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6748a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6748a-126">-Confirm</span></span>
<span data-ttu-id="6748a-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6748a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6748a-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6748a-128">-WhatIf</span></span>
<span data-ttu-id="6748a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6748a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6748a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6748a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6748a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6748a-131">CommonParameters</span></span>
<span data-ttu-id="6748a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6748a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6748a-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6748a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6748a-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6748a-134">INPUTS</span></span>

### <span data-ttu-id="6748a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6748a-135">System.String</span></span>

### <span data-ttu-id="6748a-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6748a-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6748a-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6748a-137">OUTPUTS</span></span>

### <span data-ttu-id="6748a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6748a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="6748a-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6748a-139">NOTES</span></span>

## <span data-ttu-id="6748a-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6748a-140">RELATED LINKS</span></span>
