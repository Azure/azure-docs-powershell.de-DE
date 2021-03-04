---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 76e712a881c88490a71933056f82fe1959df2948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920536"
---
# <span data-ttu-id="7fdf0-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="7fdf0-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="7fdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdf0-103">Aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-103">Updates a database.</span></span>

## <span data-ttu-id="7fdf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fdf0-104">SYNTAX</span></span>

### <span data-ttu-id="7fdf0-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7fdf0-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7fdf0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7fdf0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7fdf0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fdf0-107">DESCRIPTION</span></span>
<span data-ttu-id="7fdf0-108">Aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-108">Updates a database.</span></span>

## <span data-ttu-id="7fdf0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7fdf0-109">EXAMPLES</span></span>

### <span data-ttu-id="7fdf0-110">Beispiel 1: Aktualisieren einer vorhandenen Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="7fdf0-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="7fdf0-111">Mit dem oben genannten Befehl wird der Zeitraum für die weiche Löschung und der Zwischenspeicherzeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "testnewkustocluster" aktualisiert, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="7fdf0-112">Beispiel 2: Aktualisieren einer vorhandenen Datenbank über die Identität</span><span class="sxs-lookup"><span data-stu-id="7fdf0-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="7fdf0-113">Mit dem oben genannten Befehl wird der Zeitraum für die weiche Löschung und der Zwischenspeicherzeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "testnewkustocluster" aktualisiert, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="7fdf0-114">Beispiel 3: Aktualisieren einer vorhandenen ReadOnly-Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="7fdf0-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="7fdf0-115">Der obige Befehl aktualisiert den heißen Cachezeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "myfollowercluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="7fdf0-116">Beispiel 4: Aktualisieren einer vorhandenen ReadOnly-Datenbank über die Identität</span><span class="sxs-lookup"><span data-stu-id="7fdf0-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="7fdf0-117">Der obige Befehl aktualisiert den heißen Cachezeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "myfollowercluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="7fdf0-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7fdf0-118">PARAMETERS</span></span>

### <span data-ttu-id="7fdf0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fdf0-119">-AsJob</span></span>
<span data-ttu-id="7fdf0-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7fdf0-120">Run the command as a job</span></span>

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

### <span data-ttu-id="7fdf0-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7fdf0-121">-ClusterName</span></span>
<span data-ttu-id="7fdf0-122">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7fdf0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fdf0-123">-DefaultProfile</span></span>
<span data-ttu-id="7fdf0-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fdf0-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="7fdf0-125">-HotCachePeriod</span></span>
<span data-ttu-id="7fdf0-126">Die Zeit, zu der die Daten im Cache für schnelle Abfragen in TimeSpan gespeichert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdf0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fdf0-127">-InputObject</span></span>
<span data-ttu-id="7fdf0-128">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdf0-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="7fdf0-129">-Kind</span></span>
<span data-ttu-id="7fdf0-130">Art der Datenbank</span><span class="sxs-lookup"><span data-stu-id="7fdf0-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdf0-131">-Location</span><span class="sxs-lookup"><span data-stu-id="7fdf0-131">-Location</span></span>
<span data-ttu-id="7fdf0-132">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-132">Resource location.</span></span>

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

### <span data-ttu-id="7fdf0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="7fdf0-133">-Name</span></span>
<span data-ttu-id="7fdf0-134">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdf0-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7fdf0-135">-NoWait</span></span>
<span data-ttu-id="7fdf0-136">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7fdf0-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7fdf0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fdf0-137">-ResourceGroupName</span></span>
<span data-ttu-id="7fdf0-138">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7fdf0-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="7fdf0-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="7fdf0-140">Die Zeit, zu der die Daten aufbewahrt werden sollten, bevor sie für Abfragen in TimeSpan nicht mehr zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdf0-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fdf0-141">-SubscriptionId</span></span>
<span data-ttu-id="7fdf0-142">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7fdf0-143">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7fdf0-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7fdf0-144">-Confirm</span></span>
<span data-ttu-id="7fdf0-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fdf0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fdf0-146">-WhatIf</span></span>
<span data-ttu-id="7fdf0-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fdf0-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fdf0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdf0-149">CommonParameters</span></span>
<span data-ttu-id="7fdf0-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdf0-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fdf0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdf0-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7fdf0-152">INPUTS</span></span>

### <span data-ttu-id="7fdf0-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7fdf0-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7fdf0-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7fdf0-154">OUTPUTS</span></span>

### <span data-ttu-id="7fdf0-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="7fdf0-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="7fdf0-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7fdf0-156">NOTES</span></span>

<span data-ttu-id="7fdf0-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7fdf0-157">ALIASES</span></span>

<span data-ttu-id="7fdf0-158">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7fdf0-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fdf0-159">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fdf0-160">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fdf0-161">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="7fdf0-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fdf0-162">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7fdf0-163">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7fdf0-164">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7fdf0-165">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7fdf0-166">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7fdf0-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fdf0-167">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7fdf0-168">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7fdf0-169">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7fdf0-170">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7fdf0-171">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="7fdf0-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7fdf0-172">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7fdf0-172">RELATED LINKS</span></span>

