---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175692"
---
# <span data-ttu-id="3f468-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="3f468-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="3f468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f468-102">SYNOPSIS</span></span>
<span data-ttu-id="3f468-103">Aktualisieren Sie vNet Peering für Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="3f468-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="3f468-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f468-104">SYNTAX</span></span>

### <span data-ttu-id="3f468-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f468-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f468-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3f468-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f468-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f468-107">DESCRIPTION</span></span>
<span data-ttu-id="3f468-108">Aktualisieren Sie vNet Peering für Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="3f468-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="3f468-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f468-109">EXAMPLES</span></span>

### <span data-ttu-id="3f468-110">Beispiel 1: Aktualisieren von "AllowForwardedTraffic" für vnet-Peering</span><span class="sxs-lookup"><span data-stu-id="3f468-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="3f468-111">Mit diesem Befehl wird "AllowForwardedTraffic" des vnet-Peerings aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f468-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="3f468-112">Beispiel 2: Aktualisieren von "AllowForwardedTraffic" des vnet-Peerings nach Objekt</span><span class="sxs-lookup"><span data-stu-id="3f468-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="3f468-113">Mit diesem Befehl wird "AllowForwardedTraffic" des vnet-Peerings nach Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f468-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="3f468-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f468-114">PARAMETERS</span></span>

### <span data-ttu-id="3f468-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="3f468-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="3f468-116">[System.Management.Automation.SwitchParameter] Gibt an, ob der weitergeleitete Datenverkehr von den VMs im lokalen virtuellen Netzwerk im virtuellen Remotenetzwerk zugelassen bzw. nicht zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="3f468-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="3f468-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="3f468-118">[System.Management.Automation.SwitchParameter] Wenn Gatewaylinks in virtuellen Remotenetzwerken verwendet werden können, um eine Verknüpfung mit diesem virtuellen Netzwerk zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f468-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="3f468-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="3f468-120">[System.Management.Automation.SwitchParameter] Gibt an, ob die VMs im lokalen virtuellen Netzwerkbereich im Remotespeicherplatz des virtuellen Netzwerks auf die VMs zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="3f468-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f468-121">-AsJob</span></span>
<span data-ttu-id="3f468-122">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f468-122">Run the command as a job</span></span>

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

### <span data-ttu-id="3f468-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f468-123">-DefaultProfile</span></span>
<span data-ttu-id="3f468-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f468-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f468-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f468-125">-InputObject</span></span>
<span data-ttu-id="3f468-126">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="3f468-126">Identity parameter.</span></span>
<span data-ttu-id="3f468-127">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3f468-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3f468-128">-Name</span></span>
<span data-ttu-id="3f468-129">Der Name von VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="3f468-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f468-130">-NoWait</span></span>
<span data-ttu-id="3f468-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3f468-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f468-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f468-132">-ResourceGroupName</span></span>
<span data-ttu-id="3f468-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f468-133">The name of the resource group.</span></span>
<span data-ttu-id="3f468-134">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="3f468-134">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f468-135">-SubscriptionId</span></span>
<span data-ttu-id="3f468-136">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3f468-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="3f468-137">-UseRemoteGateway</span></span>
<span data-ttu-id="3f468-138">[System.Management.Automation.SwitchParameter] Wenn Remotegateways in diesem virtuellen Netzwerk verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3f468-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="3f468-139">Wenn das Kennzeichen auf "true" festgelegt ist und "allowGatewayTransit" für Remote peering ebenfalls "true" ist, verwendet das virtuelle Netzwerk Gateways des virtuellen Remotenetzwerks für die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="3f468-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="3f468-140">Dieses Kennzeichen kann nur für einen Peering auf "true" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3f468-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="3f468-141">Dieses Kennzeichen kann nicht festgelegt werden, wenn das virtuelle Netzwerk bereits über ein Gateway verfügt.</span><span class="sxs-lookup"><span data-stu-id="3f468-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f468-142">-WorkspaceName</span></span>
<span data-ttu-id="3f468-143">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3f468-143">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f468-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f468-144">-Confirm</span></span>
<span data-ttu-id="3f468-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f468-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f468-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3f468-146">-WhatIf</span></span>
<span data-ttu-id="3f468-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f468-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f468-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f468-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f468-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f468-149">CommonParameters</span></span>
<span data-ttu-id="3f468-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f468-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f468-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f468-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f468-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f468-152">INPUTS</span></span>

### <span data-ttu-id="3f468-153">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.IDatabseriesIdentity</span><span class="sxs-lookup"><span data-stu-id="3f468-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="3f468-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f468-154">OUTPUTS</span></span>

### <span data-ttu-id="3f468-155">Microsoft.Azure.PowerShell.Cmdlets.Databaffes.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3f468-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="3f468-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f468-156">NOTES</span></span>

<span data-ttu-id="3f468-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3f468-157">ALIASES</span></span>

<span data-ttu-id="3f468-158">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3f468-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f468-159">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f468-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f468-160">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f468-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f468-161">INPUTOBJECT <IDatabricksIdentity> : Identity-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3f468-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="3f468-162">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3f468-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f468-163">`[PeeringName <String>]`: Der Name des vNet-Arbeitsbereichs-Peerings.</span><span class="sxs-lookup"><span data-stu-id="3f468-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="3f468-164">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f468-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3f468-165">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="3f468-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="3f468-166">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3f468-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3f468-167">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3f468-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="3f468-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f468-168">RELATED LINKS</span></span>

