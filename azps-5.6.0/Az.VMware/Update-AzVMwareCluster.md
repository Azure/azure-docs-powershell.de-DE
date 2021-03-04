---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: f708d1b752c0d8106d7a8f9f7613fa74b6b19937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937211"
---
# <span data-ttu-id="1f610-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="1f610-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="1f610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f610-102">SYNOPSIS</span></span>
<span data-ttu-id="1f610-103">Aktualisieren eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="1f610-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f610-104">SYNTAX</span></span>

### <span data-ttu-id="1f610-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f610-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f610-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1f610-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f610-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f610-107">DESCRIPTION</span></span>
<span data-ttu-id="1f610-108">Aktualisieren eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="1f610-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1f610-109">EXAMPLES</span></span>

### <span data-ttu-id="1f610-110">Beispiel 1: Aktualisieren der Clustergröße nach Name</span><span class="sxs-lookup"><span data-stu-id="1f610-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="1f610-111">Aktualisieren der Clustergröße nach Name</span><span class="sxs-lookup"><span data-stu-id="1f610-111">Update cluster size by name</span></span>

### <span data-ttu-id="1f610-112">Beispiel 2: Aktualisieren der Clustergröße nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1f610-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="1f610-113">Aktualisieren der Clustergröße nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1f610-113">Update cluster size by input object</span></span>

## <span data-ttu-id="1f610-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1f610-114">PARAMETERS</span></span>

### <span data-ttu-id="1f610-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f610-115">-AsJob</span></span>
<span data-ttu-id="1f610-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1f610-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1f610-117">-ClusterGröße</span><span class="sxs-lookup"><span data-stu-id="1f610-117">-ClusterSize</span></span>
<span data-ttu-id="1f610-118">Die Clustergröße</span><span class="sxs-lookup"><span data-stu-id="1f610-118">The cluster size</span></span>

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

### <span data-ttu-id="1f610-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f610-119">-DefaultProfile</span></span>
<span data-ttu-id="1f610-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f610-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f610-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f610-121">-InputObject</span></span>
<span data-ttu-id="1f610-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1f610-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f610-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1f610-123">-Name</span></span>
<span data-ttu-id="1f610-124">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="1f610-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1f610-125">-NoWait</span></span>
<span data-ttu-id="1f610-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1f610-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1f610-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1f610-127">-PrivateCloudName</span></span>
<span data-ttu-id="1f610-128">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="1f610-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f610-129">-ResourceGroupName</span></span>
<span data-ttu-id="1f610-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1f610-130">The name of the resource group.</span></span>
<span data-ttu-id="1f610-131">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="1f610-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1f610-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f610-132">-SubscriptionId</span></span>
<span data-ttu-id="1f610-133">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1f610-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1f610-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f610-134">-Confirm</span></span>
<span data-ttu-id="1f610-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f610-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f610-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f610-136">-WhatIf</span></span>
<span data-ttu-id="1f610-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f610-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f610-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f610-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f610-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f610-139">CommonParameters</span></span>
<span data-ttu-id="1f610-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f610-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f610-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f610-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f610-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1f610-142">INPUTS</span></span>

### <span data-ttu-id="1f610-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="1f610-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="1f610-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1f610-144">OUTPUTS</span></span>

### <span data-ttu-id="1f610-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="1f610-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="1f610-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1f610-146">NOTES</span></span>

<span data-ttu-id="1f610-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1f610-147">ALIASES</span></span>

<span data-ttu-id="1f610-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1f610-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f610-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="1f610-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f610-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f610-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f610-151">INPUTOBJECT <IVMWareIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="1f610-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f610-152">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1f610-153">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1f610-154">`[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1f610-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="1f610-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f610-156">`[Location <String>]`: Azure Region</span><span class="sxs-lookup"><span data-stu-id="1f610-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1f610-157">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="1f610-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1f610-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1f610-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1f610-159">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="1f610-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="1f610-160">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1f610-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1f610-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1f610-161">RELATED LINKS</span></span>

