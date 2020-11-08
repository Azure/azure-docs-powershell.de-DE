---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996081"
---
# <span data-ttu-id="670c2-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="670c2-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="670c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="670c2-102">SYNOPSIS</span></span>
<span data-ttu-id="670c2-103">Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="670c2-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="670c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="670c2-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="670c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="670c2-105">DESCRIPTION</span></span>
<span data-ttu-id="670c2-106">Das Cmdlet " **Get-AzVirtualNetworkPeering** " Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="670c2-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="670c2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="670c2-107">EXAMPLES</span></span>

### <span data-ttu-id="670c2-108">Beispiel 1: Abrufen eines Peers zwischen zwei virtuellen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="670c2-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="670c2-109">Beispiel 2: Abrufen aller Peerings im virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="670c2-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="670c2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="670c2-110">PARAMETERS</span></span>

### <span data-ttu-id="670c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670c2-111">-DefaultProfile</span></span>
<span data-ttu-id="670c2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="670c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="670c2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="670c2-113">-Name</span></span>
<span data-ttu-id="670c2-114">Gibt den Namen des virtuellen Netzwerk Peering an.</span><span class="sxs-lookup"><span data-stu-id="670c2-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="670c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="670c2-116">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk Peering gehört.</span><span class="sxs-lookup"><span data-stu-id="670c2-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="670c2-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="670c2-117">-VirtualNetworkName</span></span>
<span data-ttu-id="670c2-118">Gibt den virtuellen Netzwerknamen an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="670c2-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="670c2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670c2-119">CommonParameters</span></span>
<span data-ttu-id="670c2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670c2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670c2-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="670c2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670c2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="670c2-122">INPUTS</span></span>

### <span data-ttu-id="670c2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="670c2-123">System.String</span></span>

## <span data-ttu-id="670c2-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="670c2-124">OUTPUTS</span></span>

### <span data-ttu-id="670c2-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="670c2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="670c2-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="670c2-126">NOTES</span></span>

## <span data-ttu-id="670c2-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="670c2-127">RELATED LINKS</span></span>

[<span data-ttu-id="670c2-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="670c2-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="670c2-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="670c2-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="670c2-130">Satz-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="670c2-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
