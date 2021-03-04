---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: f0fc298ba92b7e9dc0f0bf5ed4f8cbdba5b8091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920787"
---
# <span data-ttu-id="520d5-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="520d5-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="520d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="520d5-102">SYNOPSIS</span></span>
<span data-ttu-id="520d5-103">Erstellen oder Aktualisieren eines Netzwerkregelsatzs</span><span class="sxs-lookup"><span data-stu-id="520d5-103">Create or update a network rule set.</span></span> <span data-ttu-id="520d5-104">Regelsatz kann nur auf die "Premium"-Registrierung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="520d5-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="520d5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="520d5-105">SYNTAX</span></span>

### <span data-ttu-id="520d5-106">AddAddNetworkRuleWithoutInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="520d5-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="520d5-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="520d5-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="520d5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="520d5-108">DESCRIPTION</span></span>
<span data-ttu-id="520d5-109">Erstellen oder Aktualisieren eines Netzwerkregelsatzs</span><span class="sxs-lookup"><span data-stu-id="520d5-109">Create or update a network rule set</span></span>

## <span data-ttu-id="520d5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="520d5-110">EXAMPLES</span></span>

### <span data-ttu-id="520d5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="520d5-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="520d5-112">Erstellen Sie einen neuen Netzwerkregelsatz.</span><span class="sxs-lookup"><span data-stu-id="520d5-112">Create a new network rule set.</span></span>

## <span data-ttu-id="520d5-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="520d5-113">PARAMETERS</span></span>

### <span data-ttu-id="520d5-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="520d5-114">-DefaultAction</span></span>
<span data-ttu-id="520d5-115">Die Standardaktion könnte "Zulassen" oder "Verweigern" sein.</span><span class="sxs-lookup"><span data-stu-id="520d5-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520d5-116">-DefaultProfile</span></span>
<span data-ttu-id="520d5-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="520d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="520d5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="520d5-118">-InputObject</span></span>
<span data-ttu-id="520d5-119">Eingabe PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="520d5-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d5-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="520d5-120">-NetworkRule</span></span>
<span data-ttu-id="520d5-121">Liste der Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="520d5-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520d5-122">CommonParameters</span></span>
<span data-ttu-id="520d5-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="520d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520d5-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="520d5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520d5-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="520d5-125">INPUTS</span></span>

### <span data-ttu-id="520d5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="520d5-126">System.String</span></span>

### <span data-ttu-id="520d5-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="520d5-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="520d5-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="520d5-128">OUTPUTS</span></span>

### <span data-ttu-id="520d5-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="520d5-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="520d5-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="520d5-130">NOTES</span></span>

## <span data-ttu-id="520d5-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="520d5-131">RELATED LINKS</span></span>
