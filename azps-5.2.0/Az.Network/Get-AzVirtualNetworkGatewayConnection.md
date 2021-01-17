---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303160"
---
# <span data-ttu-id="16e4a-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="16e4a-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="16e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="16e4a-103">Ruft eine Virtuelle Netzwerkgatewayverbindung ab</span><span class="sxs-lookup"><span data-stu-id="16e4a-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="16e4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16e4a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16e4a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="16e4a-106">Die Virtuelle Netzwerkgatewayverbindung ist das Objekt, das den mit dem virtuellen Netzwerkgateway in Azure verbundenen IPsec-Tunnel (Site-to-Site oder Vnet-to-Vnet) darstellt.</span><span class="sxs-lookup"><span data-stu-id="16e4a-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="16e4a-107">Das **Cmdlet "Get-AzVirtualNetworkGatewayConnection"** gibt das Objekt Ihrer Verbindung basierend auf "Name" und "Ressourcengruppenname" zurück.</span><span class="sxs-lookup"><span data-stu-id="16e4a-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="16e4a-108">Wenn das **Cmdlet "Get-AzVirtualNetworkGatewayConnection"** ohne Angabe des Parameters "-Name" ausgegeben wird, werden in der Ausgabe keine ConnectionStatus- und SharedKey-Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="16e4a-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="16e4a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16e4a-109">EXAMPLES</span></span>

### <span data-ttu-id="16e4a-110">1: Herstellen einer Virtuellen Netzwerkgatewayverbindung</span><span class="sxs-lookup"><span data-stu-id="16e4a-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="16e4a-111">Gibt das Objekt der Virtuellen Netzwerkgatewayverbindung mit dem Namen "myKg" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="16e4a-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="16e4a-112">2: Erhalten aller Verbindungen des virtuellen Netzwerkgateways mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="16e4a-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="16e4a-113">Gibt alle Verbindungen des virtuellen Netzwerkgateways zurück, die mit "my Ganz" in der Ressourcengruppe "myRG" beginnen.</span><span class="sxs-lookup"><span data-stu-id="16e4a-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="16e4a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16e4a-114">PARAMETERS</span></span>

### <span data-ttu-id="16e4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e4a-115">-DefaultProfile</span></span>
<span data-ttu-id="16e4a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16e4a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e4a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="16e4a-117">-Name</span></span>
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

### <span data-ttu-id="16e4a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e4a-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="16e4a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e4a-119">CommonParameters</span></span>
<span data-ttu-id="16e4a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e4a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e4a-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16e4a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e4a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16e4a-122">INPUTS</span></span>

### <span data-ttu-id="16e4a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="16e4a-123">System.String</span></span>

## <span data-ttu-id="16e4a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16e4a-124">OUTPUTS</span></span>

### <span data-ttu-id="16e4a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="16e4a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="16e4a-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16e4a-126">NOTES</span></span>

## <span data-ttu-id="16e4a-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16e4a-127">RELATED LINKS</span></span>

[<span data-ttu-id="16e4a-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="16e4a-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="16e4a-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="16e4a-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="16e4a-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="16e4a-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
