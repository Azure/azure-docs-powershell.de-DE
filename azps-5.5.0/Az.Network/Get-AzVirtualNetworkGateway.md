---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147081"
---
# <span data-ttu-id="1781b-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1781b-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="1781b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1781b-102">SYNOPSIS</span></span>
<span data-ttu-id="1781b-103">Ruft ein virtuelles Netzwerkgateway ab</span><span class="sxs-lookup"><span data-stu-id="1781b-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="1781b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1781b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1781b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1781b-105">DESCRIPTION</span></span>
<span data-ttu-id="1781b-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="1781b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="1781b-107">Das **Cmdlet "Get-AzVirtualNetworkGateway"** gibt das Objekt Ihres Gateways in Azure basierend auf "Name" und "Ressourcengruppenname" zurück.</span><span class="sxs-lookup"><span data-stu-id="1781b-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="1781b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1781b-108">EXAMPLES</span></span>

### <span data-ttu-id="1781b-109">Beispiel 1: Erhalten eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="1781b-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="1781b-110">Gibt das Objekt des virtuellen Netzwerkgateways mit dem Namen "myGateway1" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="1781b-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="1781b-111">Beispiel 2: Erhalten eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="1781b-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="1781b-112">Gibt alle Virtuellen Netzwerkgateways zurück, die mit "myGateway" innerhalb der Ressourcengruppe "myRG" beginnen.</span><span class="sxs-lookup"><span data-stu-id="1781b-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="1781b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1781b-113">PARAMETERS</span></span>

### <span data-ttu-id="1781b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1781b-114">-DefaultProfile</span></span>
<span data-ttu-id="1781b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1781b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1781b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1781b-116">-Name</span></span>
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

### <span data-ttu-id="1781b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1781b-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1781b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1781b-118">CommonParameters</span></span>
<span data-ttu-id="1781b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1781b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1781b-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1781b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1781b-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1781b-121">INPUTS</span></span>

### <span data-ttu-id="1781b-122">System.String</span><span class="sxs-lookup"><span data-stu-id="1781b-122">System.String</span></span>

## <span data-ttu-id="1781b-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1781b-123">OUTPUTS</span></span>

### <span data-ttu-id="1781b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1781b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1781b-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1781b-125">NOTES</span></span>

## <span data-ttu-id="1781b-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1781b-126">RELATED LINKS</span></span>

[<span data-ttu-id="1781b-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1781b-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1781b-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1781b-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1781b-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1781b-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1781b-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1781b-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1781b-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1781b-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
