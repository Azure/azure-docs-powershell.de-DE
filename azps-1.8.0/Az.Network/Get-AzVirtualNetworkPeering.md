---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: e2b4625536124cdb5352c97564cd4c2792dadb96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660673"
---
# <span data-ttu-id="fc13a-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fc13a-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="fc13a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc13a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc13a-103">Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="fc13a-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="fc13a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc13a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc13a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc13a-105">DESCRIPTION</span></span>
<span data-ttu-id="fc13a-106">Das Cmdlet " **Get-AzVirtualNetworkPeering** " Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="fc13a-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="fc13a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc13a-107">EXAMPLES</span></span>

### <span data-ttu-id="fc13a-108">Beispiel 1: Abrufen eines Peers zwischen zwei virtuellen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="fc13a-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="fc13a-109">Beispiel 2: Abrufen aller Peerings im virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="fc13a-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="fc13a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc13a-110">PARAMETERS</span></span>

### <span data-ttu-id="fc13a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc13a-111">-DefaultProfile</span></span>
<span data-ttu-id="fc13a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc13a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc13a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fc13a-113">-Name</span></span>
<span data-ttu-id="fc13a-114">Gibt den Namen des virtuellen Netzwerk Peering an.</span><span class="sxs-lookup"><span data-stu-id="fc13a-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fc13a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc13a-115">-ResourceGroupName</span></span>
<span data-ttu-id="fc13a-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk Peering gehört.</span><span class="sxs-lookup"><span data-stu-id="fc13a-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="fc13a-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fc13a-117">-VirtualNetworkName</span></span>
<span data-ttu-id="fc13a-118">Gibt den virtuellen Netzwerknamen an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="fc13a-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fc13a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc13a-119">CommonParameters</span></span>
<span data-ttu-id="fc13a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc13a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc13a-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc13a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc13a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc13a-122">INPUTS</span></span>

### <span data-ttu-id="fc13a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fc13a-123">System.String</span></span>

## <span data-ttu-id="fc13a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc13a-124">OUTPUTS</span></span>

### <span data-ttu-id="fc13a-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fc13a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="fc13a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc13a-126">NOTES</span></span>

## <span data-ttu-id="fc13a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc13a-127">RELATED LINKS</span></span>

[<span data-ttu-id="fc13a-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fc13a-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="fc13a-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fc13a-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="fc13a-130">Satz-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fc13a-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
