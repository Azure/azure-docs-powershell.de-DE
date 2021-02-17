---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158913"
---
# <span data-ttu-id="7bca0-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7bca0-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="7bca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bca0-102">SYNOPSIS</span></span>
<span data-ttu-id="7bca0-103">Das Remove-AzVpnGateway entfernt ein Azure VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7bca0-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="7bca0-104">Dies ist ein Gateway speziell für die softwaredefinierte Konnektivität des virtuellen Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="7bca0-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="7bca0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bca0-105">SYNTAX</span></span>

### <span data-ttu-id="7bca0-106">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bca0-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bca0-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7bca0-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bca0-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7bca0-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bca0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bca0-109">DESCRIPTION</span></span>
<span data-ttu-id="7bca0-110">Das Remove-AzVpnGateway entfernt ein Azure VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7bca0-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="7bca0-111">Dies ist ein Gateway speziell für die softwaredefinierte Konnektivität des virtuellen Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="7bca0-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="7bca0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7bca0-112">EXAMPLES</span></span>

### <span data-ttu-id="7bca0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bca0-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="7bca0-114">In diesem Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtueller Hub und ein skalierbares VPN-Gateway in den USA erstellt, die dann sofort gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7bca0-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="7bca0-115">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="7bca0-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="7bca0-116">Dadurch werden das VpnGateway und alle daran angefügten VpnConnections gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7bca0-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="7bca0-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7bca0-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="7bca0-118">In diesem Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtueller Hub und ein skalierbares VPN-Gateway in den USA erstellt, die dann sofort gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7bca0-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="7bca0-119">Dieser Löschvorgang erfolgt mithilfe der Powershell-Piping, die das vom Befehl "Get-AzVpnGateway" zurückgegebene Get-AzVpnGateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="7bca0-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="7bca0-120">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="7bca0-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="7bca0-121">Dadurch werden das VpnGateway und alle daran angefügten VpnConnections gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7bca0-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="7bca0-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bca0-122">PARAMETERS</span></span>

### <span data-ttu-id="7bca0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bca0-123">-DefaultProfile</span></span>
<span data-ttu-id="7bca0-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bca0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bca0-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7bca0-125">-Force</span></span>
<span data-ttu-id="7bca0-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="7bca0-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7bca0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bca0-127">-InputObject</span></span>
<span data-ttu-id="7bca0-128">Das zu löschende vpnGateway-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7bca0-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bca0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7bca0-129">-Name</span></span>
<span data-ttu-id="7bca0-130">Der Name des vpnGateways.</span><span class="sxs-lookup"><span data-stu-id="7bca0-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bca0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bca0-131">-PassThru</span></span>
<span data-ttu-id="7bca0-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7bca0-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7bca0-133">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7bca0-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7bca0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bca0-134">-ResourceGroupName</span></span>
<span data-ttu-id="7bca0-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7bca0-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bca0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bca0-136">-ResourceId</span></span>
<span data-ttu-id="7bca0-137">Die Azure-Ressourcen-ID für das zu löschende vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7bca0-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bca0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bca0-138">-Confirm</span></span>
<span data-ttu-id="7bca0-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bca0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bca0-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7bca0-140">-WhatIf</span></span>
<span data-ttu-id="7bca0-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bca0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bca0-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bca0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bca0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bca0-143">CommonParameters</span></span>
<span data-ttu-id="7bca0-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bca0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bca0-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bca0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bca0-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7bca0-146">INPUTS</span></span>

### <span data-ttu-id="7bca0-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7bca0-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="7bca0-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7bca0-148">System.String</span></span>

## <span data-ttu-id="7bca0-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7bca0-149">OUTPUTS</span></span>

### <span data-ttu-id="7bca0-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7bca0-150">System.Boolean</span></span>

## <span data-ttu-id="7bca0-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7bca0-151">NOTES</span></span>

## <span data-ttu-id="7bca0-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7bca0-152">RELATED LINKS</span></span>

[<span data-ttu-id="7bca0-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7bca0-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="7bca0-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7bca0-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="7bca0-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7bca0-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
