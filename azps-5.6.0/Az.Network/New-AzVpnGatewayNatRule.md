---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: d4f0b908a229ee47472d40eefe60c5771c0147d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934800"
---
# <span data-ttu-id="32cac-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="32cac-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="32cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32cac-102">SYNOPSIS</span></span>
<span data-ttu-id="32cac-103">Erstellt eine NAT-Regel auf einem VpnGateway, die mit VpnSiteLinkConnection verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="32cac-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="32cac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32cac-104">SYNTAX</span></span>

### <span data-ttu-id="32cac-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="32cac-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32cac-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="32cac-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32cac-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="32cac-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32cac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32cac-108">DESCRIPTION</span></span>
<span data-ttu-id="32cac-109">Erstellt eine NAT-Regel auf einem VpnGateway, die vpnGateway zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="32cac-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="32cac-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32cac-110">EXAMPLES</span></span>

### <span data-ttu-id="32cac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32cac-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule
```

<span data-ttu-id="32cac-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub erstellt.</span><span class="sxs-lookup"><span data-stu-id="32cac-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="32cac-113">Anschließend erstellen wir VpnGateway unter diesem virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="32cac-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="32cac-114">Anschließend kann mithilfe dieses Befehls: New-AzVpnGatewayNatRule die NAT-Regel erstellt und dem erstellten VpnGateway zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="32cac-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="32cac-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="32cac-115">PARAMETERS</span></span>

### <span data-ttu-id="32cac-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32cac-116">-AsJob</span></span>
<span data-ttu-id="32cac-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="32cac-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32cac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cac-118">-DefaultProfile</span></span>
<span data-ttu-id="32cac-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32cac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32cac-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="32cac-120">-ExternalMapping</span></span>
<span data-ttu-id="32cac-121">Liste der externen Subnetzzuordnungen für private IP-Adresse für NAT</span><span class="sxs-lookup"><span data-stu-id="32cac-121">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-122">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="32cac-122">-InternalMapping</span></span>
<span data-ttu-id="32cac-123">Die Liste der internen Subnetzzuordnungen für private IP-Adressen für NAT</span><span class="sxs-lookup"><span data-stu-id="32cac-123">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="32cac-124">-IpConfigurationId</span></span>
<span data-ttu-id="32cac-125">Die IP-Konfigurations-ID, die diese NAT-Regel für</span><span class="sxs-lookup"><span data-stu-id="32cac-125">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="32cac-126">-Modus</span><span class="sxs-lookup"><span data-stu-id="32cac-126">-Mode</span></span>
<span data-ttu-id="32cac-127">Die Quell-NAT-Richtung eines VPN-NAT</span><span class="sxs-lookup"><span data-stu-id="32cac-127">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-128">-Name</span><span class="sxs-lookup"><span data-stu-id="32cac-128">-Name</span></span>
<span data-ttu-id="32cac-129">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="32cac-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="32cac-130">-ParentObject</span></span>
<span data-ttu-id="32cac-131">Das übergeordnete VpnGateway für diese NAT-Regel.</span><span class="sxs-lookup"><span data-stu-id="32cac-131">The parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="32cac-132">-ParentResourceId</span></span>
<span data-ttu-id="32cac-133">Die Ressourcen-ID des übergeordneten VpnGateways für diese NAT-Regel.</span><span class="sxs-lookup"><span data-stu-id="32cac-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="32cac-134">-ParentResourceName</span></span>
<span data-ttu-id="32cac-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="32cac-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32cac-136">-ResourceGroupName</span></span>
<span data-ttu-id="32cac-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="32cac-137">The resource group name.</span></span>

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

### <span data-ttu-id="32cac-138">-Type</span><span class="sxs-lookup"><span data-stu-id="32cac-138">-Type</span></span>
<span data-ttu-id="32cac-139">Der Typ der NAT-Regel für VPN NAT</span><span class="sxs-lookup"><span data-stu-id="32cac-139">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cac-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32cac-140">-Confirm</span></span>
<span data-ttu-id="32cac-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32cac-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32cac-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32cac-142">-WhatIf</span></span>
<span data-ttu-id="32cac-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32cac-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32cac-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32cac-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32cac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cac-145">CommonParameters</span></span>
<span data-ttu-id="32cac-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32cac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cac-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32cac-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cac-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32cac-148">INPUTS</span></span>

### <span data-ttu-id="32cac-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="32cac-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="32cac-150">System.String</span><span class="sxs-lookup"><span data-stu-id="32cac-150">System.String</span></span>

## <span data-ttu-id="32cac-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32cac-151">OUTPUTS</span></span>

### <span data-ttu-id="32cac-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="32cac-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="32cac-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="32cac-153">NOTES</span></span>

## <span data-ttu-id="32cac-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="32cac-154">RELATED LINKS</span></span>
