---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 5c91ba0dbca881e7e6a6909ef1b7200adf2ba1ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938024"
---
# <span data-ttu-id="92676-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="92676-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="92676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92676-102">SYNOPSIS</span></span>
<span data-ttu-id="92676-103">Entfernt eine NAT-Regel, die vpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92676-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="92676-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92676-104">SYNTAX</span></span>

### <span data-ttu-id="92676-105">ByVpnGatewayNatRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="92676-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92676-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="92676-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92676-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="92676-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92676-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92676-108">DESCRIPTION</span></span>
<span data-ttu-id="92676-109">Entfernt eine NAT-Regel, die vpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92676-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="92676-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92676-110">EXAMPLES</span></span>

### <span data-ttu-id="92676-111">Beispiel1</span><span class="sxs-lookup"><span data-stu-id="92676-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="92676-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub, VpnGateway und NAT-Regel erstellt, die diesem VpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92676-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="92676-113">Anschließend wird die NAT-Regel mit dem Namen der NAT-Regel entfernt.</span><span class="sxs-lookup"><span data-stu-id="92676-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="92676-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92676-114">PARAMETERS</span></span>

### <span data-ttu-id="92676-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92676-115">-DefaultProfile</span></span>
<span data-ttu-id="92676-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92676-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92676-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="92676-117">-Force</span></span>
<span data-ttu-id="92676-118">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="92676-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="92676-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92676-119">-InputObject</span></span>
<span data-ttu-id="92676-120">Das zu aktualisierende VpnGatewayNatRule-Objekt.</span><span class="sxs-lookup"><span data-stu-id="92676-120">The VpnGatewayNatRule object to update.</span></span>

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

### <span data-ttu-id="92676-121">-Name</span><span class="sxs-lookup"><span data-stu-id="92676-121">-Name</span></span>
<span data-ttu-id="92676-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="92676-122">The resource name.</span></span>

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

### <span data-ttu-id="92676-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="92676-123">-ParentResourceName</span></span>
<span data-ttu-id="92676-124">Der übergeordnete Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="92676-124">The parent resource name.</span></span>

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

### <span data-ttu-id="92676-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92676-125">-PassThru</span></span>
<span data-ttu-id="92676-126">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92676-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="92676-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92676-127">-ResourceGroupName</span></span>
<span data-ttu-id="92676-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="92676-128">The resource group name.</span></span>

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

### <span data-ttu-id="92676-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92676-129">-ResourceId</span></span>
<span data-ttu-id="92676-130">Die Ressourcen-ID des zu löschende VpnGatewayNatRule-Objekts.</span><span class="sxs-lookup"><span data-stu-id="92676-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

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

### <span data-ttu-id="92676-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92676-131">-Confirm</span></span>
<span data-ttu-id="92676-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92676-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92676-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92676-133">-WhatIf</span></span>
<span data-ttu-id="92676-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92676-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92676-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92676-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92676-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92676-136">CommonParameters</span></span>
<span data-ttu-id="92676-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92676-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92676-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92676-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92676-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92676-139">INPUTS</span></span>

### <span data-ttu-id="92676-140">System.String</span><span class="sxs-lookup"><span data-stu-id="92676-140">System.String</span></span>

### <span data-ttu-id="92676-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="92676-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="92676-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92676-142">OUTPUTS</span></span>

### <span data-ttu-id="92676-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92676-143">System.Boolean</span></span>

## <span data-ttu-id="92676-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92676-144">NOTES</span></span>

## <span data-ttu-id="92676-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92676-145">RELATED LINKS</span></span>
