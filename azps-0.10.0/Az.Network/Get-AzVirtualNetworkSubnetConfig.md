---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841479"
---
# <span data-ttu-id="1211b-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1211b-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="1211b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1211b-102">SYNOPSIS</span></span>
<span data-ttu-id="1211b-103">Ruft ein Subnetz in einem virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="1211b-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="1211b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1211b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1211b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1211b-105">DESCRIPTION</span></span>
<span data-ttu-id="1211b-106">Das Cmdlet " **Get-AzVirtualNetworkSubnetConfig** " ruft mindestens eine Subnetz-Konfiguration in einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="1211b-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="1211b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1211b-107">EXAMPLES</span></span>

### <span data-ttu-id="1211b-108">1: Abrufen eines Subnetzes in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="1211b-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="1211b-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1211b-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="1211b-110">Anschließend werden Daten zu diesem Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1211b-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="1211b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1211b-111">PARAMETERS</span></span>

### <span data-ttu-id="1211b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1211b-112">-DefaultProfile</span></span>
<span data-ttu-id="1211b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1211b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1211b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1211b-114">-Name</span></span>
<span data-ttu-id="1211b-115">Gibt den Namen der Subnet-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1211b-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1211b-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1211b-116">-VirtualNetwork</span></span>
<span data-ttu-id="1211b-117">Gibt das **VirtualNetwork** -Objekt an, das die Subnet-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1211b-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1211b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1211b-118">CommonParameters</span></span>
<span data-ttu-id="1211b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1211b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1211b-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1211b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1211b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1211b-121">INPUTS</span></span>

### <span data-ttu-id="1211b-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1211b-122">PSVirtualNetwork</span></span>
<span data-ttu-id="1211b-123">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1211b-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="1211b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1211b-124">OUTPUTS</span></span>

### <span data-ttu-id="1211b-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="1211b-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="1211b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1211b-126">NOTES</span></span>

## <span data-ttu-id="1211b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1211b-127">RELATED LINKS</span></span>

[<span data-ttu-id="1211b-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1211b-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1211b-129">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1211b-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1211b-130">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1211b-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1211b-131">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1211b-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


