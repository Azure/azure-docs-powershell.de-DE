---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: a6affc87ab0ace3e3808d43ac6bd9cfeb9496970
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178511"
---
# <span data-ttu-id="78afd-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="78afd-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="78afd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78afd-102">SYNOPSIS</span></span>
<span data-ttu-id="78afd-103">Das Remove-AzVirtualHubVnetConnection-Cmdlet entfernt eine Azure-Virtual-Netzwerkverbindung, die einem Remote-VNET mit dem Hub-VNET Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="78afd-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="78afd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78afd-104">SYNTAX</span></span>

### <span data-ttu-id="78afd-105">ByHubVirtualNetworkConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="78afd-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78afd-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="78afd-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78afd-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="78afd-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78afd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78afd-108">DESCRIPTION</span></span>
<span data-ttu-id="78afd-109">Das Remove-AzVirtualHubVnetConnection-Cmdlet entfernt eine Azure-Virtual-Netzwerkverbindung, die einem Remote-VNET mit dem Hub-VNET Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="78afd-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="78afd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78afd-110">EXAMPLES</span></span>

### <span data-ttu-id="78afd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78afd-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="78afd-112">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="78afd-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="78afd-113">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="78afd-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="78afd-114">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, wird die virtuelle Hub-Netzwerkverbindung mit dem Namen der Ressourcengruppe, dem Hub-Namen und dem Verbindungsnamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="78afd-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="78afd-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="78afd-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="78afd-116">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="78afd-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="78afd-117">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="78afd-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="78afd-118">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, wird die virtuelle Hub-Netzwerkverbindung mithilfe von PowerShell-Piping für die Ausgabe von Get-AzHubVirtualNetworkConnection entfernt.</span><span class="sxs-lookup"><span data-stu-id="78afd-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="78afd-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="78afd-119">PARAMETERS</span></span>

### <span data-ttu-id="78afd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78afd-120">-AsJob</span></span>
<span data-ttu-id="78afd-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="78afd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78afd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78afd-122">-DefaultProfile</span></span>
<span data-ttu-id="78afd-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78afd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78afd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="78afd-124">-Force</span></span>
<span data-ttu-id="78afd-125">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="78afd-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="78afd-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78afd-126">-InputObject</span></span>
<span data-ttu-id="78afd-127">Die zu ändernde hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="78afd-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78afd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="78afd-128">-Name</span></span>
<span data-ttu-id="78afd-129">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="78afd-129">The resource name.</span></span>

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

### <span data-ttu-id="78afd-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="78afd-130">-ParentResourceName</span></span>
<span data-ttu-id="78afd-131">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="78afd-131">The parent resource name.</span></span>

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

### <span data-ttu-id="78afd-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78afd-132">-PassThru</span></span>
<span data-ttu-id="78afd-133">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="78afd-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78afd-134">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="78afd-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78afd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78afd-135">-ResourceGroupName</span></span>
<span data-ttu-id="78afd-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78afd-136">The resource group name.</span></span>

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

### <span data-ttu-id="78afd-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="78afd-137">-ResourceId</span></span>
<span data-ttu-id="78afd-138">Die Ressourcen-ID der zu ändernden hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="78afd-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="78afd-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78afd-139">-Confirm</span></span>
<span data-ttu-id="78afd-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78afd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78afd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78afd-141">-WhatIf</span></span>
<span data-ttu-id="78afd-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78afd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78afd-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78afd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78afd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78afd-144">CommonParameters</span></span>
<span data-ttu-id="78afd-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78afd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78afd-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78afd-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78afd-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78afd-147">INPUTS</span></span>

### <span data-ttu-id="78afd-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="78afd-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="78afd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="78afd-149">System.String</span></span>

## <span data-ttu-id="78afd-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78afd-150">OUTPUTS</span></span>

### <span data-ttu-id="78afd-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78afd-151">System.Boolean</span></span>

## <span data-ttu-id="78afd-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="78afd-152">NOTES</span></span>

## <span data-ttu-id="78afd-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78afd-153">RELATED LINKS</span></span>

[<span data-ttu-id="78afd-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="78afd-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="78afd-155">Neu – AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="78afd-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
