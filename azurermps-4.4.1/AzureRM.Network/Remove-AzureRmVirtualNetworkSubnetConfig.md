---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: f2e0bb88df867da0a110422debea4d6688ad3af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501722"
---
# <span data-ttu-id="5a5b4-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a5b4-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5a5b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5b4-103">Entfernt eine Subnetz-Konfiguration aus einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a5b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a5b4-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a5b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a5b4-105">DESCRIPTION</span></span>
<span data-ttu-id="5a5b4-106">Das Cmdlet **Remove-AzureRmVirtualNetworkSubnetConfig** entfernt ein Subnetz aus einem virtuellen Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="5a5b4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a5b4-107">EXAMPLES</span></span>

### <span data-ttu-id="5a5b4-108">1: Entfernen eines Subnets aus einem virtuellen Netzwerk und Aktualisieren des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="5a5b4-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="5a5b4-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="5a5b4-110">Anschließend wird der Befehl Remove-AzureRmVirtualNetworkSubnetConfig verwendet, um das Back-End-Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5a5b4-111">Set-AzureRmVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk auf der Serverseite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="5a5b4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a5b4-112">PARAMETERS</span></span>

### <span data-ttu-id="5a5b4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5a5b4-113">-Name</span></span>
<span data-ttu-id="5a5b4-114">Gibt den Namen der zu entfernenden Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-114">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="5a5b4-115">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a5b4-115">-VirtualNetwork</span></span>
<span data-ttu-id="5a5b4-116">Gibt das **VirtualNetwork** -Objekt an, das die zu entfernende Subnet-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-116">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="5a5b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5b4-117">-DefaultProfile</span></span>
<span data-ttu-id="5a5b4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5b4-119">CommonParameters</span></span>
<span data-ttu-id="5a5b4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5b4-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a5b4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5b4-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a5b4-122">INPUTS</span></span>

### <span data-ttu-id="5a5b4-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a5b4-123">PSVirtualNetwork</span></span>
<span data-ttu-id="5a5b4-124">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a5b4-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="5a5b4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a5b4-125">OUTPUTS</span></span>

### <span data-ttu-id="5a5b4-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a5b4-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5a5b4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a5b4-127">NOTES</span></span>

## <span data-ttu-id="5a5b4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a5b4-128">RELATED LINKS</span></span>

[<span data-ttu-id="5a5b4-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a5b4-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5a5b4-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a5b4-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5a5b4-131">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a5b4-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5a5b4-132">Satz-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a5b4-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


