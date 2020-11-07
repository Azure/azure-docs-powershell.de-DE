---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e8b824e889965ca608a589c52d72c8f383678ca8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660471"
---
# <span data-ttu-id="6d029-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6d029-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="6d029-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d029-102">SYNOPSIS</span></span>
<span data-ttu-id="6d029-103">Mit dem New-AzVirtualHubVnetConnection-Cmdlet wird eine HubVirtualNetworkConnection-Ressource erstellt, die einem virtuellen Netzwerk mit dem Azure Virtual-Hub Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d029-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="6d029-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d029-104">SYNTAX</span></span>

### <span data-ttu-id="6d029-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d029-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d029-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6d029-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d029-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="6d029-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d029-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6d029-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d029-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="6d029-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d029-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6d029-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d029-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d029-111">DESCRIPTION</span></span>
<span data-ttu-id="6d029-112">Mit dem New-AzVirtualHubVnetConnection-Cmdlet wird eine HubVirtualNetworkConnection-Ressource erstellt, die einem virtuellen Netzwerk mit dem Azure Virtual-Hub Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d029-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="6d029-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d029-113">EXAMPLES</span></span>

### <span data-ttu-id="6d029-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d029-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="6d029-115">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="6d029-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="6d029-116">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="6d029-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="6d029-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d029-117">PARAMETERS</span></span>

### <span data-ttu-id="6d029-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d029-118">-AsJob</span></span>
<span data-ttu-id="6d029-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6d029-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d029-120">-DefaultProfile</span></span>
<span data-ttu-id="6d029-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d029-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d029-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6d029-122">-Name</span></span>
<span data-ttu-id="6d029-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6d029-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6d029-124">-ParentObject</span></span>
<span data-ttu-id="6d029-125">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="6d029-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6d029-126">-ParentResourceId</span></span>
<span data-ttu-id="6d029-127">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="6d029-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6d029-128">-ParentResourceName</span></span>
<span data-ttu-id="6d029-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d029-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6d029-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="6d029-131">Das virtuelle Remotenetzwerk, mit dem diese virtuelle Hub-Netzwerkverbindung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6d029-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6d029-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="6d029-133">Das virtuelle Remotenetzwerk, mit dem diese virtuelle Hub-Netzwerkverbindung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6d029-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d029-134">-ResourceGroupName</span></span>
<span data-ttu-id="6d029-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d029-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d029-136">-Confirm</span></span>
<span data-ttu-id="6d029-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d029-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d029-138">-WhatIf</span></span>
<span data-ttu-id="6d029-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d029-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d029-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d029-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d029-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d029-141">CommonParameters</span></span>
<span data-ttu-id="6d029-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d029-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d029-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d029-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d029-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d029-144">INPUTS</span></span>

### <span data-ttu-id="6d029-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d029-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6d029-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6d029-146">System.String</span></span>

## <span data-ttu-id="6d029-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d029-147">OUTPUTS</span></span>

### <span data-ttu-id="6d029-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="6d029-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="6d029-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d029-149">NOTES</span></span>

## <span data-ttu-id="6d029-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d029-150">RELATED LINKS</span></span>

[<span data-ttu-id="6d029-151">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6d029-151">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="6d029-152">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6d029-152">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
