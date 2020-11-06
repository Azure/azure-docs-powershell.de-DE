---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 7ffe74795725e0751ed45dcc76864078ec372ac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497078"
---
# <span data-ttu-id="744f8-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744f8-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="744f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="744f8-102">SYNOPSIS</span></span>
<span data-ttu-id="744f8-103">Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="744f8-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="744f8-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="744f8-105">DESCRIPTION</span></span>
<span data-ttu-id="744f8-106">Das Cmdlet " **Get-AzureRmVirtualNetworkPeering** " Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="744f8-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="744f8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="744f8-107">EXAMPLES</span></span>

### <span data-ttu-id="744f8-108">Beispiel 1: Abrufen eines Peers zwischen zwei virtuellen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="744f8-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="744f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="744f8-109">PARAMETERS</span></span>

### <span data-ttu-id="744f8-110">-Name</span><span class="sxs-lookup"><span data-stu-id="744f8-110">-Name</span></span>
<span data-ttu-id="744f8-111">Gibt den Namen des virtuellen Netzwerk Peering an.</span><span class="sxs-lookup"><span data-stu-id="744f8-111">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744f8-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744f8-112">-ResourceGroupName</span></span>
<span data-ttu-id="744f8-113">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk Peering gehört.</span><span class="sxs-lookup"><span data-stu-id="744f8-113">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="744f8-114">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="744f8-114">-VirtualNetworkName</span></span>
<span data-ttu-id="744f8-115">Gibt den virtuellen Netzwerknamen an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="744f8-115">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="744f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744f8-116">-DefaultProfile</span></span>
<span data-ttu-id="744f8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="744f8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744f8-118">CommonParameters</span></span>
<span data-ttu-id="744f8-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744f8-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744f8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744f8-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="744f8-121">INPUTS</span></span>

## <span data-ttu-id="744f8-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="744f8-122">OUTPUTS</span></span>

### <span data-ttu-id="744f8-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744f8-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="744f8-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="744f8-124">NOTES</span></span>

## <span data-ttu-id="744f8-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="744f8-125">RELATED LINKS</span></span>

[<span data-ttu-id="744f8-126">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744f8-126">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="744f8-127">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744f8-127">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="744f8-128">Satz-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744f8-128">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


