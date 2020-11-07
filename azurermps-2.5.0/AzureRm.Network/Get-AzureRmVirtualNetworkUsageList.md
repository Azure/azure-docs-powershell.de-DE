---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
ms.openlocfilehash: 61717f314629259caca9329c2ef1a458aa9a0e0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848147"
---
# <span data-ttu-id="70b4a-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="70b4a-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="70b4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="70b4a-103">Ruft die aktuelle Nutzung des virtuellen Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="70b4a-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70b4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70b4a-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70b4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="70b4a-106">Das Cmdlet " **Get-AzureRmVirtualNetworkUsageList** " erhält pro Subnetz-Nutzung für das angegebene virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="70b4a-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="70b4a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70b4a-107">EXAMPLES</span></span>

### <span data-ttu-id="70b4a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70b4a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="70b4a-109">Ruft pro Subnetz aktuelle Nutzungswerte für usagetest virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="70b4a-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="70b4a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="70b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="70b4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b4a-111">-DefaultProfile</span></span>
<span data-ttu-id="70b4a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70b4a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70b4a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="70b4a-113">-Name</span></span>
<span data-ttu-id="70b4a-114">Gibt den Namen des virtuellen Netzwerks an, für das die Verwendungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="70b4a-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70b4a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70b4a-115">-ResourceGroupName</span></span>
<span data-ttu-id="70b4a-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk gehört.</span><span class="sxs-lookup"><span data-stu-id="70b4a-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70b4a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b4a-117">CommonParameters</span></span>
<span data-ttu-id="70b4a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b4a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b4a-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b4a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b4a-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70b4a-120">INPUTS</span></span>

### <span data-ttu-id="70b4a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="70b4a-121">System.String</span></span>

## <span data-ttu-id="70b4a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70b4a-122">OUTPUTS</span></span>

### <span data-ttu-id="70b4a-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="70b4a-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="70b4a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="70b4a-124">NOTES</span></span>

## <span data-ttu-id="70b4a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70b4a-125">RELATED LINKS</span></span>

