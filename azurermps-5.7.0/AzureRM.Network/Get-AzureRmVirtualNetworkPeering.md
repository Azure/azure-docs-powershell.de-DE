---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 0c68886906957204ee0885a00bfc07740fb6ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662838"
---
# <span data-ttu-id="93344-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="93344-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="93344-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93344-102">SYNOPSIS</span></span>
<span data-ttu-id="93344-103">Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="93344-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93344-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93344-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93344-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93344-105">DESCRIPTION</span></span>
<span data-ttu-id="93344-106">Das Cmdlet " **Get-AzureRmVirtualNetworkPeering** " Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="93344-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="93344-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93344-107">EXAMPLES</span></span>

### <span data-ttu-id="93344-108">Beispiel 1: Abrufen eines Peers zwischen zwei virtuellen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="93344-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="93344-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="93344-109">PARAMETERS</span></span>

### <span data-ttu-id="93344-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93344-110">-DefaultProfile</span></span>
<span data-ttu-id="93344-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93344-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93344-112">-Name</span><span class="sxs-lookup"><span data-stu-id="93344-112">-Name</span></span>
<span data-ttu-id="93344-113">Gibt den Namen des virtuellen Netzwerk Peering an.</span><span class="sxs-lookup"><span data-stu-id="93344-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93344-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93344-114">-ResourceGroupName</span></span>
<span data-ttu-id="93344-115">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk Peering gehört.</span><span class="sxs-lookup"><span data-stu-id="93344-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="93344-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="93344-116">-VirtualNetworkName</span></span>
<span data-ttu-id="93344-117">Gibt den virtuellen Netzwerknamen an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="93344-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="93344-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93344-118">CommonParameters</span></span>
<span data-ttu-id="93344-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93344-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93344-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93344-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93344-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93344-121">INPUTS</span></span>

### <span data-ttu-id="93344-122">Keine</span><span class="sxs-lookup"><span data-stu-id="93344-122">None</span></span>
<span data-ttu-id="93344-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="93344-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93344-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93344-124">OUTPUTS</span></span>

### <span data-ttu-id="93344-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="93344-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="93344-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="93344-126">NOTES</span></span>

## <span data-ttu-id="93344-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93344-127">RELATED LINKS</span></span>

[<span data-ttu-id="93344-128">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="93344-128">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="93344-129">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="93344-129">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="93344-130">Satz-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="93344-130">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


