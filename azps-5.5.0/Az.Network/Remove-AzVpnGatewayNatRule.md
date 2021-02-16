---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 35a59b24297efe3fd94a66d19a778913f488b800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146633"
---
# <span data-ttu-id="8f539-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="8f539-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="8f539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f539-102">SYNOPSIS</span></span>
<span data-ttu-id="8f539-103">Entfernt eine NAT-Regel, die vpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8f539-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="8f539-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f539-104">SYNTAX</span></span>

### <span data-ttu-id="8f539-105">ByVpnGatewayNatRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f539-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f539-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="8f539-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f539-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="8f539-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f539-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f539-108">DESCRIPTION</span></span>
<span data-ttu-id="8f539-109">Entfernt eine NAT-Regel, die vpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8f539-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="8f539-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f539-110">EXAMPLES</span></span>

### <span data-ttu-id="8f539-111">Beispiel1</span><span class="sxs-lookup"><span data-stu-id="8f539-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="8f539-112">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk, ein virtueller Hub, vpnGateway und eine diesem VpnGateway zugeordnete NAT-Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="8f539-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="8f539-113">Anschließend wird die NAT-Regel unter Verwendung des Namens der NAT-Regel entfernt.</span><span class="sxs-lookup"><span data-stu-id="8f539-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="8f539-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f539-114">PARAMETERS</span></span>

### <span data-ttu-id="8f539-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f539-115">-DefaultProfile</span></span>
<span data-ttu-id="8f539-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f539-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f539-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8f539-117">-Force</span></span>
<span data-ttu-id="8f539-118">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="8f539-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="8f539-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f539-119">-InputObject</span></span>
<span data-ttu-id="8f539-120">Das zu aktualisierende VpnGatewayNatRule-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f539-120">The VpnGatewayNatRule object to update.</span></span>

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

### <span data-ttu-id="8f539-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8f539-121">-Name</span></span>
<span data-ttu-id="8f539-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8f539-122">The resource name.</span></span>

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

### <span data-ttu-id="8f539-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="8f539-123">-ParentResourceName</span></span>
<span data-ttu-id="8f539-124">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8f539-124">The parent resource name.</span></span>

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

### <span data-ttu-id="8f539-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f539-125">-PassThru</span></span>
<span data-ttu-id="8f539-126">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f539-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="8f539-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f539-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f539-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f539-128">The resource group name.</span></span>

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

### <span data-ttu-id="8f539-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f539-129">-ResourceId</span></span>
<span data-ttu-id="8f539-130">Die Ressourcen-ID des zu löschende VpnGatewayNatRule-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f539-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f539-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f539-131">-Confirm</span></span>
<span data-ttu-id="8f539-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f539-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f539-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8f539-133">-WhatIf</span></span>
<span data-ttu-id="8f539-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f539-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f539-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f539-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f539-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f539-136">CommonParameters</span></span>
<span data-ttu-id="8f539-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f539-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f539-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f539-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f539-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f539-139">INPUTS</span></span>

### <span data-ttu-id="8f539-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8f539-140">System.String</span></span>

### <span data-ttu-id="8f539-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="8f539-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="8f539-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f539-142">OUTPUTS</span></span>

### <span data-ttu-id="8f539-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f539-143">System.Boolean</span></span>

## <span data-ttu-id="8f539-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f539-144">NOTES</span></span>

## <span data-ttu-id="8f539-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f539-145">RELATED LINKS</span></span>
