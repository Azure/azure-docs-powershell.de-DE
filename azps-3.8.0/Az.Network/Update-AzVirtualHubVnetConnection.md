---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847456"
---
# <span data-ttu-id="e45be-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e45be-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e45be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e45be-102">SYNOPSIS</span></span>
<span data-ttu-id="e45be-103">Aktualisiert eine vorhandene HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="e45be-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="e45be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e45be-104">SYNTAX</span></span>

### <span data-ttu-id="e45be-105">ByHubVirtualNetworkConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e45be-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e45be-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e45be-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e45be-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="e45be-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e45be-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e45be-108">DESCRIPTION</span></span>
<span data-ttu-id="e45be-109">Aktualisiert eine vorhandene HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="e45be-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="e45be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e45be-110">EXAMPLES</span></span>

### <span data-ttu-id="e45be-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e45be-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
```

<span data-ttu-id="e45be-112">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="e45be-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e45be-113">Darüber hinaus wird eine virtuelle Netzwerkverbindung erstellt, die dem virtuellen Netzwerk Peer entspricht.</span><span class="sxs-lookup"><span data-stu-id="e45be-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="e45be-114">Diese virtuelle Netzwerkverbindung wird dann aktualisiert, um die Internetsicherheit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e45be-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="e45be-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e45be-115">PARAMETERS</span></span>

### <span data-ttu-id="e45be-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e45be-116">-AsJob</span></span>
<span data-ttu-id="e45be-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e45be-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e45be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45be-118">-DefaultProfile</span></span>
<span data-ttu-id="e45be-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e45be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45be-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e45be-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="e45be-121">Aktivieren Sie die Internetsicherheit für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e45be-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45be-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e45be-122">-InputObject</span></span>
<span data-ttu-id="e45be-123">Die zu ändernde hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e45be-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e45be-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e45be-124">-Name</span></span>
<span data-ttu-id="e45be-125">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e45be-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45be-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e45be-126">-ParentResourceName</span></span>
<span data-ttu-id="e45be-127">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="e45be-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45be-128">-ResourceGroupName</span></span>
<span data-ttu-id="e45be-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e45be-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45be-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e45be-130">-ResourceId</span></span>
<span data-ttu-id="e45be-131">Die Ressourcen-ID der zu ändernden hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e45be-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45be-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e45be-132">-Confirm</span></span>
<span data-ttu-id="e45be-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e45be-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45be-134">-WhatIf</span></span>
<span data-ttu-id="e45be-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e45be-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45be-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e45be-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45be-137">CommonParameters</span></span>
<span data-ttu-id="e45be-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e45be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45be-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45be-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45be-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e45be-140">INPUTS</span></span>

### <span data-ttu-id="e45be-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e45be-141">System.String</span></span>

### <span data-ttu-id="e45be-142">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e45be-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e45be-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e45be-143">OUTPUTS</span></span>

### <span data-ttu-id="e45be-144">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e45be-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e45be-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e45be-145">NOTES</span></span>

## <span data-ttu-id="e45be-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e45be-146">RELATED LINKS</span></span>