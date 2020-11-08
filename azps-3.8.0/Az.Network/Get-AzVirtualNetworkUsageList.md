---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996068"
---
# <span data-ttu-id="20a24-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="20a24-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="20a24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20a24-102">SYNOPSIS</span></span>
<span data-ttu-id="20a24-103">Ruft die aktuelle Nutzung des virtuellen Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="20a24-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="20a24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20a24-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20a24-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a24-105">DESCRIPTION</span></span>
<span data-ttu-id="20a24-106">Das Cmdlet " **Get-AzVirtualNetworkUsageList** " erhält pro Subnetz-Nutzung für das angegebene virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="20a24-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="20a24-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20a24-107">EXAMPLES</span></span>

### <span data-ttu-id="20a24-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20a24-108">Example 1</span></span>
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

<span data-ttu-id="20a24-109">Ruft pro Subnetz aktuelle Nutzungswerte für usagetest virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="20a24-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="20a24-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a24-110">PARAMETERS</span></span>

### <span data-ttu-id="20a24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a24-111">-DefaultProfile</span></span>
<span data-ttu-id="20a24-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20a24-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20a24-113">-Name</span><span class="sxs-lookup"><span data-stu-id="20a24-113">-Name</span></span>
<span data-ttu-id="20a24-114">Gibt den Namen des virtuellen Netzwerks an, für das die Verwendungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20a24-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="20a24-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a24-115">-ResourceGroupName</span></span>
<span data-ttu-id="20a24-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="20a24-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="20a24-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a24-117">CommonParameters</span></span>
<span data-ttu-id="20a24-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a24-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a24-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a24-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a24-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20a24-120">INPUTS</span></span>

### <span data-ttu-id="20a24-121">System. String</span><span class="sxs-lookup"><span data-stu-id="20a24-121">System.String</span></span>

## <span data-ttu-id="20a24-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20a24-122">OUTPUTS</span></span>

### <span data-ttu-id="20a24-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="20a24-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="20a24-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="20a24-124">NOTES</span></span>

## <span data-ttu-id="20a24-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20a24-125">RELATED LINKS</span></span>
