---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: f410ba5dc89f29c3a928ed459be87769bf5ffca7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922971"
---
# <span data-ttu-id="f6f53-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="f6f53-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="f6f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f53-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f53-103">Trennt alle Follower einer Datenbank, die sich im Besitz dieses Clusters befindet.</span><span class="sxs-lookup"><span data-stu-id="f6f53-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="f6f53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6f53-104">SYNTAX</span></span>

### <span data-ttu-id="f6f53-105">DetachExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6f53-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6f53-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f6f53-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6f53-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6f53-107">DESCRIPTION</span></span>
<span data-ttu-id="f6f53-108">Trennt alle Follower einer Datenbank, die sich im Besitz dieses Clusters befindet.</span><span class="sxs-lookup"><span data-stu-id="f6f53-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="f6f53-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6f53-109">EXAMPLES</span></span>

### <span data-ttu-id="f6f53-110">Beispiel 1: Trennen einer Followerdatenbank</span><span class="sxs-lookup"><span data-stu-id="f6f53-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="f6f53-111">Der obige Befehl trennt die in AttachedDatabaseConfiguration "myfollowerconfiguration" definierte Followerdatenbank vom Cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="f6f53-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="f6f53-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6f53-112">PARAMETERS</span></span>

### <span data-ttu-id="f6f53-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6f53-113">-AsJob</span></span>
<span data-ttu-id="f6f53-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f6f53-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f6f53-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f6f53-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="f6f53-116">Ressourcenname der angefügten Datenbankkonfiguration im Followercluster.</span><span class="sxs-lookup"><span data-stu-id="f6f53-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="f6f53-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f6f53-117">-ClusterName</span></span>
<span data-ttu-id="f6f53-118">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f6f53-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f6f53-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="f6f53-119">-ClusterResourceId</span></span>
<span data-ttu-id="f6f53-120">Ressourcen-ID des Clusters, der auf eine Datenbank folgt, die sich im Besitz dieses Clusters befindet.</span><span class="sxs-lookup"><span data-stu-id="f6f53-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="f6f53-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f53-121">-DefaultProfile</span></span>
<span data-ttu-id="f6f53-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6f53-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f53-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6f53-123">-InputObject</span></span>
<span data-ttu-id="f6f53-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f6f53-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6f53-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f6f53-125">-NoWait</span></span>
<span data-ttu-id="f6f53-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f6f53-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f6f53-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6f53-127">-PassThru</span></span>
<span data-ttu-id="f6f53-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6f53-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6f53-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f53-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6f53-130">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f6f53-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f6f53-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6f53-131">-SubscriptionId</span></span>
<span data-ttu-id="f6f53-132">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f6f53-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6f53-133">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="f6f53-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6f53-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6f53-134">-Confirm</span></span>
<span data-ttu-id="f6f53-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6f53-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f53-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f53-136">-WhatIf</span></span>
<span data-ttu-id="f6f53-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6f53-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6f53-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6f53-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f53-139">CommonParameters</span></span>
<span data-ttu-id="f6f53-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f53-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6f53-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f53-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6f53-142">INPUTS</span></span>

### <span data-ttu-id="f6f53-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f6f53-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f6f53-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6f53-144">OUTPUTS</span></span>

### <span data-ttu-id="f6f53-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6f53-145">System.Boolean</span></span>

## <span data-ttu-id="f6f53-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6f53-146">NOTES</span></span>

<span data-ttu-id="f6f53-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f6f53-147">ALIASES</span></span>

<span data-ttu-id="f6f53-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f6f53-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6f53-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f6f53-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6f53-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6f53-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6f53-151">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="f6f53-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6f53-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f6f53-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f6f53-153">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f6f53-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f6f53-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="f6f53-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f6f53-155">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f6f53-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f6f53-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f6f53-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6f53-157">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="f6f53-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f6f53-158">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f6f53-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f6f53-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f6f53-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f6f53-160">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f6f53-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f6f53-161">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="f6f53-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f6f53-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6f53-162">RELATED LINKS</span></span>

