---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 8aeb992b08e2749168ef3da2db6c264158c6a9ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480318"
---
# <span data-ttu-id="d137e-101">Get-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d137e-101">Get-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="d137e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d137e-102">SYNOPSIS</span></span>
<span data-ttu-id="d137e-103">Ruft eine virtuelle Netzwerkverbindung in einem virtuellen Hub ab oder listet alle virtuellen Netzwerkverbindungen in einem virtuellen Hub auf.</span><span class="sxs-lookup"><span data-stu-id="d137e-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d137e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d137e-104">SYNTAX</span></span>

### <span data-ttu-id="d137e-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d137e-105">ByVirtualHubName (Default)</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d137e-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d137e-106">ByVirtualHubObject</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d137e-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d137e-107">ByVirtualHubResourceId</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d137e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d137e-108">DESCRIPTION</span></span>
<span data-ttu-id="d137e-109">Ruft eine virtuelle Netzwerkverbindung in einem virtuellen Hub ab oder listet alle virtuellen Netzwerkverbindungen in einem virtuellen Hub auf.</span><span class="sxs-lookup"><span data-stu-id="d137e-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="d137e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d137e-110">EXAMPLES</span></span>

### <span data-ttu-id="d137e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d137e-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="d137e-112">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="d137e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d137e-113">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="d137e-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="d137e-114">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, wird die virtuelle Hub-Netzwerkverbindung mit dem Namen der Ressourcengruppe, dem Hub-Namen und dem Verbindungsnamen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d137e-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="d137e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d137e-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="d137e-116">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="d137e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d137e-117">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="d137e-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="d137e-118">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, werden alle virtuellen Hub-Netzwerkverbindungen mit dem Namen der Ressourcengruppe und dem Hub-Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d137e-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

## <span data-ttu-id="d137e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d137e-119">PARAMETERS</span></span>

### <span data-ttu-id="d137e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d137e-120">-DefaultProfile</span></span>
<span data-ttu-id="d137e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d137e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d137e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d137e-122">-Name</span></span>
<span data-ttu-id="d137e-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d137e-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d137e-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d137e-124">-ParentObject</span></span>
<span data-ttu-id="d137e-125">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="d137e-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d137e-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d137e-126">-ParentResourceId</span></span>
<span data-ttu-id="d137e-127">Die übergeordnete Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d137e-127">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d137e-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d137e-128">-ParentResourceName</span></span>
<span data-ttu-id="d137e-129">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="d137e-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d137e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d137e-130">-ResourceGroupName</span></span>
<span data-ttu-id="d137e-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d137e-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d137e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d137e-132">CommonParameters</span></span>
<span data-ttu-id="d137e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d137e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d137e-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d137e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d137e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d137e-135">INPUTS</span></span>

### <span data-ttu-id="d137e-136">Keine</span><span class="sxs-lookup"><span data-stu-id="d137e-136">None</span></span>

## <span data-ttu-id="d137e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d137e-137">OUTPUTS</span></span>

### <span data-ttu-id="d137e-138">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="d137e-138">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="d137e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d137e-139">NOTES</span></span>

## <span data-ttu-id="d137e-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d137e-140">RELATED LINKS</span></span>
