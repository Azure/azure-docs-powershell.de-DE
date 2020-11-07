---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: e5b881547f84714e238f541948602569c773c9c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660672"
---
# <span data-ttu-id="c40a1-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c40a1-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c40a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c40a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c40a1-103">Ruft ein Subnetz in einem virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="c40a1-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="c40a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c40a1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c40a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c40a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c40a1-106">Das Cmdlet " **Get-AzVirtualNetworkSubnetConfig** " ruft mindestens eine Subnetz-Konfiguration in einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="c40a1-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="c40a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c40a1-107">EXAMPLES</span></span>

### <span data-ttu-id="c40a1-108">1: Abrufen eines Subnetzes in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c40a1-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="c40a1-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="c40a1-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="c40a1-110">Anschließend werden Daten zu diesem Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c40a1-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="c40a1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c40a1-111">PARAMETERS</span></span>

### <span data-ttu-id="c40a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40a1-112">-DefaultProfile</span></span>
<span data-ttu-id="c40a1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c40a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c40a1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c40a1-114">-Name</span></span>
<span data-ttu-id="c40a1-115">Gibt den Namen der Subnet-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c40a1-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40a1-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c40a1-116">-VirtualNetwork</span></span>
<span data-ttu-id="c40a1-117">Gibt das **VirtualNetwork** -Objekt an, das die Subnet-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c40a1-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c40a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40a1-118">CommonParameters</span></span>
<span data-ttu-id="c40a1-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40a1-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c40a1-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40a1-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c40a1-121">INPUTS</span></span>

### <span data-ttu-id="c40a1-122">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c40a1-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c40a1-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c40a1-123">OUTPUTS</span></span>

### <span data-ttu-id="c40a1-124">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c40a1-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c40a1-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="c40a1-125">NOTES</span></span>

## <span data-ttu-id="c40a1-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c40a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="c40a1-127">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c40a1-127">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c40a1-128">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c40a1-128">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c40a1-129">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c40a1-129">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c40a1-130">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c40a1-130">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


