---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: b7638780dc4fa360998d7d974d74c93ccd5c2afe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147649"
---
# <span data-ttu-id="02dbb-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="02dbb-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="02dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="02dbb-103">Aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="02dbb-103">Updates a database.</span></span>

## <span data-ttu-id="02dbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02dbb-104">SYNTAX</span></span>

### <span data-ttu-id="02dbb-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="02dbb-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02dbb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="02dbb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02dbb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02dbb-107">DESCRIPTION</span></span>
<span data-ttu-id="02dbb-108">Aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="02dbb-108">Updates a database.</span></span>

## <span data-ttu-id="02dbb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02dbb-109">EXAMPLES</span></span>

### <span data-ttu-id="02dbb-110">Beispiel 1: Aktualisieren einer vorhandenen Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="02dbb-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="02dbb-111">Der obige Befehl aktualisiert den Zeitraum für das weiche Löschen und den Hot-Cache-Zeitraum der "mykustodatabase" der Datenbank "mykustodatabase" im Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="02dbb-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="02dbb-112">Beispiel 2: Aktualisieren einer vorhandenen Datenbank über identität</span><span class="sxs-lookup"><span data-stu-id="02dbb-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="02dbb-113">Der obige Befehl aktualisiert den Zeitraum für das weiche Löschen und den Hot-Cache-Zeitraum der "mykustodatabase" der Datenbank "mykustodatabase" im Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="02dbb-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="02dbb-114">Beispiel 3: Aktualisieren einer vorhandenen "ReadOnly"-Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="02dbb-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="02dbb-115">Der oben aufgeführte Befehl aktualisiert den hot cache period der "mykustodatabase" der Datenbank "mykustodatabase" im Cluster "myfollowercluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="02dbb-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="02dbb-116">Beispiel 4: Aktualisieren einer vorhandenen ReadOnly-Datenbank über Identität</span><span class="sxs-lookup"><span data-stu-id="02dbb-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="02dbb-117">Der oben aufgeführte Befehl aktualisiert den hot cache period der "mykustodatabase" der Datenbank "mykustodatabase" im Cluster "myfollowercluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="02dbb-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="02dbb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02dbb-118">PARAMETERS</span></span>

### <span data-ttu-id="02dbb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02dbb-119">-AsJob</span></span>
<span data-ttu-id="02dbb-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="02dbb-120">Run the command as a job</span></span>

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

### <span data-ttu-id="02dbb-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="02dbb-121">-ClusterName</span></span>
<span data-ttu-id="02dbb-122">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="02dbb-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="02dbb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02dbb-123">-DefaultProfile</span></span>
<span data-ttu-id="02dbb-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02dbb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02dbb-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="02dbb-125">-HotCachePeriod</span></span>
<span data-ttu-id="02dbb-126">Die Zeit, zu der die Daten für schnelle Abfragen in TimeSpan im Cache gespeichert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="02dbb-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="02dbb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02dbb-127">-InputObject</span></span>
<span data-ttu-id="02dbb-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="02dbb-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="02dbb-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="02dbb-129">-Kind</span></span>
<span data-ttu-id="02dbb-130">Art der Datenbank</span><span class="sxs-lookup"><span data-stu-id="02dbb-130">Kind of the database</span></span>

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

### <span data-ttu-id="02dbb-131">-Location</span><span class="sxs-lookup"><span data-stu-id="02dbb-131">-Location</span></span>
<span data-ttu-id="02dbb-132">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="02dbb-132">Resource location.</span></span>

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

### <span data-ttu-id="02dbb-133">-Name</span><span class="sxs-lookup"><span data-stu-id="02dbb-133">-Name</span></span>
<span data-ttu-id="02dbb-134">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="02dbb-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="02dbb-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="02dbb-135">-NoWait</span></span>
<span data-ttu-id="02dbb-136">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="02dbb-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="02dbb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02dbb-137">-ResourceGroupName</span></span>
<span data-ttu-id="02dbb-138">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="02dbb-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="02dbb-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="02dbb-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="02dbb-140">Die Zeit, zu der die Daten gespeichert werden sollten, bevor sie für Abfragen in TimeSpan nicht mehr zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="02dbb-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="02dbb-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02dbb-141">-SubscriptionId</span></span>
<span data-ttu-id="02dbb-142">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="02dbb-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="02dbb-143">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="02dbb-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="02dbb-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02dbb-144">-Confirm</span></span>
<span data-ttu-id="02dbb-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02dbb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02dbb-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="02dbb-146">-WhatIf</span></span>
<span data-ttu-id="02dbb-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02dbb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02dbb-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02dbb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02dbb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02dbb-149">CommonParameters</span></span>
<span data-ttu-id="02dbb-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02dbb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02dbb-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02dbb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02dbb-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02dbb-152">INPUTS</span></span>

### <span data-ttu-id="02dbb-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="02dbb-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="02dbb-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02dbb-154">OUTPUTS</span></span>

### <span data-ttu-id="02dbb-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="02dbb-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="02dbb-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="02dbb-156">NOTES</span></span>

<span data-ttu-id="02dbb-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="02dbb-157">ALIASES</span></span>

<span data-ttu-id="02dbb-158">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="02dbb-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02dbb-159">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02dbb-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02dbb-160">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02dbb-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02dbb-161">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="02dbb-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02dbb-162">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="02dbb-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="02dbb-163">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="02dbb-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="02dbb-164">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="02dbb-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="02dbb-165">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="02dbb-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="02dbb-166">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="02dbb-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02dbb-167">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="02dbb-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="02dbb-168">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="02dbb-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="02dbb-169">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="02dbb-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="02dbb-170">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="02dbb-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="02dbb-171">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="02dbb-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="02dbb-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="02dbb-172">RELATED LINKS</span></span>

