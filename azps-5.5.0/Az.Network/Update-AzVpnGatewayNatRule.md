---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: 60f68795e79e751dda75ae4d549d2b25a43392e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154028"
---
# <span data-ttu-id="b30a2-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="b30a2-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="b30a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b30a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b30a2-103">Aktualisiert eine NAT-Regel, die vpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b30a2-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="b30a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b30a2-104">SYNTAX</span></span>

### <span data-ttu-id="b30a2-105">ByVpnGatewayNatRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b30a2-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b30a2-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="b30a2-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b30a2-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="b30a2-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b30a2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b30a2-108">DESCRIPTION</span></span>
<span data-ttu-id="b30a2-109">Das **Cmdlet "Update-AzVpnGatewayNatRule"** aktualisiert eine NAT-Regel, die VpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b30a2-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="b30a2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b30a2-110">EXAMPLES</span></span>

### <span data-ttu-id="b30a2-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b30a2-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
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

<span data-ttu-id="b30a2-112">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk, ein virtueller Hub erstellt.</span><span class="sxs-lookup"><span data-stu-id="b30a2-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="b30a2-113">Anschließend erstellen wir VpnGateway unter diesem virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="b30a2-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="b30a2-114">Erstellen Sie dann eine neue NAT-Regel, die dem erstellten VpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b30a2-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="b30a2-115">Verwenden Sie diesen Befehl: "Update-AzVpnGatewayNatRule", "NAT-Regel aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="b30a2-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="b30a2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b30a2-116">PARAMETERS</span></span>

### <span data-ttu-id="b30a2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b30a2-117">-AsJob</span></span>
<span data-ttu-id="b30a2-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b30a2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b30a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30a2-119">-DefaultProfile</span></span>
<span data-ttu-id="b30a2-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b30a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b30a2-121">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="b30a2-121">-ExternalMapping</span></span>
<span data-ttu-id="b30a2-122">Liste der externen Subnetzzuordnungen für private IP-Adressen für NAT</span><span class="sxs-lookup"><span data-stu-id="b30a2-122">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30a2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b30a2-123">-InputObject</span></span>
<span data-ttu-id="b30a2-124">Das zu aktualisierende VpnGatewayNatRule-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b30a2-124">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b30a2-125">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="b30a2-125">-InternalMapping</span></span>
<span data-ttu-id="b30a2-126">Liste der internen Subnetzzuordnungen für NAT für private IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="b30a2-126">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30a2-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b30a2-127">-IpConfigurationId</span></span>
<span data-ttu-id="b30a2-128">Die IP-Konfigurations-ID, auf die diese NAT-Regel zutrifft</span><span class="sxs-lookup"><span data-stu-id="b30a2-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="b30a2-129">-Mode</span><span class="sxs-lookup"><span data-stu-id="b30a2-129">-Mode</span></span>
<span data-ttu-id="b30a2-130">Die Source NAT-Richtung eines VPN NAT</span><span class="sxs-lookup"><span data-stu-id="b30a2-130">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="b30a2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b30a2-131">-Name</span></span>
<span data-ttu-id="b30a2-132">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b30a2-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30a2-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b30a2-133">-ParentResourceName</span></span>
<span data-ttu-id="b30a2-134">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="b30a2-134">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30a2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30a2-135">-ResourceGroupName</span></span>
<span data-ttu-id="b30a2-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b30a2-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30a2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b30a2-137">-ResourceId</span></span>
<span data-ttu-id="b30a2-138">Die Ressourcen-ID des zu löschende VpnGatewayNatRule-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b30a2-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b30a2-139">-Type</span><span class="sxs-lookup"><span data-stu-id="b30a2-139">-Type</span></span>
<span data-ttu-id="b30a2-140">Der Typ der NAT-Regel für VPN NAT</span><span class="sxs-lookup"><span data-stu-id="b30a2-140">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="b30a2-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b30a2-141">-Confirm</span></span>
<span data-ttu-id="b30a2-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b30a2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b30a2-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b30a2-143">-WhatIf</span></span>
<span data-ttu-id="b30a2-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b30a2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b30a2-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b30a2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b30a2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30a2-146">CommonParameters</span></span>
<span data-ttu-id="b30a2-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30a2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30a2-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b30a2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30a2-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b30a2-149">INPUTS</span></span>

### <span data-ttu-id="b30a2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b30a2-150">System.String</span></span>

### <span data-ttu-id="b30a2-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="b30a2-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="b30a2-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b30a2-152">OUTPUTS</span></span>

### <span data-ttu-id="b30a2-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="b30a2-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="b30a2-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b30a2-154">NOTES</span></span>

## <span data-ttu-id="b30a2-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b30a2-155">RELATED LINKS</span></span>
