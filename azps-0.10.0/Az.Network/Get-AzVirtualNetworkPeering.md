---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841480"
---
# <span data-ttu-id="60c67-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="60c67-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="60c67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60c67-102">SYNOPSIS</span></span>
<span data-ttu-id="60c67-103">Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="60c67-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="60c67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60c67-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60c67-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60c67-105">DESCRIPTION</span></span>
<span data-ttu-id="60c67-106">Das Cmdlet " **Get-AzVirtualNetworkPeering** " Ruft das virtuelle Netzwerk Peering ab.</span><span class="sxs-lookup"><span data-stu-id="60c67-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="60c67-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60c67-107">EXAMPLES</span></span>

### <span data-ttu-id="60c67-108">Beispiel 1: Abrufen eines Peers zwischen zwei virtuellen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="60c67-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="60c67-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="60c67-109">PARAMETERS</span></span>

### <span data-ttu-id="60c67-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c67-110">-DefaultProfile</span></span>
<span data-ttu-id="60c67-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60c67-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60c67-112">-Name</span><span class="sxs-lookup"><span data-stu-id="60c67-112">-Name</span></span>
<span data-ttu-id="60c67-113">Gibt den Namen des virtuellen Netzwerk Peering an.</span><span class="sxs-lookup"><span data-stu-id="60c67-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="60c67-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c67-114">-ResourceGroupName</span></span>
<span data-ttu-id="60c67-115">Gibt den Namen der Ressourcengruppe an, zu der das virtuelle Netzwerk Peering gehört.</span><span class="sxs-lookup"><span data-stu-id="60c67-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="60c67-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="60c67-116">-VirtualNetworkName</span></span>
<span data-ttu-id="60c67-117">Gibt den virtuellen Netzwerknamen an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="60c67-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="60c67-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c67-118">CommonParameters</span></span>
<span data-ttu-id="60c67-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c67-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c67-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c67-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c67-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60c67-121">INPUTS</span></span>

## <span data-ttu-id="60c67-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60c67-122">OUTPUTS</span></span>

### <span data-ttu-id="60c67-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="60c67-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="60c67-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="60c67-124">NOTES</span></span>

## <span data-ttu-id="60c67-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60c67-125">RELATED LINKS</span></span>

[<span data-ttu-id="60c67-126">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="60c67-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="60c67-127">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="60c67-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="60c67-128">Satz-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="60c67-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


