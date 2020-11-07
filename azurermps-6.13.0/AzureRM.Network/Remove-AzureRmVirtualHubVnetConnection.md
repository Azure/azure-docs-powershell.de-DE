---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 3a7c48803f18bf73f75e721296757e37ff89d44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662313"
---
# <span data-ttu-id="4ca5e-101">Remove-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4ca5e-101">Remove-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="4ca5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ca5e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca5e-103">Das Remove-AzureRmVirtualHubVnetConnection-Cmdlet entfernt eine Azure-Virtual-Netzwerkverbindung, die einem Remote-VNET mit dem Hub-VNET Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-103">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ca5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ca5e-104">SYNTAX</span></span>

### <span data-ttu-id="4ca5e-105">ByHubVirtualNetworkConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ca5e-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ca5e-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4ca5e-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzureRmVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca5e-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca5e-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ca5e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ca5e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ca5e-109">Das Remove-AzureRmVirtualHubVnetConnection-Cmdlet entfernt eine Azure-Virtual-Netzwerkverbindung, die einem Remote-VNET mit dem Hub-VNET Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-109">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="4ca5e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ca5e-110">EXAMPLES</span></span>

### <span data-ttu-id="4ca5e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ca5e-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="4ca5e-112">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4ca5e-113">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="4ca5e-114">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, wird die virtuelle Hub-Netzwerkverbindung mit dem Namen der Ressourcengruppe, dem Hub-Namen und dem Verbindungsnamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="4ca5e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ca5e-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzureRmHubVnetConnection
```

<span data-ttu-id="4ca5e-116">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4ca5e-117">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="4ca5e-118">Nachdem die virtuelle Hub-Netzwerkverbindung erstellt wurde, wird die virtuelle Hub-Netzwerkverbindung mithilfe von PowerShell-Piping für die Ausgabe von Get-AzureRmHubVirtualNetworkConnection entfernt.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzureRmHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="4ca5e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ca5e-119">PARAMETERS</span></span>

### <span data-ttu-id="4ca5e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ca5e-120">-AsJob</span></span>
<span data-ttu-id="4ca5e-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4ca5e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ca5e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca5e-122">-DefaultProfile</span></span>
<span data-ttu-id="4ca5e-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca5e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4ca5e-124">-Force</span></span>
<span data-ttu-id="4ca5e-125">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="4ca5e-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4ca5e-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ca5e-126">-InputObject</span></span>
<span data-ttu-id="4ca5e-127">Die zu ändernde hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="4ca5e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4ca5e-128">-Name</span></span>
<span data-ttu-id="4ca5e-129">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-129">The resource name.</span></span>

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

### <span data-ttu-id="4ca5e-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4ca5e-130">-ParentResourceName</span></span>
<span data-ttu-id="4ca5e-131">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-131">The parent resource name.</span></span>

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

### <span data-ttu-id="4ca5e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ca5e-132">-PassThru</span></span>
<span data-ttu-id="4ca5e-133">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4ca5e-134">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ca5e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ca5e-135">-ResourceGroupName</span></span>
<span data-ttu-id="4ca5e-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-136">The resource group name.</span></span>

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

### <span data-ttu-id="4ca5e-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4ca5e-137">-ResourceId</span></span>
<span data-ttu-id="4ca5e-138">Die Ressourcen-ID der zu ändernden hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="4ca5e-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ca5e-139">-Confirm</span></span>
<span data-ttu-id="4ca5e-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ca5e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca5e-141">-WhatIf</span></span>
<span data-ttu-id="4ca5e-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ca5e-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ca5e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca5e-144">CommonParameters</span></span>
<span data-ttu-id="4ca5e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca5e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca5e-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca5e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca5e-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ca5e-147">INPUTS</span></span>

### <span data-ttu-id="4ca5e-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="4ca5e-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="4ca5e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4ca5e-149">System.String</span></span>

## <span data-ttu-id="4ca5e-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ca5e-150">OUTPUTS</span></span>

### <span data-ttu-id="4ca5e-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca5e-151">System.Boolean</span></span>

## <span data-ttu-id="4ca5e-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ca5e-152">NOTES</span></span>

## <span data-ttu-id="4ca5e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ca5e-153">RELATED LINKS</span></span>
