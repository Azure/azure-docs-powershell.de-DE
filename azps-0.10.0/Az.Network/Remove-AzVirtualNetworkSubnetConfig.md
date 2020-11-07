---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 5f05672c5fd3f0866652507fd0f61f7a8b6e0fcc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843739"
---
# <span data-ttu-id="241fc-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="241fc-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="241fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="241fc-102">SYNOPSIS</span></span>
<span data-ttu-id="241fc-103">Entfernt eine Subnetz-Konfiguration aus einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="241fc-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="241fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="241fc-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="241fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="241fc-105">DESCRIPTION</span></span>
<span data-ttu-id="241fc-106">Das Cmdlet **Remove-AzVirtualNetworkSubnetConfig** entfernt ein Subnetz aus einem virtuellen Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="241fc-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="241fc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="241fc-107">EXAMPLES</span></span>

### <span data-ttu-id="241fc-108">1: Entfernen eines Subnets aus einem virtuellen Netzwerk und Aktualisieren des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="241fc-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="241fc-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="241fc-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="241fc-110">Anschließend wird der Befehl Remove-AzVirtualNetworkSubnetConfig verwendet, um das Back-End-Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="241fc-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="241fc-111">Set-AzVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk auf der Serverseite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="241fc-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="241fc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="241fc-112">PARAMETERS</span></span>

### <span data-ttu-id="241fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241fc-113">-DefaultProfile</span></span>
<span data-ttu-id="241fc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="241fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="241fc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="241fc-115">-Name</span></span>
<span data-ttu-id="241fc-116">Gibt den Namen der zu entfernenden Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="241fc-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="241fc-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241fc-117">-VirtualNetwork</span></span>
<span data-ttu-id="241fc-118">Gibt das **VirtualNetwork** -Objekt an, das die zu entfernende Subnet-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="241fc-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="241fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241fc-119">CommonParameters</span></span>
<span data-ttu-id="241fc-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241fc-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241fc-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241fc-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="241fc-122">INPUTS</span></span>

### <span data-ttu-id="241fc-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241fc-123">PSVirtualNetwork</span></span>
<span data-ttu-id="241fc-124">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="241fc-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="241fc-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="241fc-125">OUTPUTS</span></span>

### <span data-ttu-id="241fc-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241fc-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="241fc-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="241fc-127">NOTES</span></span>

## <span data-ttu-id="241fc-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="241fc-128">RELATED LINKS</span></span>

[<span data-ttu-id="241fc-129">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="241fc-129">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="241fc-130">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="241fc-130">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="241fc-131">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="241fc-131">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="241fc-132">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="241fc-132">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


