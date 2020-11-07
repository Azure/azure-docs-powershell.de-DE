---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b4a6ae7db1221a2dee8a0bd5343ad78ed88a0abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662938"
---
# <span data-ttu-id="dd5b6-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dd5b6-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="dd5b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5b6-103">Ruft eine Verbindung mit einem virtuellen Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="dd5b6-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd5b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd5b6-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd5b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd5b6-105">DESCRIPTION</span></span>
<span data-ttu-id="dd5b6-106">Die VPN-Gatewayverbindung ist das Objekt, das den IPSec-Tunnel (Site-to-Site oder vnet-to-vnet) darstellt, der mit dem virtuellen Netzwerkgateway in Azure verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="dd5b6-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="dd5b6-107">Das Cmdlet " **Get-AzureRmVirtualNetworkGatewayConnection** " gibt das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="dd5b6-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="dd5b6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd5b6-108">EXAMPLES</span></span>

### <span data-ttu-id="dd5b6-109">1: Abrufen einer virtuellen Netzwerk Gateway-Verbindung</span><span class="sxs-lookup"><span data-stu-id="dd5b6-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="dd5b6-110">Gibt das Objekt der virtuellen Netzwerk Gateway-Verbindung mit dem Namen "mytunnel" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="dd5b6-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="dd5b6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd5b6-111">PARAMETERS</span></span>

### <span data-ttu-id="dd5b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5b6-112">-DefaultProfile</span></span>
<span data-ttu-id="dd5b6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd5b6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd5b6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="dd5b6-114">-Name</span></span>
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

### <span data-ttu-id="dd5b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5b6-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="dd5b6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5b6-116">CommonParameters</span></span>
<span data-ttu-id="dd5b6-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5b6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5b6-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5b6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5b6-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd5b6-119">INPUTS</span></span>

### <span data-ttu-id="dd5b6-120">Keine</span><span class="sxs-lookup"><span data-stu-id="dd5b6-120">None</span></span>
<span data-ttu-id="dd5b6-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="dd5b6-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd5b6-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd5b6-122">OUTPUTS</span></span>

### <span data-ttu-id="dd5b6-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dd5b6-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="dd5b6-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd5b6-124">NOTES</span></span>

## <span data-ttu-id="dd5b6-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd5b6-125">RELATED LINKS</span></span>

