---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175784"
---
# <span data-ttu-id="4e6e1-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e6e1-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="4e6e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6e1-103">Erstellen oder Aktualisieren eines Netzwerkregel Satzes</span><span class="sxs-lookup"><span data-stu-id="4e6e1-103">Create or update a network rule set.</span></span> <span data-ttu-id="4e6e1-104">Der Regelsatz kann nur auf die "Premium"-Registrierung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e6e1-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="4e6e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e6e1-105">SYNTAX</span></span>

### <span data-ttu-id="4e6e1-106">AddAddNetworkRuleWithoutInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e6e1-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6e1-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="4e6e1-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e6e1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e6e1-108">DESCRIPTION</span></span>
<span data-ttu-id="4e6e1-109">Erstellen oder Aktualisieren eines Netzwerkregel Satzes</span><span class="sxs-lookup"><span data-stu-id="4e6e1-109">Create or update a network rule set</span></span>

## <span data-ttu-id="4e6e1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e6e1-110">EXAMPLES</span></span>

### <span data-ttu-id="4e6e1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e6e1-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="4e6e1-112">Erstellen eines neuen Netzwerkregel Satzes</span><span class="sxs-lookup"><span data-stu-id="4e6e1-112">Create a new network rule set.</span></span>

## <span data-ttu-id="4e6e1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e6e1-113">PARAMETERS</span></span>

### <span data-ttu-id="4e6e1-114">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="4e6e1-114">-DefaultAction</span></span>
<span data-ttu-id="4e6e1-115">Standardaktion: "zulassen" oder "ablehnen"</span><span class="sxs-lookup"><span data-stu-id="4e6e1-115">Default action, could be 'Allow' or 'Deny'</span></span>

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

### <span data-ttu-id="4e6e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6e1-116">-DefaultProfile</span></span>
<span data-ttu-id="4e6e1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e6e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e6e1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e6e1-118">-InputObject</span></span>
<span data-ttu-id="4e6e1-119">Eingabe PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e6e1-119">Input PSNetworkRuleSet</span></span>

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

### <span data-ttu-id="4e6e1-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="4e6e1-120">-NetworkRule</span></span>
<span data-ttu-id="4e6e1-121">Liste der Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="4e6e1-121">List of Network rules</span></span>

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

### <span data-ttu-id="4e6e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6e1-122">CommonParameters</span></span>
<span data-ttu-id="4e6e1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6e1-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e6e1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6e1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e6e1-125">INPUTS</span></span>

### <span data-ttu-id="4e6e1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4e6e1-126">System.String</span></span>

### <span data-ttu-id="4e6e1-127">Microsoft. Azure. Commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4e6e1-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="4e6e1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e6e1-128">OUTPUTS</span></span>

### <span data-ttu-id="4e6e1-129">Microsoft. Azure. Commands. ContainerRegistry. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e6e1-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="4e6e1-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e6e1-130">NOTES</span></span>

## <span data-ttu-id="4e6e1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e6e1-131">RELATED LINKS</span></span>
