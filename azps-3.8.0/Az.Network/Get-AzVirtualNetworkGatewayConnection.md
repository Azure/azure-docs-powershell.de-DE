---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995381"
---
# <span data-ttu-id="52e1b-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="52e1b-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="52e1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="52e1b-103">Ruft eine Verbindung mit einem virtuellen Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="52e1b-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="52e1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52e1b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52e1b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="52e1b-106">Die VPN-Gatewayverbindung ist das Objekt, das den IPSec-Tunnel (Site-to-Site oder vnet-to-vnet) darstellt, der mit dem virtuellen Netzwerkgateway in Azure verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="52e1b-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="52e1b-107">Das Cmdlet " **Get-AzVirtualNetworkGatewayConnection** " gibt das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="52e1b-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="52e1b-108">Wenn das Cmdlet **Get-AzVirtualNetworkGatewayConnection** ohne Angabe des-Name-Parameters ausgegeben wird, werden in der Ausgabe keine Details zu ConnectionStatus und SharedKey angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52e1b-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="52e1b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52e1b-109">EXAMPLES</span></span>

### <span data-ttu-id="52e1b-110">1: Abrufen einer virtuellen Netzwerk Gateway-Verbindung</span><span class="sxs-lookup"><span data-stu-id="52e1b-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="52e1b-111">Gibt das Objekt der virtuellen Netzwerk Gateway-Verbindung mit dem Namen "mytunnel" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="52e1b-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="52e1b-112">2: Abrufen aller virtuellen Netzwerk-Gateway-Verbindungen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="52e1b-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="52e1b-113">Gibt alle virtuellen Netzwerk-Gateway-Verbindungen zurück, die mit "mytunnel" in der Ressourcengruppe "myRG" beginnen.</span><span class="sxs-lookup"><span data-stu-id="52e1b-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="52e1b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="52e1b-114">PARAMETERS</span></span>

### <span data-ttu-id="52e1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e1b-115">-DefaultProfile</span></span>
<span data-ttu-id="52e1b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52e1b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52e1b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="52e1b-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="52e1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e1b-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="52e1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e1b-119">CommonParameters</span></span>
<span data-ttu-id="52e1b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e1b-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52e1b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e1b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52e1b-122">INPUTS</span></span>

### <span data-ttu-id="52e1b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="52e1b-123">System.String</span></span>

## <span data-ttu-id="52e1b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52e1b-124">OUTPUTS</span></span>

### <span data-ttu-id="52e1b-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="52e1b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="52e1b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="52e1b-126">NOTES</span></span>

## <span data-ttu-id="52e1b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52e1b-127">RELATED LINKS</span></span>

[<span data-ttu-id="52e1b-128">Neu – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="52e1b-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="52e1b-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="52e1b-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="52e1b-130">Satz-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="52e1b-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
