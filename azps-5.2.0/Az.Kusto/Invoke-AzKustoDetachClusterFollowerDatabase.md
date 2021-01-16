---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302227"
---
# <span data-ttu-id="be8f0-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="be8f0-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="be8f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="be8f0-103">Trennt alle Follower einer Datenbank, die sich im Besitz dieses Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="be8f0-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="be8f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be8f0-104">SYNTAX</span></span>

### <span data-ttu-id="be8f0-105">DetachExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="be8f0-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be8f0-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="be8f0-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be8f0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be8f0-107">DESCRIPTION</span></span>
<span data-ttu-id="be8f0-108">Trennt alle Follower einer Datenbank, die sich im Besitz dieses Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="be8f0-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="be8f0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be8f0-109">EXAMPLES</span></span>

### <span data-ttu-id="be8f0-110">Beispiel 1: Trennen einer Folgedatenbank</span><span class="sxs-lookup"><span data-stu-id="be8f0-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="be8f0-111">Der oben aufgeführte Befehl trennt die in AttachedDatabaseConfiguration "myfollowerconfiguration" definierte Followerdatenbank vom Cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="be8f0-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="be8f0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be8f0-112">PARAMETERS</span></span>

### <span data-ttu-id="be8f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be8f0-113">-AsJob</span></span>
<span data-ttu-id="be8f0-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="be8f0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="be8f0-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="be8f0-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="be8f0-116">Ressourcenname der angefügten Datenbankkonfiguration im Follower-Cluster.</span><span class="sxs-lookup"><span data-stu-id="be8f0-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="be8f0-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="be8f0-117">-ClusterName</span></span>
<span data-ttu-id="be8f0-118">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="be8f0-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="be8f0-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="be8f0-119">-ClusterResourceId</span></span>
<span data-ttu-id="be8f0-120">Ressourcen-ID des Clusters, der auf eine Datenbank folgt, die sich im Besitz dieses Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="be8f0-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="be8f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8f0-121">-DefaultProfile</span></span>
<span data-ttu-id="be8f0-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be8f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be8f0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be8f0-123">-InputObject</span></span>
<span data-ttu-id="be8f0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="be8f0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be8f0-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be8f0-125">-NoWait</span></span>
<span data-ttu-id="be8f0-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="be8f0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be8f0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be8f0-127">-PassThru</span></span>
<span data-ttu-id="be8f0-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="be8f0-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="be8f0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be8f0-129">-ResourceGroupName</span></span>
<span data-ttu-id="be8f0-130">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="be8f0-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="be8f0-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be8f0-131">-SubscriptionId</span></span>
<span data-ttu-id="be8f0-132">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="be8f0-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="be8f0-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="be8f0-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="be8f0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be8f0-134">-Confirm</span></span>
<span data-ttu-id="be8f0-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be8f0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be8f0-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="be8f0-136">-WhatIf</span></span>
<span data-ttu-id="be8f0-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be8f0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be8f0-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be8f0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be8f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8f0-139">CommonParameters</span></span>
<span data-ttu-id="be8f0-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be8f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8f0-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be8f0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8f0-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be8f0-142">INPUTS</span></span>

### <span data-ttu-id="be8f0-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="be8f0-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="be8f0-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be8f0-144">OUTPUTS</span></span>

### <span data-ttu-id="be8f0-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be8f0-145">System.Boolean</span></span>

## <span data-ttu-id="be8f0-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be8f0-146">NOTES</span></span>

<span data-ttu-id="be8f0-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="be8f0-147">ALIASES</span></span>

<span data-ttu-id="be8f0-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="be8f0-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be8f0-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="be8f0-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be8f0-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be8f0-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be8f0-151">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="be8f0-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be8f0-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="be8f0-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="be8f0-153">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="be8f0-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="be8f0-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="be8f0-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="be8f0-155">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="be8f0-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="be8f0-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="be8f0-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be8f0-157">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="be8f0-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="be8f0-158">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="be8f0-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="be8f0-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="be8f0-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="be8f0-160">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="be8f0-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="be8f0-161">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="be8f0-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="be8f0-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be8f0-162">RELATED LINKS</span></span>

