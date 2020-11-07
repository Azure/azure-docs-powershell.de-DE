---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ceb009dba1984f69e7da3e04a9ae57a9da14c067
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850680"
---
# <span data-ttu-id="cdc59-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdc59-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="cdc59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdc59-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc59-103">Ruft ein Subnetz in einem virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="cdc59-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdc59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdc59-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc59-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdc59-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc59-106">Das Cmdlet " **Get-AzureRmVirtualNetworkSubnetConfig** " ruft mindestens eine Subnetz-Konfiguration in einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="cdc59-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="cdc59-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdc59-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc59-108">1: Abrufen eines Subnetzes in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="cdc59-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="cdc59-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="cdc59-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="cdc59-110">Anschließend werden Daten zu diesem Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cdc59-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="cdc59-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdc59-111">PARAMETERS</span></span>

### <span data-ttu-id="cdc59-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc59-112">-DefaultProfile</span></span>
<span data-ttu-id="cdc59-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdc59-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc59-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cdc59-114">-Name</span></span>
<span data-ttu-id="cdc59-115">Gibt den Namen der Subnet-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cdc59-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc59-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdc59-116">-VirtualNetwork</span></span>
<span data-ttu-id="cdc59-117">Gibt das **VirtualNetwork** -Objekt an, das die Subnet-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cdc59-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc59-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc59-118">CommonParameters</span></span>
<span data-ttu-id="cdc59-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc59-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc59-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc59-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc59-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdc59-121">INPUTS</span></span>

### <span data-ttu-id="cdc59-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdc59-122">PSVirtualNetwork</span></span>
<span data-ttu-id="cdc59-123">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdc59-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="cdc59-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdc59-124">OUTPUTS</span></span>

### <span data-ttu-id="cdc59-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cdc59-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cdc59-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdc59-126">NOTES</span></span>

## <span data-ttu-id="cdc59-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdc59-127">RELATED LINKS</span></span>

[<span data-ttu-id="cdc59-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdc59-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="cdc59-129">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdc59-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="cdc59-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdc59-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="cdc59-131">Satz-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdc59-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


