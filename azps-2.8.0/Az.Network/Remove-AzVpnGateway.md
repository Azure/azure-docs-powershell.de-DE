---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 17731d3f864f429fdad58bf767fb5cb25950387d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821295"
---
# <span data-ttu-id="2c22c-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2c22c-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="2c22c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c22c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c22c-103">Das Remove-AzVpnGateway-Cmdlet entfernt ein Azure VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c22c-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="2c22c-104">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="2c22c-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="2c22c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c22c-105">SYNTAX</span></span>

### <span data-ttu-id="2c22c-106">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c22c-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c22c-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2c22c-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c22c-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2c22c-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c22c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c22c-109">DESCRIPTION</span></span>
<span data-ttu-id="2c22c-110">Das Remove-AzVpnGateway-Cmdlet entfernt ein Azure VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c22c-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="2c22c-111">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="2c22c-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="2c22c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c22c-112">EXAMPLES</span></span>

### <span data-ttu-id="2c22c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c22c-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="2c22c-114">In diesem Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares VPN-Gateway in Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2c22c-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="2c22c-115">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="2c22c-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="2c22c-116">Dadurch werden die VpnGateway und alle VpnConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2c22c-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="2c22c-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2c22c-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="2c22c-118">In diesem Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares VPN-Gateway in Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2c22c-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="2c22c-119">Dieser Löschvorgang erfolgt mithilfe der PowerShell-Rohrverlegung, die das vom Get-AzVpnGateway-Befehl zurückgegebene VpnGateway-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c22c-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="2c22c-120">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="2c22c-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="2c22c-121">Dadurch werden die VpnGateway und alle VpnConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2c22c-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="2c22c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c22c-122">PARAMETERS</span></span>

### <span data-ttu-id="2c22c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c22c-123">-DefaultProfile</span></span>
<span data-ttu-id="2c22c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c22c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c22c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="2c22c-125">-Force</span></span>
<span data-ttu-id="2c22c-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2c22c-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c22c-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c22c-127">-InputObject</span></span>
<span data-ttu-id="2c22c-128">Das vpnGateway-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c22c-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="2c22c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2c22c-129">-Name</span></span>
<span data-ttu-id="2c22c-130">Der vpnGateway-Name.</span><span class="sxs-lookup"><span data-stu-id="2c22c-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="2c22c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c22c-131">-PassThru</span></span>
<span data-ttu-id="2c22c-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2c22c-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c22c-133">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2c22c-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c22c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c22c-134">-ResourceGroupName</span></span>
<span data-ttu-id="2c22c-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c22c-135">The resource group name.</span></span>

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

### <span data-ttu-id="2c22c-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2c22c-136">-ResourceId</span></span>
<span data-ttu-id="2c22c-137">Die Azure-Ressourcen-ID für die vpnGateway, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c22c-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="2c22c-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c22c-138">-Confirm</span></span>
<span data-ttu-id="2c22c-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c22c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c22c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c22c-140">-WhatIf</span></span>
<span data-ttu-id="2c22c-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c22c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c22c-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c22c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c22c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c22c-143">CommonParameters</span></span>
<span data-ttu-id="2c22c-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c22c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c22c-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c22c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c22c-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c22c-146">INPUTS</span></span>

### <span data-ttu-id="2c22c-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2c22c-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="2c22c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2c22c-148">System.String</span></span>

## <span data-ttu-id="2c22c-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c22c-149">OUTPUTS</span></span>

### <span data-ttu-id="2c22c-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c22c-150">System.Boolean</span></span>

## <span data-ttu-id="2c22c-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c22c-151">NOTES</span></span>

## <span data-ttu-id="2c22c-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c22c-152">RELATED LINKS</span></span>

[<span data-ttu-id="2c22c-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2c22c-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="2c22c-154">Neu – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2c22c-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="2c22c-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2c22c-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
