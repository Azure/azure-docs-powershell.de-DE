---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: cfe9a8aa16803433055eb0cec5993cedcbcb5874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149761"
---
# <span data-ttu-id="6d6cb-101">Update-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="6d6cb-101">Update-AzVMwareCluster</span></span>

## <span data-ttu-id="6d6cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6cb-103">Aktualisieren eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="6d6cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d6cb-104">SYNTAX</span></span>

### <span data-ttu-id="6d6cb-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d6cb-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d6cb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6d6cb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwareCluster -InputObject <IVMwareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d6cb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d6cb-107">DESCRIPTION</span></span>
<span data-ttu-id="6d6cb-108">Aktualisieren eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="6d6cb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d6cb-109">EXAMPLES</span></span>

### <span data-ttu-id="6d6cb-110">Beispiel 1: Aktualisieren der Clustergröße nach Name</span><span class="sxs-lookup"><span data-stu-id="6d6cb-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="6d6cb-111">Aktualisieren der Clustergröße nach Name</span><span class="sxs-lookup"><span data-stu-id="6d6cb-111">Update cluster size by name</span></span>

### <span data-ttu-id="6d6cb-112">Beispiel 2: Aktualisieren der Clustergröße nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="6d6cb-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMwareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="6d6cb-113">Aktualisieren der Clustergröße durch Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="6d6cb-113">Update cluster size by input object</span></span>

## <span data-ttu-id="6d6cb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d6cb-114">PARAMETERS</span></span>

### <span data-ttu-id="6d6cb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d6cb-115">-AsJob</span></span>
<span data-ttu-id="6d6cb-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6d6cb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6d6cb-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="6d6cb-117">-ClusterSize</span></span>
<span data-ttu-id="6d6cb-118">Clustergröße</span><span class="sxs-lookup"><span data-stu-id="6d6cb-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6cb-119">-DefaultProfile</span></span>
<span data-ttu-id="6d6cb-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d6cb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d6cb-121">-InputObject</span></span>
<span data-ttu-id="6d6cb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d6cb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6d6cb-123">-Name</span></span>
<span data-ttu-id="6d6cb-124">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6cb-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6d6cb-125">-NoWait</span></span>
<span data-ttu-id="6d6cb-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6d6cb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d6cb-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="6d6cb-127">-PrivateCloudName</span></span>
<span data-ttu-id="6d6cb-128">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="6d6cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d6cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d6cb-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-130">The name of the resource group.</span></span>
<span data-ttu-id="6d6cb-131">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6d6cb-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d6cb-132">-SubscriptionId</span></span>
<span data-ttu-id="6d6cb-133">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6d6cb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d6cb-134">-Confirm</span></span>
<span data-ttu-id="6d6cb-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d6cb-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6d6cb-136">-WhatIf</span></span>
<span data-ttu-id="6d6cb-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6cb-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d6cb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6cb-139">CommonParameters</span></span>
<span data-ttu-id="6d6cb-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d6cb-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d6cb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6cb-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d6cb-142">INPUTS</span></span>

### <span data-ttu-id="6d6cb-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="6d6cb-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="6d6cb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d6cb-144">OUTPUTS</span></span>

### <span data-ttu-id="6d6cb-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="6d6cb-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="6d6cb-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6d6cb-146">NOTES</span></span>

<span data-ttu-id="6d6cb-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6d6cb-147">ALIASES</span></span>

<span data-ttu-id="6d6cb-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6d6cb-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d6cb-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d6cb-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d6cb-151">INPUTOBJECT <IVMwareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6d6cb-151">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d6cb-152">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="6d6cb-153">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="6d6cb-154">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="6d6cb-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6d6cb-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d6cb-156">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="6d6cb-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="6d6cb-157">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="6d6cb-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="6d6cb-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6d6cb-159">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="6d6cb-160">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6d6cb-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6d6cb-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6d6cb-161">RELATED LINKS</span></span>

