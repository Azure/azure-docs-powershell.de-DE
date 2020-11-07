---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841492"
---
# <span data-ttu-id="d8309-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d8309-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d8309-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8309-102">SYNOPSIS</span></span>
<span data-ttu-id="d8309-103">Ruft eine Verbindung mit einem virtuellen Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="d8309-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="d8309-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8309-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8309-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8309-105">DESCRIPTION</span></span>
<span data-ttu-id="d8309-106">Die VPN-Gatewayverbindung ist das Objekt, das den IPSec-Tunnel (Site-to-Site oder vnet-to-vnet) darstellt, der mit dem virtuellen Netzwerkgateway in Azure verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d8309-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="d8309-107">Das Cmdlet " **Get-AzVirtualNetworkGatewayConnection** " gibt das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="d8309-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d8309-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8309-108">EXAMPLES</span></span>

### <span data-ttu-id="d8309-109">1: Abrufen einer virtuellen Netzwerk Gateway-Verbindung</span><span class="sxs-lookup"><span data-stu-id="d8309-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="d8309-110">Gibt das Objekt der virtuellen Netzwerk Gateway-Verbindung mit dem Namen "mytunnel" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="d8309-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="d8309-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8309-111">PARAMETERS</span></span>

### <span data-ttu-id="d8309-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8309-112">-DefaultProfile</span></span>
<span data-ttu-id="d8309-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8309-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8309-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d8309-114">-Name</span></span>
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

### <span data-ttu-id="d8309-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8309-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d8309-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8309-116">CommonParameters</span></span>
<span data-ttu-id="d8309-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8309-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8309-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8309-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8309-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8309-119">INPUTS</span></span>

## <span data-ttu-id="d8309-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8309-120">OUTPUTS</span></span>

### <span data-ttu-id="d8309-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d8309-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d8309-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8309-122">NOTES</span></span>

## <span data-ttu-id="d8309-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8309-123">RELATED LINKS</span></span>

