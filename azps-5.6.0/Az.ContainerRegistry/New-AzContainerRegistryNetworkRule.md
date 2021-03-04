---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: 0fef46fb32c299a0d3117e8168e845777293d496
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924211"
---
# <span data-ttu-id="a7ed3-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a7ed3-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="a7ed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ed3-103">Erstellen Sie eine Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-103">Create a network rule.</span></span>

## <span data-ttu-id="a7ed3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7ed3-104">SYNTAX</span></span>

### <span data-ttu-id="a7ed3-105">ByVirtualNetworkRule (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7ed3-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7ed3-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="a7ed3-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7ed3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7ed3-107">DESCRIPTION</span></span>
<span data-ttu-id="a7ed3-108">Erstellen Sie ein Netzwerkregelobjekt in der aktuellen Powershellsitzung.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="a7ed3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7ed3-109">EXAMPLES</span></span>

### <span data-ttu-id="a7ed3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7ed3-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="a7ed3-111">Erstellen Sie virtualnetwork-Regelsatz.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="a7ed3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7ed3-112">PARAMETERS</span></span>

### <span data-ttu-id="a7ed3-113">-Aktion</span><span class="sxs-lookup"><span data-stu-id="a7ed3-113">-Action</span></span>
<span data-ttu-id="a7ed3-114">Die Aktion der Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-114">The action of network rule.</span></span>

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

### <span data-ttu-id="a7ed3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ed3-115">-DefaultProfile</span></span>
<span data-ttu-id="a7ed3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ed3-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a7ed3-117">-IPAddressOrRange</span></span>
<span data-ttu-id="a7ed3-118">Gibt den IP- oder IP-Bereich im CIDR-Format an.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="a7ed3-119">Nur die IPV4-Adresse ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ed3-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="a7ed3-120">-IPRule</span></span>
<span data-ttu-id="a7ed3-121">Geben Sie an, dass IPRule erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ed3-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a7ed3-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="a7ed3-123">Ressourcen-ID eines Subnetzes, z. B.: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ed3-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a7ed3-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="a7ed3-125">Geben Sie an, dass VirtualNetworkRule erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ed3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ed3-126">CommonParameters</span></span>
<span data-ttu-id="a7ed3-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ed3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ed3-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7ed3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ed3-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7ed3-129">INPUTS</span></span>

### <span data-ttu-id="a7ed3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a7ed3-130">System.String</span></span>

## <span data-ttu-id="a7ed3-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7ed3-131">OUTPUTS</span></span>

### <span data-ttu-id="a7ed3-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a7ed3-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="a7ed3-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7ed3-133">NOTES</span></span>

## <span data-ttu-id="a7ed3-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7ed3-134">RELATED LINKS</span></span>
