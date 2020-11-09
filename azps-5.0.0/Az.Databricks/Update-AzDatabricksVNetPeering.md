---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297303"
---
# <span data-ttu-id="ce69e-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="ce69e-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="ce69e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce69e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce69e-103">Aktualisieren Sie vNet-Peering für Workspace.</span><span class="sxs-lookup"><span data-stu-id="ce69e-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="ce69e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce69e-104">SYNTAX</span></span>

### <span data-ttu-id="ce69e-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce69e-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce69e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ce69e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce69e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce69e-107">DESCRIPTION</span></span>
<span data-ttu-id="ce69e-108">Aktualisieren Sie vNet-Peering für Workspace.</span><span class="sxs-lookup"><span data-stu-id="ce69e-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="ce69e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce69e-109">EXAMPLES</span></span>

### <span data-ttu-id="ce69e-110">Beispiel 1: Aktualisieren von AllowForwardedTraffic von vnet-Peering</span><span class="sxs-lookup"><span data-stu-id="ce69e-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="ce69e-111">Dieser Befehl aktualisiert AllowForwardedTraffic des vnet-Peerings.</span><span class="sxs-lookup"><span data-stu-id="ce69e-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="ce69e-112">Beispiel 2: Aktualisieren von AllowForwardedTraffic von vnet-Peering nach Objekt</span><span class="sxs-lookup"><span data-stu-id="ce69e-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="ce69e-113">Dieser Befehl aktualisiert AllowForwardedTraffic von vnet-Peering nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="ce69e-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="ce69e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce69e-114">PARAMETERS</span></span>

### <span data-ttu-id="ce69e-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="ce69e-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="ce69e-116">[System. Management. Automation. Switchparameter] gibt an, ob der weitergeleitete Datenverkehr von den VMS im lokalen virtuellen Netzwerk im virtuellen Remotenetzwerk zugelassen/nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ce69e-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="ce69e-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="ce69e-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="ce69e-118">[System. Management. Automation. Switchparameter], wenn Gateway-Links im virtuellen Remotenetzwerk verwendet werden können, um eine Verknüpfung mit diesem virtuellen Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ce69e-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="ce69e-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ce69e-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="ce69e-120">[System. Management. Automation. Switchparameter] unabhängig davon, ob die VMs im lokalen virtuellen Netzwerkbereich auf die VMs im Remotespeicher des virtuellen Netzwerks zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="ce69e-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="ce69e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce69e-121">-AsJob</span></span>
<span data-ttu-id="ce69e-122">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ce69e-122">Run the command as a job</span></span>

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

### <span data-ttu-id="ce69e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce69e-123">-DefaultProfile</span></span>
<span data-ttu-id="ce69e-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce69e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce69e-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ce69e-125">-InputObject</span></span>
<span data-ttu-id="ce69e-126">Parameter Identity.</span><span class="sxs-lookup"><span data-stu-id="ce69e-126">Identity parameter.</span></span>
<span data-ttu-id="ce69e-127">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ce69e-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ce69e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ce69e-128">-Name</span></span>
<span data-ttu-id="ce69e-129">Der Name des VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="ce69e-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="ce69e-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ce69e-130">-NoWait</span></span>
<span data-ttu-id="ce69e-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ce69e-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce69e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce69e-132">-ResourceGroupName</span></span>
<span data-ttu-id="ce69e-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce69e-133">The name of the resource group.</span></span>
<span data-ttu-id="ce69e-134">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ce69e-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ce69e-135">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ce69e-135">-SubscriptionId</span></span>
<span data-ttu-id="ce69e-136">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ce69e-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ce69e-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="ce69e-137">-UseRemoteGateway</span></span>
<span data-ttu-id="ce69e-138">[System. Management. Automation. Switchparameter], wenn Remote Gateways in diesem virtuellen Netzwerk verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ce69e-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="ce69e-139">Wenn das Flag auf "true" festgelegt ist und allowGatewayTransit auf Remote Peering ebenfalls wahr ist, verwendet virtuelles Netzwerkgateways des virtuellen Remotenetzwerks für die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="ce69e-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="ce69e-140">Dieses Flag kann nur von einem Peering auf "true" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ce69e-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="ce69e-141">Dieses Flag kann nicht gesetzt werden, wenn virtuelles Netzwerk bereits über ein Gateway verfügt.</span><span class="sxs-lookup"><span data-stu-id="ce69e-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="ce69e-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce69e-142">-WorkspaceName</span></span>
<span data-ttu-id="ce69e-143">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ce69e-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="ce69e-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce69e-144">-Confirm</span></span>
<span data-ttu-id="ce69e-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce69e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce69e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce69e-146">-WhatIf</span></span>
<span data-ttu-id="ce69e-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce69e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce69e-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce69e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce69e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce69e-149">CommonParameters</span></span>
<span data-ttu-id="ce69e-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce69e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce69e-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce69e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce69e-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce69e-152">INPUTS</span></span>

### <span data-ttu-id="ce69e-153">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="ce69e-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="ce69e-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce69e-154">OUTPUTS</span></span>

### <span data-ttu-id="ce69e-155">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ce69e-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="ce69e-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce69e-156">NOTES</span></span>

<span data-ttu-id="ce69e-157">Aliase</span><span class="sxs-lookup"><span data-stu-id="ce69e-157">ALIASES</span></span>

<span data-ttu-id="ce69e-158">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce69e-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce69e-159">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ce69e-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce69e-160">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ce69e-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce69e-161">Inputobject <IDatabricksIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="ce69e-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="ce69e-162">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="ce69e-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce69e-163">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="ce69e-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="ce69e-164">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce69e-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ce69e-165">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ce69e-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="ce69e-166">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ce69e-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ce69e-167">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ce69e-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="ce69e-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce69e-168">RELATED LINKS</span></span>

