---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: b4daa24f787633d2f18896910faed340a969a0f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942424"
---
# <span data-ttu-id="bba6e-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="bba6e-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="bba6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba6e-102">SYNOPSIS</span></span>
<span data-ttu-id="bba6e-103">Ruft die aktuelle Nutzung des virtuellen Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="bba6e-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="bba6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bba6e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba6e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bba6e-105">DESCRIPTION</span></span>
<span data-ttu-id="bba6e-106">Das **Get-AzVirtualNetworkUsageList-Cmdlet** ruft pro Subnetznutzung für das angegebene virtuelle Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="bba6e-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="bba6e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bba6e-107">EXAMPLES</span></span>

### <span data-ttu-id="bba6e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bba6e-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="bba6e-109">Ruft die aktuellen Nutzungswerte pro Subnetz für das nutzungsteste virtuelle Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="bba6e-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="bba6e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bba6e-110">PARAMETERS</span></span>

### <span data-ttu-id="bba6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba6e-111">-DefaultProfile</span></span>
<span data-ttu-id="bba6e-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bba6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bba6e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bba6e-113">-Name</span></span>
<span data-ttu-id="bba6e-114">Gibt den Namen des virtuellen Netzwerks an, für das Verwendungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bba6e-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="bba6e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba6e-115">-ResourceGroupName</span></span>
<span data-ttu-id="bba6e-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="bba6e-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="bba6e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba6e-117">CommonParameters</span></span>
<span data-ttu-id="bba6e-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba6e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba6e-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bba6e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba6e-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bba6e-120">INPUTS</span></span>

### <span data-ttu-id="bba6e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="bba6e-121">System.String</span></span>

## <span data-ttu-id="bba6e-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bba6e-122">OUTPUTS</span></span>

### <span data-ttu-id="bba6e-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="bba6e-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="bba6e-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bba6e-124">NOTES</span></span>

## <span data-ttu-id="bba6e-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bba6e-125">RELATED LINKS</span></span>
