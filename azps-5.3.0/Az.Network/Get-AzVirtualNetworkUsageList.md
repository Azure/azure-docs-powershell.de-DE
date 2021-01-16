---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379824"
---
# <span data-ttu-id="17831-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="17831-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="17831-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17831-102">SYNOPSIS</span></span>
<span data-ttu-id="17831-103">Ruft die aktuelle Nutzung des virtuellen Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="17831-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="17831-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17831-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17831-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17831-105">DESCRIPTION</span></span>
<span data-ttu-id="17831-106">Das **Cmdlet "Get-AzVirtualNetworkUsageList"** ruft pro Subnetznutzung für das angegebene virtuelle Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="17831-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="17831-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17831-107">EXAMPLES</span></span>

### <span data-ttu-id="17831-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17831-108">Example 1</span></span>
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

<span data-ttu-id="17831-109">Ruft aktuelle Nutzungswerte pro Subnetz für das virtuelle Nutzungstestnetzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="17831-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="17831-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17831-110">PARAMETERS</span></span>

### <span data-ttu-id="17831-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17831-111">-DefaultProfile</span></span>
<span data-ttu-id="17831-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17831-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17831-113">-Name</span><span class="sxs-lookup"><span data-stu-id="17831-113">-Name</span></span>
<span data-ttu-id="17831-114">Gibt den Namen des virtuellen Netzwerks an, für das Nutzungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="17831-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="17831-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17831-115">-ResourceGroupName</span></span>
<span data-ttu-id="17831-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="17831-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="17831-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17831-117">CommonParameters</span></span>
<span data-ttu-id="17831-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17831-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17831-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17831-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17831-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17831-120">INPUTS</span></span>

### <span data-ttu-id="17831-121">System.String</span><span class="sxs-lookup"><span data-stu-id="17831-121">System.String</span></span>

## <span data-ttu-id="17831-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17831-122">OUTPUTS</span></span>

### <span data-ttu-id="17831-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="17831-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="17831-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="17831-124">NOTES</span></span>

## <span data-ttu-id="17831-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="17831-125">RELATED LINKS</span></span>
