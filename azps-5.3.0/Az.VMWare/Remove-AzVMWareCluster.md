---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460508"
---
# <span data-ttu-id="73c3d-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="73c3d-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="73c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="73c3d-103">Löschen eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="73c3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73c3d-104">SYNTAX</span></span>

### <span data-ttu-id="73c3d-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="73c3d-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="73c3d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73c3d-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73c3d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="73c3d-108">Löschen eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="73c3d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="73c3d-110">Beispiel 1: Löschen des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="73c3d-111">Löschen eines Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="73c3d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73c3d-112">PARAMETERS</span></span>

### <span data-ttu-id="73c3d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73c3d-113">-AsJob</span></span>
<span data-ttu-id="73c3d-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="73c3d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="73c3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c3d-115">-DefaultProfile</span></span>
<span data-ttu-id="73c3d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73c3d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73c3d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73c3d-117">-InputObject</span></span>
<span data-ttu-id="73c3d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="73c3d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73c3d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="73c3d-119">-Name</span></span>
<span data-ttu-id="73c3d-120">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c3d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="73c3d-121">-NoWait</span></span>
<span data-ttu-id="73c3d-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="73c3d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="73c3d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73c3d-123">-PassThru</span></span>
<span data-ttu-id="73c3d-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="73c3d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="73c3d-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="73c3d-125">-PrivateCloudName</span></span>
<span data-ttu-id="73c3d-126">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-126">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c3d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c3d-127">-ResourceGroupName</span></span>
<span data-ttu-id="73c3d-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="73c3d-128">The name of the resource group.</span></span>
<span data-ttu-id="73c3d-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="73c3d-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c3d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73c3d-130">-SubscriptionId</span></span>
<span data-ttu-id="73c3d-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="73c3d-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c3d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73c3d-132">-Confirm</span></span>
<span data-ttu-id="73c3d-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73c3d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c3d-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="73c3d-134">-WhatIf</span></span>
<span data-ttu-id="73c3d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73c3d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c3d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73c3d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c3d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c3d-137">CommonParameters</span></span>
<span data-ttu-id="73c3d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c3d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c3d-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73c3d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c3d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73c3d-140">INPUTS</span></span>

### <span data-ttu-id="73c3d-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="73c3d-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="73c3d-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73c3d-142">OUTPUTS</span></span>

### <span data-ttu-id="73c3d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73c3d-143">System.Boolean</span></span>

## <span data-ttu-id="73c3d-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73c3d-144">NOTES</span></span>

<span data-ttu-id="73c3d-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="73c3d-145">ALIASES</span></span>

<span data-ttu-id="73c3d-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="73c3d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73c3d-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="73c3d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73c3d-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73c3d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73c3d-149">INPUTOBJECT <IVMWareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="73c3d-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73c3d-150">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="73c3d-151">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="73c3d-152">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="73c3d-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="73c3d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73c3d-154">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="73c3d-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="73c3d-155">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="73c3d-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="73c3d-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="73c3d-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="73c3d-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="73c3d-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="73c3d-158">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="73c3d-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="73c3d-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73c3d-159">RELATED LINKS</span></span>

