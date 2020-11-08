---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179207"
---
# <span data-ttu-id="91d7c-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="91d7c-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="91d7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="91d7c-103">Trennt alle Nachfolger einer Datenbank, die sich im Besitz dieses Clusters befindet.</span><span class="sxs-lookup"><span data-stu-id="91d7c-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="91d7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91d7c-104">SYNTAX</span></span>

### <span data-ttu-id="91d7c-105">DetachExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="91d7c-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="91d7c-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="91d7c-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91d7c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91d7c-107">DESCRIPTION</span></span>
<span data-ttu-id="91d7c-108">Trennt alle Nachfolger einer Datenbank, die sich im Besitz dieses Clusters befindet.</span><span class="sxs-lookup"><span data-stu-id="91d7c-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="91d7c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91d7c-109">EXAMPLES</span></span>

### <span data-ttu-id="91d7c-110">Beispiel 1: Trennen einer Nachfolger Datenbank</span><span class="sxs-lookup"><span data-stu-id="91d7c-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="91d7c-111">Der obige Befehl trennt die in AttachedDatabaseConfiguration "myfollowerconfiguration" definierte Nachfolger Datenbank aus dem Cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="91d7c-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="91d7c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="91d7c-112">PARAMETERS</span></span>

### <span data-ttu-id="91d7c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91d7c-113">-AsJob</span></span>
<span data-ttu-id="91d7c-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="91d7c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="91d7c-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="91d7c-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="91d7c-116">Der Ressourcenname der angefügten Datenbankkonfiguration im Nachfolge Cluster.</span><span class="sxs-lookup"><span data-stu-id="91d7c-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="91d7c-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="91d7c-117">-ClusterName</span></span>
<span data-ttu-id="91d7c-118">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="91d7c-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="91d7c-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="91d7c-119">-ClusterResourceId</span></span>
<span data-ttu-id="91d7c-120">Die Ressourcen-ID des Clusters, der einer Datenbank folgt, die diesem Cluster gehört.</span><span class="sxs-lookup"><span data-stu-id="91d7c-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="91d7c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d7c-121">-DefaultProfile</span></span>
<span data-ttu-id="91d7c-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91d7c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d7c-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91d7c-123">-InputObject</span></span>
<span data-ttu-id="91d7c-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="91d7c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91d7c-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="91d7c-125">-NoWait</span></span>
<span data-ttu-id="91d7c-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="91d7c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="91d7c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91d7c-127">-PassThru</span></span>
<span data-ttu-id="91d7c-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="91d7c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="91d7c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91d7c-129">-ResourceGroupName</span></span>
<span data-ttu-id="91d7c-130">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="91d7c-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="91d7c-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="91d7c-131">-SubscriptionId</span></span>
<span data-ttu-id="91d7c-132">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="91d7c-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="91d7c-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="91d7c-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="91d7c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91d7c-134">-Confirm</span></span>
<span data-ttu-id="91d7c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91d7c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d7c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d7c-136">-WhatIf</span></span>
<span data-ttu-id="91d7c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91d7c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91d7c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91d7c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91d7c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d7c-139">CommonParameters</span></span>
<span data-ttu-id="91d7c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d7c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d7c-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91d7c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d7c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91d7c-142">INPUTS</span></span>

### <span data-ttu-id="91d7c-143">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="91d7c-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="91d7c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91d7c-144">OUTPUTS</span></span>

### <span data-ttu-id="91d7c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91d7c-145">System.Boolean</span></span>

## <span data-ttu-id="91d7c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="91d7c-146">NOTES</span></span>

<span data-ttu-id="91d7c-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="91d7c-147">ALIASES</span></span>

<span data-ttu-id="91d7c-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91d7c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91d7c-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91d7c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91d7c-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="91d7c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91d7c-151">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="91d7c-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91d7c-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="91d7c-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="91d7c-153">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="91d7c-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="91d7c-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="91d7c-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="91d7c-155">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="91d7c-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="91d7c-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="91d7c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91d7c-157">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="91d7c-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="91d7c-158">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="91d7c-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="91d7c-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="91d7c-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="91d7c-160">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="91d7c-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="91d7c-161">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="91d7c-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="91d7c-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91d7c-162">RELATED LINKS</span></span>

