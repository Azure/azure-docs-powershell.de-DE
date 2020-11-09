---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296379"
---
# <span data-ttu-id="1677b-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1677b-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="1677b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1677b-102">SYNOPSIS</span></span>
<span data-ttu-id="1677b-103">Erstellen Sie eine Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="1677b-103">Create a network rule.</span></span>

## <span data-ttu-id="1677b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1677b-104">SYNTAX</span></span>

### <span data-ttu-id="1677b-105">ByVirtualNetworkRule (Standard)</span><span class="sxs-lookup"><span data-stu-id="1677b-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1677b-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="1677b-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1677b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1677b-107">DESCRIPTION</span></span>
<span data-ttu-id="1677b-108">Erstellen eines Netzwerkregel Objekts in der aktuellen PowerShell-Sitzung</span><span class="sxs-lookup"><span data-stu-id="1677b-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="1677b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1677b-109">EXAMPLES</span></span>

### <span data-ttu-id="1677b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1677b-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="1677b-111">Erstellen eines VirtualNetwork-Regelsatzes</span><span class="sxs-lookup"><span data-stu-id="1677b-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="1677b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1677b-112">PARAMETERS</span></span>

### <span data-ttu-id="1677b-113">– Aktion</span><span class="sxs-lookup"><span data-stu-id="1677b-113">-Action</span></span>
<span data-ttu-id="1677b-114">Die Aktion der Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="1677b-114">The action of network rule.</span></span>

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

### <span data-ttu-id="1677b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1677b-115">-DefaultProfile</span></span>
<span data-ttu-id="1677b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1677b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1677b-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1677b-117">-IPAddressOrRange</span></span>
<span data-ttu-id="1677b-118">Gibt den IP-oder IP-Bereich im CIDR-Format an.</span><span class="sxs-lookup"><span data-stu-id="1677b-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="1677b-119">Nur IPv4-Adresse ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1677b-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="1677b-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="1677b-120">-IPRule</span></span>
<span data-ttu-id="1677b-121">Geben Sie an, IPRule zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1677b-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="1677b-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="1677b-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1677b-123">Ressourcen-ID eines Subnets, beispielsweise:/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Network/virtualNetworks/{vnetName}/Subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="1677b-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="1677b-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1677b-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="1677b-125">Geben Sie an, VirtualNetworkRule zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1677b-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="1677b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1677b-126">CommonParameters</span></span>
<span data-ttu-id="1677b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1677b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1677b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1677b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1677b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1677b-129">INPUTS</span></span>

### <span data-ttu-id="1677b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1677b-130">System.String</span></span>

## <span data-ttu-id="1677b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1677b-131">OUTPUTS</span></span>

### <span data-ttu-id="1677b-132">Microsoft. Azure. Commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1677b-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="1677b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1677b-133">NOTES</span></span>

## <span data-ttu-id="1677b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1677b-134">RELATED LINKS</span></span>
