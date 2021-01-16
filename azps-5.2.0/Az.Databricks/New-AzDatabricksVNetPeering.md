---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368793"
---
# <span data-ttu-id="905d1-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="905d1-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="905d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905d1-102">SYNOPSIS</span></span>
<span data-ttu-id="905d1-103">Erstellt vNet Peering für Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="905d1-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="905d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="905d1-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="905d1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="905d1-105">DESCRIPTION</span></span>
<span data-ttu-id="905d1-106">Erstellt vNet Peering für Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="905d1-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="905d1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="905d1-107">EXAMPLES</span></span>

### <span data-ttu-id="905d1-108">Beispiel 1: Erstellen eines vnet-Peerings für Databinnen und Daten</span><span class="sxs-lookup"><span data-stu-id="905d1-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="905d1-109">Mit diesem Befehl wird ein vnet-Peering für Databinnen erstellt.</span><span class="sxs-lookup"><span data-stu-id="905d1-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="905d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="905d1-110">PARAMETERS</span></span>

### <span data-ttu-id="905d1-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="905d1-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="905d1-112">Gibt an, ob der weitergeleitete Datenverkehr von den VMs im lokalen virtuellen Netzwerk im virtuellen Remotenetzwerk zugelassen bzw. nicht zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="905d1-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="905d1-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="905d1-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="905d1-114">Wenn Gatewaylinks in virtuellen Remotenetzwerken verwendet werden können, um eine Verknüpfung mit diesem virtuellen Netzwerk zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="905d1-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="905d1-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="905d1-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="905d1-116">Ob die VMs im lokalen virtuellen Netzwerkbereich auf die VMs im remote virtuellen Netzwerkbereich zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="905d1-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="905d1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="905d1-117">-AsJob</span></span>
<span data-ttu-id="905d1-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="905d1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="905d1-119">-DataberinsAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="905d1-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="905d1-120">Eine Liste der Adressblöcke, die für dieses virtuelle Netzwerk in der CIDR-Notation reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="905d1-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="905d1-121">-DatabidosVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="905d1-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="905d1-122">Die ID des virtuellen Datennetzwerks.</span><span class="sxs-lookup"><span data-stu-id="905d1-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="905d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905d1-123">-DefaultProfile</span></span>
<span data-ttu-id="905d1-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="905d1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905d1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="905d1-125">-Name</span></span>
<span data-ttu-id="905d1-126">Der Name des vNet-Arbeitsbereichs-Peerings.</span><span class="sxs-lookup"><span data-stu-id="905d1-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905d1-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="905d1-127">-NoWait</span></span>
<span data-ttu-id="905d1-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="905d1-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="905d1-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="905d1-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="905d1-130">Eine Liste der Adressblöcke, die für dieses virtuelle Netzwerk in der CIDR-Notation reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="905d1-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="905d1-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="905d1-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="905d1-132">Die ID des virtuellen Remotenetzwerks.</span><span class="sxs-lookup"><span data-stu-id="905d1-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="905d1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905d1-133">-ResourceGroupName</span></span>
<span data-ttu-id="905d1-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="905d1-134">The name of the resource group.</span></span>
<span data-ttu-id="905d1-135">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="905d1-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905d1-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="905d1-136">-SubscriptionId</span></span>
<span data-ttu-id="905d1-137">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="905d1-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905d1-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="905d1-138">-UseRemoteGateway</span></span>
<span data-ttu-id="905d1-139">Remotegateways können in diesem virtuellen Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="905d1-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="905d1-140">Wenn das Kennzeichen auf "true" festgelegt ist und "allowGatewayTransit" für Remote peering ebenfalls "true" ist, verwendet das virtuelle Netzwerk Gateways des virtuellen Remotenetzwerks für die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="905d1-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="905d1-141">Dieses Kennzeichen kann nur für einen Peering auf "true" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="905d1-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="905d1-142">Dieses Kennzeichen kann nicht festgelegt werden, wenn das virtuelle Netzwerk bereits über ein Gateway verfügt.</span><span class="sxs-lookup"><span data-stu-id="905d1-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="905d1-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="905d1-143">-WorkspaceName</span></span>
<span data-ttu-id="905d1-144">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="905d1-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905d1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="905d1-145">-Confirm</span></span>
<span data-ttu-id="905d1-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="905d1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="905d1-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="905d1-147">-WhatIf</span></span>
<span data-ttu-id="905d1-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="905d1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="905d1-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="905d1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="905d1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905d1-150">CommonParameters</span></span>
<span data-ttu-id="905d1-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905d1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905d1-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="905d1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905d1-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="905d1-153">INPUTS</span></span>

## <span data-ttu-id="905d1-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="905d1-154">OUTPUTS</span></span>

### <span data-ttu-id="905d1-155">Microsoft.Azure.PowerShell.Cmdlets.Databaffes.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="905d1-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="905d1-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="905d1-156">NOTES</span></span>

<span data-ttu-id="905d1-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="905d1-157">ALIASES</span></span>

## <span data-ttu-id="905d1-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="905d1-158">RELATED LINKS</span></span>

