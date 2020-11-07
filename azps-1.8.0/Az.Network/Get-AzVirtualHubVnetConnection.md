---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 79bf22b5da9426ccb895b42faaeb4b01036828aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660695"
---
# <span data-ttu-id="15dc2-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="15dc2-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="15dc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="15dc2-103">Ruft eine virtuelle Netzwerkverbindung in einem virtuellen Hub ab oder listet alle virtuellen Netzwerkverbindungen in einem virtuellen Hub auf.</span><span class="sxs-lookup"><span data-stu-id="15dc2-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="15dc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15dc2-104">SYNTAX</span></span>

### <span data-ttu-id="15dc2-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="15dc2-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15dc2-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="15dc2-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15dc2-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="15dc2-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15dc2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="15dc2-109">Ruft eine virtuelle Netzwerkverbindung in einem virtuellen Hub ab oder listet alle virtuellen Netzwerkverbindungen in einem virtuellen Hub auf.</span><span class="sxs-lookup"><span data-stu-id="15dc2-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="15dc2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15dc2-110">EXAMPLES</span></span>

### <span data-ttu-id="15dc2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15dc2-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="15dc2-112">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="15dc2-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="15dc2-113">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="15dc2-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="15dc2-114">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, wird die virtuelle Hub-Netzwerkverbindung mit dem Namen der Ressourcengruppe, dem Hub-Namen und dem Verbindungsnamen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="15dc2-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="15dc2-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="15dc2-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="15dc2-116">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="15dc2-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="15dc2-117">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="15dc2-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="15dc2-118">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, werden alle virtuellen Hub-Netzwerkverbindungen mit dem Namen der Ressourcengruppe und dem Hub-Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="15dc2-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="15dc2-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="15dc2-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="15dc2-120">Dieses Cmdlet listet alle virtuellen Hub-Netzwerkverbindungen auf, die mit "Test" mit dem Namen der Ressourcengruppe und dem Namen des Hubs beginnen.</span><span class="sxs-lookup"><span data-stu-id="15dc2-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="15dc2-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="15dc2-121">PARAMETERS</span></span>

### <span data-ttu-id="15dc2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15dc2-122">-DefaultProfile</span></span>
<span data-ttu-id="15dc2-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15dc2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15dc2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="15dc2-124">-Name</span></span>
<span data-ttu-id="15dc2-125">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="15dc2-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="15dc2-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15dc2-126">-ParentObject</span></span>
<span data-ttu-id="15dc2-127">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="15dc2-127">The parent resource.</span></span>

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

### <span data-ttu-id="15dc2-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="15dc2-128">-ParentResourceId</span></span>
<span data-ttu-id="15dc2-129">Die übergeordnete Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="15dc2-129">The parent resource id.</span></span>

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

### <span data-ttu-id="15dc2-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="15dc2-130">-ParentResourceName</span></span>
<span data-ttu-id="15dc2-131">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="15dc2-131">The parent resource name.</span></span>

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

### <span data-ttu-id="15dc2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15dc2-132">-ResourceGroupName</span></span>
<span data-ttu-id="15dc2-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15dc2-133">The resource group name.</span></span>

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

### <span data-ttu-id="15dc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15dc2-134">CommonParameters</span></span>
<span data-ttu-id="15dc2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15dc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15dc2-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15dc2-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15dc2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15dc2-137">INPUTS</span></span>

### <span data-ttu-id="15dc2-138">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="15dc2-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="15dc2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="15dc2-139">System.String</span></span>

## <span data-ttu-id="15dc2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15dc2-140">OUTPUTS</span></span>

### <span data-ttu-id="15dc2-141">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="15dc2-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="15dc2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="15dc2-142">NOTES</span></span>

## <span data-ttu-id="15dc2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15dc2-143">RELATED LINKS</span></span>

[<span data-ttu-id="15dc2-144">Neu – AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="15dc2-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="15dc2-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="15dc2-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
