---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: c0599f599770467c3528cff902d2d60434c335e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849203"
---
# <span data-ttu-id="2eccd-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2eccd-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2eccd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2eccd-102">SYNOPSIS</span></span>
<span data-ttu-id="2eccd-103">Ruft eine Verbindung mit einem virtuellen Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="2eccd-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eccd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eccd-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eccd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2eccd-105">DESCRIPTION</span></span>
<span data-ttu-id="2eccd-106">Die VPN-Gatewayverbindung ist das Objekt, das den IPSec-Tunnel (Site-to-Site oder vnet-to-vnet) darstellt, der mit dem virtuellen Netzwerkgateway in Azure verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="2eccd-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="2eccd-107">Das Cmdlet " **Get-AzureRmVirtualNetworkGatewayConnection** " gibt das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="2eccd-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="2eccd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2eccd-108">EXAMPLES</span></span>

### <span data-ttu-id="2eccd-109">1: Abrufen einer virtuellen Netzwerk Gateway-Verbindung</span><span class="sxs-lookup"><span data-stu-id="2eccd-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="2eccd-110">Gibt das Objekt der virtuellen Netzwerk Gateway-Verbindung mit dem Namen "mytunnel" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="2eccd-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="2eccd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eccd-111">PARAMETERS</span></span>

### <span data-ttu-id="2eccd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eccd-112">-DefaultProfile</span></span>
<span data-ttu-id="2eccd-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2eccd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eccd-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2eccd-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eccd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eccd-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2eccd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eccd-116">CommonParameters</span></span>
<span data-ttu-id="2eccd-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eccd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eccd-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eccd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eccd-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2eccd-119">INPUTS</span></span>

## <span data-ttu-id="2eccd-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2eccd-120">OUTPUTS</span></span>

### <span data-ttu-id="2eccd-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2eccd-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2eccd-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="2eccd-122">NOTES</span></span>

## <span data-ttu-id="2eccd-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2eccd-123">RELATED LINKS</span></span>

