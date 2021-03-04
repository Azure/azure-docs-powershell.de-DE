---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: e4b972944f757c9b0072f091dc820de5fa5d5b1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924744"
---
# <span data-ttu-id="d219e-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d219e-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d219e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d219e-102">SYNOPSIS</span></span>
<span data-ttu-id="d219e-103">Ruft eine Verbindung mit einem virtuellen Netzwerkgateway ab</span><span class="sxs-lookup"><span data-stu-id="d219e-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="d219e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d219e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d219e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d219e-105">DESCRIPTION</span></span>
<span data-ttu-id="d219e-106">Die Virtual Network Gateway Connection ist das Objekt, das den IPsec-Tunnel (Site-to-Site oder Vnet-to-Vnet) darstellt, der mit Ihrem Virtuellen Netzwerkgateway in Azure verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d219e-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d219e-107">Das **Get-AzVirtualNetworkGatewayConnection-Cmdlet** gibt das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppenname zurück.</span><span class="sxs-lookup"><span data-stu-id="d219e-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="d219e-108">Wenn das **Get-AzVirtualNetworkGatewayConnection-Cmdlet** ohne Angabe des -Name-Parameters ausgegeben wird, werden in der Ausgabe keine Details zu ConnectionStatus und SharedKey angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d219e-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="d219e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d219e-109">EXAMPLES</span></span>

### <span data-ttu-id="d219e-110">1: Herstellen einer Virtuellen Netzwerkgatewayverbindung</span><span class="sxs-lookup"><span data-stu-id="d219e-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="d219e-111">Gibt das Objekt der Virtual Network Gateway Connection mit dem Namen "myTunnel" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="d219e-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="d219e-112">2: Alle Verbindungen des virtuellen Netzwerkgateways mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="d219e-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="d219e-113">Gibt alle Virtuellen Netzwerkgatewayverbindungen zurück, die mit "myTunnel" innerhalb der Ressourcengruppe "myRG" beginnen.</span><span class="sxs-lookup"><span data-stu-id="d219e-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="d219e-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d219e-114">PARAMETERS</span></span>

### <span data-ttu-id="d219e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d219e-115">-DefaultProfile</span></span>
<span data-ttu-id="d219e-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d219e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d219e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d219e-117">-Name</span></span>
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

### <span data-ttu-id="d219e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d219e-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d219e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d219e-119">CommonParameters</span></span>
<span data-ttu-id="d219e-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d219e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d219e-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d219e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d219e-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d219e-122">INPUTS</span></span>

### <span data-ttu-id="d219e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d219e-123">System.String</span></span>

## <span data-ttu-id="d219e-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d219e-124">OUTPUTS</span></span>

### <span data-ttu-id="d219e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d219e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d219e-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d219e-126">NOTES</span></span>

## <span data-ttu-id="d219e-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d219e-127">RELATED LINKS</span></span>

[<span data-ttu-id="d219e-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d219e-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d219e-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d219e-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d219e-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d219e-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
