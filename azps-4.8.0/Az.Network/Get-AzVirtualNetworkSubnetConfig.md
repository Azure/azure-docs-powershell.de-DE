---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009692"
---
# <span data-ttu-id="9ddcb-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9ddcb-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9ddcb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ddcb-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddcb-103">Ruft ein Subnetz in einem virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="9ddcb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ddcb-104">SYNTAX</span></span>

### <span data-ttu-id="9ddcb-105">GetByVirtualNetwork (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ddcb-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ddcb-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ddcb-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ddcb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ddcb-107">DESCRIPTION</span></span>
<span data-ttu-id="9ddcb-108">Das Cmdlet " **Get-AzVirtualNetworkSubnetConfig** " ruft mindestens eine Subnetz-Konfiguration in einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="9ddcb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ddcb-109">EXAMPLES</span></span>

### <span data-ttu-id="9ddcb-110">1: Abrufen eines Subnetzes in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="9ddcb-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="9ddcb-111">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="9ddcb-112">Anschließend werden Daten zu diesem Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="9ddcb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ddcb-113">PARAMETERS</span></span>

### <span data-ttu-id="9ddcb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddcb-114">-DefaultProfile</span></span>
<span data-ttu-id="9ddcb-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ddcb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9ddcb-116">-Name</span></span>
<span data-ttu-id="9ddcb-117">Gibt den Namen der Subnet-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddcb-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9ddcb-118">-ResourceId</span></span>
<span data-ttu-id="9ddcb-119">Gibt die Ressourcen-ID des Subnets an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddcb-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9ddcb-120">-VirtualNetwork</span></span>
<span data-ttu-id="9ddcb-121">Gibt das **VirtualNetwork** -Objekt an, das die Subnet-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddcb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddcb-122">CommonParameters</span></span>
<span data-ttu-id="9ddcb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ddcb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddcb-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddcb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddcb-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ddcb-125">INPUTS</span></span>

### <span data-ttu-id="9ddcb-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9ddcb-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="9ddcb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9ddcb-127">System.String</span></span>

## <span data-ttu-id="9ddcb-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ddcb-128">OUTPUTS</span></span>

### <span data-ttu-id="9ddcb-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="9ddcb-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="9ddcb-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ddcb-130">NOTES</span></span>

## <span data-ttu-id="9ddcb-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ddcb-131">RELATED LINKS</span></span>

[<span data-ttu-id="9ddcb-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9ddcb-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9ddcb-133">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9ddcb-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9ddcb-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9ddcb-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9ddcb-135">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9ddcb-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
