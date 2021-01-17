---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472341"
---
# <span data-ttu-id="bbe9a-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="bbe9a-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="bbe9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbe9a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe9a-103">Trennt alle Follower einer Datenbank, die sich im Besitz dieses Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="bbe9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbe9a-104">SYNTAX</span></span>

### <span data-ttu-id="bbe9a-105">DetachExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="bbe9a-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bbe9a-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bbe9a-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bbe9a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbe9a-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe9a-108">Trennt alle Follower einer Datenbank, die sich im Besitz dieses Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="bbe9a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bbe9a-109">EXAMPLES</span></span>

### <span data-ttu-id="bbe9a-110">Beispiel 1: Trennen einer Folgedatenbank</span><span class="sxs-lookup"><span data-stu-id="bbe9a-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="bbe9a-111">Der obige Befehl trennt die in AttachedDatabaseConfiguration "myfollowerconfiguration" definierte Followerdatenbank von Cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="bbe9a-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="bbe9a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbe9a-112">PARAMETERS</span></span>

### <span data-ttu-id="bbe9a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbe9a-113">-AsJob</span></span>
<span data-ttu-id="bbe9a-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="bbe9a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bbe9a-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bbe9a-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="bbe9a-116">Ressourcenname der angefügten Datenbankkonfiguration im Follower-Cluster.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="bbe9a-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bbe9a-117">-ClusterName</span></span>
<span data-ttu-id="bbe9a-118">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9a-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe9a-119">-ClusterResourceId</span></span>
<span data-ttu-id="bbe9a-120">Ressourcen-ID des Clusters, der auf eine Datenbank folgt, die sich im Besitz dieses Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="bbe9a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe9a-121">-DefaultProfile</span></span>
<span data-ttu-id="bbe9a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbe9a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbe9a-123">-InputObject</span></span>
<span data-ttu-id="bbe9a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9a-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bbe9a-125">-NoWait</span></span>
<span data-ttu-id="bbe9a-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="bbe9a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bbe9a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbe9a-127">-PassThru</span></span>
<span data-ttu-id="bbe9a-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bbe9a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe9a-129">-ResourceGroupName</span></span>
<span data-ttu-id="bbe9a-130">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbe9a-131">-SubscriptionId</span></span>
<span data-ttu-id="bbe9a-132">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bbe9a-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbe9a-134">-Confirm</span></span>
<span data-ttu-id="bbe9a-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbe9a-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bbe9a-136">-WhatIf</span></span>
<span data-ttu-id="bbe9a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbe9a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbe9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe9a-139">CommonParameters</span></span>
<span data-ttu-id="bbe9a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe9a-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbe9a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe9a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bbe9a-142">INPUTS</span></span>

### <span data-ttu-id="bbe9a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="bbe9a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bbe9a-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bbe9a-144">OUTPUTS</span></span>

### <span data-ttu-id="bbe9a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbe9a-145">System.Boolean</span></span>

## <span data-ttu-id="bbe9a-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bbe9a-146">NOTES</span></span>

<span data-ttu-id="bbe9a-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bbe9a-147">ALIASES</span></span>

<span data-ttu-id="bbe9a-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="bbe9a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbe9a-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbe9a-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbe9a-151">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bbe9a-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbe9a-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bbe9a-153">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bbe9a-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bbe9a-155">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="bbe9a-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bbe9a-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="bbe9a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbe9a-157">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bbe9a-158">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bbe9a-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bbe9a-160">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bbe9a-161">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="bbe9a-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bbe9a-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bbe9a-162">RELATED LINKS</span></span>

