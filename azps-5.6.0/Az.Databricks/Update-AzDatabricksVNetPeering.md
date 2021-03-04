---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: 60d679cf8540e39d1be293a46f9e4e441e397627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923720"
---
# <span data-ttu-id="bd396-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="bd396-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="bd396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd396-102">SYNOPSIS</span></span>
<span data-ttu-id="bd396-103">Aktualisieren sie vNet-Peering für Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="bd396-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="bd396-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd396-104">SYNTAX</span></span>

### <span data-ttu-id="bd396-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd396-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd396-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bd396-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd396-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd396-107">DESCRIPTION</span></span>
<span data-ttu-id="bd396-108">Aktualisieren sie vNet-Peering für Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="bd396-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="bd396-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd396-109">EXAMPLES</span></span>

### <span data-ttu-id="bd396-110">Beispiel 1: Aktualisieren von AllowForwardedTraffic von vnet peering</span><span class="sxs-lookup"><span data-stu-id="bd396-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="bd396-111">Mit diesem Befehl wird AllowForwardedTraffic von vnet peering aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bd396-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="bd396-112">Beispiel 2: Aktualisieren von AllowForwardedTraffic von vnet-Peering nach -Objekt</span><span class="sxs-lookup"><span data-stu-id="bd396-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="bd396-113">Mit diesem Befehl wird AllowForwardedTraffic des vnet-Peerings nach -Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bd396-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="bd396-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd396-114">PARAMETERS</span></span>

### <span data-ttu-id="bd396-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="bd396-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="bd396-116">[System.Management.Automation.SwitchParameter] Gibt an, ob der weitergeleitete Datenverkehr von den VMs im lokalen virtuellen Netzwerk im virtuellen Remotenetzwerk zulässig/nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="bd396-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="bd396-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="bd396-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="bd396-118">[System.Management.Automation.SwitchParameter] Wenn Gatewaylinks in virtuellen Remotenetzwerken verwendet werden können, um eine Verknüpfung mit diesem virtuellen Netzwerk zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd396-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="bd396-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="bd396-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="bd396-120">[System.Management.Automation.SwitchParameter] Ob die VMs im lokalen virtuellen Netzwerkbereich in der Lage wären, auf die VMs im virtuellen Remotenetzwerkbereich zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bd396-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="bd396-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd396-121">-AsJob</span></span>
<span data-ttu-id="bd396-122">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="bd396-122">Run the command as a job</span></span>

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

### <span data-ttu-id="bd396-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd396-123">-DefaultProfile</span></span>
<span data-ttu-id="bd396-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd396-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd396-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd396-125">-InputObject</span></span>
<span data-ttu-id="bd396-126">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="bd396-126">Identity parameter.</span></span>
<span data-ttu-id="bd396-127">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="bd396-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd396-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bd396-128">-Name</span></span>
<span data-ttu-id="bd396-129">Der Name des VNetPeerings.</span><span class="sxs-lookup"><span data-stu-id="bd396-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="bd396-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bd396-130">-NoWait</span></span>
<span data-ttu-id="bd396-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="bd396-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bd396-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd396-132">-ResourceGroupName</span></span>
<span data-ttu-id="bd396-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bd396-133">The name of the resource group.</span></span>
<span data-ttu-id="bd396-134">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="bd396-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bd396-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd396-135">-SubscriptionId</span></span>
<span data-ttu-id="bd396-136">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="bd396-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bd396-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="bd396-137">-UseRemoteGateway</span></span>
<span data-ttu-id="bd396-138">[System.Management.Automation.SwitchParameter] Wenn Remotegateways in diesem virtuellen Netzwerk verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bd396-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="bd396-139">Wenn das Kennzeichen auf "true" festgelegt ist und allowGatewayTransit für Remote-Peering ebenfalls wahr ist, verwendet das virtuelle Netzwerk Gateways des virtuellen Remotenetzwerks für die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="bd396-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="bd396-140">Dieses Kennzeichen kann nur für ein Peering auf "true" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bd396-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="bd396-141">Dieses Kennzeichen kann nicht festgelegt werden, wenn das virtuelle Netzwerk bereits über ein Gateway verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd396-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="bd396-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd396-142">-WorkspaceName</span></span>
<span data-ttu-id="bd396-143">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="bd396-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="bd396-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd396-144">-Confirm</span></span>
<span data-ttu-id="bd396-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd396-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd396-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd396-146">-WhatIf</span></span>
<span data-ttu-id="bd396-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd396-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd396-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd396-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd396-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd396-149">CommonParameters</span></span>
<span data-ttu-id="bd396-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd396-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd396-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd396-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd396-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd396-152">INPUTS</span></span>

### <span data-ttu-id="bd396-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="bd396-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="bd396-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd396-154">OUTPUTS</span></span>

### <span data-ttu-id="bd396-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="bd396-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="bd396-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd396-156">NOTES</span></span>

<span data-ttu-id="bd396-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bd396-157">ALIASES</span></span>

<span data-ttu-id="bd396-158">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="bd396-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd396-159">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="bd396-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd396-160">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd396-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd396-161">INPUTOBJECT <IDatabricksIdentity> : Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="bd396-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="bd396-162">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="bd396-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd396-163">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="bd396-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="bd396-164">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bd396-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bd396-165">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="bd396-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="bd396-166">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="bd396-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bd396-167">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="bd396-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="bd396-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd396-168">RELATED LINKS</span></span>

