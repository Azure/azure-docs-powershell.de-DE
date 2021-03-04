---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 41314cb2a65912e2973e91b27036fc099d2cbca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923384"
---
# <span data-ttu-id="d8c9d-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="d8c9d-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="d8c9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c9d-103">Fügt einem Auftrag einen Auftragsschritt hinzu</span><span class="sxs-lookup"><span data-stu-id="d8c9d-103">Adds a job step to a job</span></span>

## <span data-ttu-id="d8c9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8c9d-104">SYNTAX</span></span>

### <span data-ttu-id="d8c9d-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8c9d-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="d8c9d-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="d8c9d-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d8c9d-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d8c9d-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d8c9d-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d8c9d-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c9d-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c9d-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c9d-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c9d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8c9d-114">DESCRIPTION</span></span>
<span data-ttu-id="d8c9d-115">Das Add-AzSqlElasticJobStep-Cmdlet fügt einem Auftrag einen Auftragsschritt hinzu</span><span class="sxs-lookup"><span data-stu-id="d8c9d-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="d8c9d-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8c9d-116">EXAMPLES</span></span>

### <span data-ttu-id="d8c9d-117">Beispiel 1: Fügt einem Auftrag einen Schritt hinzu</span><span class="sxs-lookup"><span data-stu-id="d8c9d-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="d8c9d-118">Fügt einem Auftrag einen Auftragsschritt hinzu</span><span class="sxs-lookup"><span data-stu-id="d8c9d-118">Adds a job step to a job</span></span>

## <span data-ttu-id="d8c9d-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d8c9d-119">PARAMETERS</span></span>

### <span data-ttu-id="d8c9d-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-120">-AgentName</span></span>
<span data-ttu-id="d8c9d-121">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="d8c9d-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="d8c9d-122">-CommandText</span></span>
<span data-ttu-id="d8c9d-123">Der Befehlstext</span><span class="sxs-lookup"><span data-stu-id="d8c9d-123">The command text</span></span>

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

### <span data-ttu-id="d8c9d-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-124">-CredentialName</span></span>
<span data-ttu-id="d8c9d-125">Der Name der Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d8c9d-125">The credential name</span></span>

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

### <span data-ttu-id="d8c9d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c9d-126">-DefaultProfile</span></span>
<span data-ttu-id="d8c9d-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8c9d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="d8c9d-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="d8c9d-129">Die ersten Sekunden des Wiederholungsintervalls</span><span class="sxs-lookup"><span data-stu-id="d8c9d-129">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-130">-JobName</span></span>
<span data-ttu-id="d8c9d-131">Der Auftragsname</span><span class="sxs-lookup"><span data-stu-id="d8c9d-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="d8c9d-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="d8c9d-133">Das maximale Wiederholungsintervall (Sekunden)</span><span class="sxs-lookup"><span data-stu-id="d8c9d-133">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d8c9d-134">-Name</span></span>
<span data-ttu-id="d8c9d-135">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="d8c9d-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-136">-OutputCredentialName</span></span>
<span data-ttu-id="d8c9d-137">Der Name der Ausgabeanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d8c9d-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d8c9d-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="d8c9d-139">Das Ausgabedatenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="d8c9d-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c9d-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="d8c9d-141">Die Ressourcen-ID der Ausgabedatenbank</span><span class="sxs-lookup"><span data-stu-id="d8c9d-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-142">-OutputSchemaName</span></span>
<span data-ttu-id="d8c9d-143">Der Name des Ausgabeschemas</span><span class="sxs-lookup"><span data-stu-id="d8c9d-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-144">-OutputTableName</span></span>
<span data-ttu-id="d8c9d-145">Der Name der Ausgabetabelle</span><span class="sxs-lookup"><span data-stu-id="d8c9d-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d8c9d-146">-ParentObject</span></span>
<span data-ttu-id="d8c9d-147">Das Auftragsobjekt</span><span class="sxs-lookup"><span data-stu-id="d8c9d-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c9d-148">-ParentResourceId</span></span>
<span data-ttu-id="d8c9d-149">Die Auftragsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d8c9d-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-150">-ResourceGroupName</span></span>
<span data-ttu-id="d8c9d-151">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d8c9d-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="d8c9d-152">-RetryAttempts</span></span>
<span data-ttu-id="d8c9d-153">Die Wiederholungsversuche</span><span class="sxs-lookup"><span data-stu-id="d8c9d-153">The retry attempts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="d8c9d-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="d8c9d-155">Das Wiederholungsintervall zurück vom Multiplikator</span><span class="sxs-lookup"><span data-stu-id="d8c9d-155">The retry interval back off multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-156">-Servername</span><span class="sxs-lookup"><span data-stu-id="d8c9d-156">-ServerName</span></span>
<span data-ttu-id="d8c9d-157">Der Servername</span><span class="sxs-lookup"><span data-stu-id="d8c9d-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="d8c9d-158">-StepId</span></span>
<span data-ttu-id="d8c9d-159">Die Schritt-ID</span><span class="sxs-lookup"><span data-stu-id="d8c9d-159">The step id</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c9d-160">-TargetGroupName</span></span>
<span data-ttu-id="d8c9d-161">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="d8c9d-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="d8c9d-162">-TimeoutSeconds</span></span>
<span data-ttu-id="d8c9d-163">Die Auszeit (Sekunden)</span><span class="sxs-lookup"><span data-stu-id="d8c9d-163">The time out seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8c9d-164">-Confirm</span></span>
<span data-ttu-id="d8c9d-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8c9d-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c9d-166">-WhatIf</span></span>
<span data-ttu-id="d8c9d-167">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8c9d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c9d-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8c9d-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c9d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c9d-169">CommonParameters</span></span>
<span data-ttu-id="d8c9d-170">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c9d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c9d-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8c9d-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c9d-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8c9d-172">INPUTS</span></span>

### <span data-ttu-id="d8c9d-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="d8c9d-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="d8c9d-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8c9d-174">OUTPUTS</span></span>

### <span data-ttu-id="d8c9d-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="d8c9d-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="d8c9d-176">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d8c9d-176">NOTES</span></span>

## <span data-ttu-id="d8c9d-177">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d8c9d-177">RELATED LINKS</span></span>
