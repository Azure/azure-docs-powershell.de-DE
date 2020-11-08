---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177921"
---
# <span data-ttu-id="c3357-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c3357-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="c3357-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3357-102">SYNOPSIS</span></span>
<span data-ttu-id="c3357-103">Aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c3357-103">Updates a database.</span></span>

## <span data-ttu-id="c3357-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3357-104">SYNTAX</span></span>

### <span data-ttu-id="c3357-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3357-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3357-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c3357-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3357-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3357-107">DESCRIPTION</span></span>
<span data-ttu-id="c3357-108">Aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c3357-108">Updates a database.</span></span>

## <span data-ttu-id="c3357-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3357-109">EXAMPLES</span></span>

### <span data-ttu-id="c3357-110">Beispiel 1: Aktualisieren einer vorhandenen Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="c3357-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c3357-111">Der obige Befehl aktualisiert den Soft-Deletion-Zeitraum und den Hot-Cache-Zeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c3357-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c3357-112">Beispiel 2: Aktualisieren einer vorhandenen Datenbank über die Identität</span><span class="sxs-lookup"><span data-stu-id="c3357-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c3357-113">Der obige Befehl aktualisiert den Soft-Deletion-Zeitraum und den Hot-Cache-Zeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c3357-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c3357-114">Beispiel 3: Aktualisieren einer vorhandenen ReadOnly-Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="c3357-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c3357-115">Der obige Befehl aktualisiert den Hot-Cache-Zeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "myfollowercluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c3357-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c3357-116">Beispiel 4: Aktualisieren einer vorhandenen ReadOnly-Datenbank über Identity</span><span class="sxs-lookup"><span data-stu-id="c3357-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c3357-117">Der obige Befehl aktualisiert den Hot-Cache-Zeitraum der Kusto-Datenbank "mykustodatabase" im Cluster "myfollowercluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c3357-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c3357-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3357-118">PARAMETERS</span></span>

### <span data-ttu-id="c3357-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3357-119">-AsJob</span></span>
<span data-ttu-id="c3357-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c3357-120">Run the command as a job</span></span>

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

### <span data-ttu-id="c3357-121">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c3357-121">-ClusterName</span></span>
<span data-ttu-id="c3357-122">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="c3357-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c3357-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3357-123">-DefaultProfile</span></span>
<span data-ttu-id="c3357-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3357-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3357-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="c3357-125">-HotCachePeriod</span></span>
<span data-ttu-id="c3357-126">Der Zeitpunkt, zu dem die Daten im Cache für schnelle Abfragen in TimeSpan aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3357-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="c3357-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3357-127">-InputObject</span></span>
<span data-ttu-id="c3357-128">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c3357-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c3357-129">-Art</span><span class="sxs-lookup"><span data-stu-id="c3357-129">-Kind</span></span>
<span data-ttu-id="c3357-130">Art der Datenbank</span><span class="sxs-lookup"><span data-stu-id="c3357-130">Kind of the database</span></span>

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

### <span data-ttu-id="c3357-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="c3357-131">-Location</span></span>
<span data-ttu-id="c3357-132">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="c3357-132">Resource location.</span></span>

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

### <span data-ttu-id="c3357-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c3357-133">-Name</span></span>
<span data-ttu-id="c3357-134">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="c3357-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c3357-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c3357-135">-NoWait</span></span>
<span data-ttu-id="c3357-136">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c3357-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3357-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3357-137">-ResourceGroupName</span></span>
<span data-ttu-id="c3357-138">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="c3357-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c3357-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="c3357-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="c3357-140">Der Zeitpunkt, zu dem die Daten aufbewahrt werden sollen, bevor Sie nicht mehr auf Abfragen in TimeSpan zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="c3357-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="c3357-141">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c3357-141">-SubscriptionId</span></span>
<span data-ttu-id="c3357-142">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c3357-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c3357-143">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c3357-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c3357-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3357-144">-Confirm</span></span>
<span data-ttu-id="c3357-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3357-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3357-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3357-146">-WhatIf</span></span>
<span data-ttu-id="c3357-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3357-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3357-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3357-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3357-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3357-149">CommonParameters</span></span>
<span data-ttu-id="c3357-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3357-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3357-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3357-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3357-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3357-152">INPUTS</span></span>

### <span data-ttu-id="c3357-153">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c3357-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c3357-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3357-154">OUTPUTS</span></span>

### <span data-ttu-id="c3357-155">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="c3357-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="c3357-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3357-156">NOTES</span></span>

<span data-ttu-id="c3357-157">Aliase</span><span class="sxs-lookup"><span data-stu-id="c3357-157">ALIASES</span></span>

<span data-ttu-id="c3357-158">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3357-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3357-159">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3357-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3357-160">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c3357-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3357-161">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c3357-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3357-162">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3357-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c3357-163">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="c3357-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c3357-164">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="c3357-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c3357-165">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="c3357-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c3357-166">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c3357-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3357-167">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="c3357-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c3357-168">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c3357-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c3357-169">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="c3357-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c3357-170">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c3357-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c3357-171">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c3357-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c3357-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3357-172">RELATED LINKS</span></span>

