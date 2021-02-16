---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165820"
---
# <span data-ttu-id="ee1f4-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="ee1f4-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="ee1f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1f4-103">Fügt einem Auftrag einen Auftragsschritt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-103">Adds a job step to a job</span></span>

## <span data-ttu-id="ee1f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee1f4-104">SYNTAX</span></span>

### <span data-ttu-id="ee1f4-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee1f4-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="ee1f4-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="ee1f4-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee1f4-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ee1f4-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ee1f4-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ee1f4-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ee1f4-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1f4-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ee1f4-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1f4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee1f4-114">DESCRIPTION</span></span>
<span data-ttu-id="ee1f4-115">Das Add-AzSqlElasticJobStep Cmdlet fügt einem Auftrag einen Auftragsschritt hinzu</span><span class="sxs-lookup"><span data-stu-id="ee1f4-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="ee1f4-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ee1f4-116">EXAMPLES</span></span>

### <span data-ttu-id="ee1f4-117">Beispiel 1: Fügt einem Auftrag einen Schritt hinzu</span><span class="sxs-lookup"><span data-stu-id="ee1f4-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="ee1f4-118">Fügt einem Auftrag einen Auftragsschritt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-118">Adds a job step to a job</span></span>

## <span data-ttu-id="ee1f4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee1f4-119">PARAMETERS</span></span>

### <span data-ttu-id="ee1f4-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-120">-AgentName</span></span>
<span data-ttu-id="ee1f4-121">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="ee1f4-121">The agent name</span></span>

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

### <span data-ttu-id="ee1f4-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="ee1f4-122">-CommandText</span></span>
<span data-ttu-id="ee1f4-123">Der Befehlstext</span><span class="sxs-lookup"><span data-stu-id="ee1f4-123">The command text</span></span>

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

### <span data-ttu-id="ee1f4-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-124">-CredentialName</span></span>
<span data-ttu-id="ee1f4-125">Der Name der Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="ee1f4-125">The credential name</span></span>

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

### <span data-ttu-id="ee1f4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1f4-126">-DefaultProfile</span></span>
<span data-ttu-id="ee1f4-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1f4-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ee1f4-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="ee1f4-129">Die Sekunden für die anfängliche Wiederholungsintervalle</span><span class="sxs-lookup"><span data-stu-id="ee1f4-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="ee1f4-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-130">-JobName</span></span>
<span data-ttu-id="ee1f4-131">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="ee1f4-131">The job name</span></span>

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

### <span data-ttu-id="ee1f4-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ee1f4-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="ee1f4-133">Das maximale Wiederholungsintervall in Sekunden</span><span class="sxs-lookup"><span data-stu-id="ee1f4-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="ee1f4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ee1f4-134">-Name</span></span>
<span data-ttu-id="ee1f4-135">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="ee1f4-135">The job step name</span></span>

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

### <span data-ttu-id="ee1f4-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-136">-OutputCredentialName</span></span>
<span data-ttu-id="ee1f4-137">Der Name der Ausgabeanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="ee1f4-137">The output credential name</span></span>

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

### <span data-ttu-id="ee1f4-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ee1f4-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="ee1f4-139">Das Ausgabedatenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="ee1f4-139">The output database object</span></span>

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

### <span data-ttu-id="ee1f4-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ee1f4-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="ee1f4-141">Die Ressourcen-ID der Ausgabedatenbank</span><span class="sxs-lookup"><span data-stu-id="ee1f4-141">The output database resource id</span></span>

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

### <span data-ttu-id="ee1f4-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-142">-OutputSchemaName</span></span>
<span data-ttu-id="ee1f4-143">Der Name des Ausgabeschemas</span><span class="sxs-lookup"><span data-stu-id="ee1f4-143">The output schema name</span></span>

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

### <span data-ttu-id="ee1f4-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-144">-OutputTableName</span></span>
<span data-ttu-id="ee1f4-145">Der Name der Ausgabetabelle</span><span class="sxs-lookup"><span data-stu-id="ee1f4-145">The output table name</span></span>

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

### <span data-ttu-id="ee1f4-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ee1f4-146">-ParentObject</span></span>
<span data-ttu-id="ee1f4-147">Das Auftragsobjekt</span><span class="sxs-lookup"><span data-stu-id="ee1f4-147">The job object</span></span>

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

### <span data-ttu-id="ee1f4-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ee1f4-148">-ParentResourceId</span></span>
<span data-ttu-id="ee1f4-149">Die Auftragsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ee1f4-149">The job resource id</span></span>

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

### <span data-ttu-id="ee1f4-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-150">-ResourceGroupName</span></span>
<span data-ttu-id="ee1f4-151">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ee1f4-151">The resource group name</span></span>

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

### <span data-ttu-id="ee1f4-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="ee1f4-152">-RetryAttempts</span></span>
<span data-ttu-id="ee1f4-153">Die Wiederholungsversuche</span><span class="sxs-lookup"><span data-stu-id="ee1f4-153">The retry attempts</span></span>

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

### <span data-ttu-id="ee1f4-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="ee1f4-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="ee1f4-155">Das Wiederholungsintervall deaktiviert den Multiplikator</span><span class="sxs-lookup"><span data-stu-id="ee1f4-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="ee1f4-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-156">-ServerName</span></span>
<span data-ttu-id="ee1f4-157">Der Servername</span><span class="sxs-lookup"><span data-stu-id="ee1f4-157">The server name</span></span>

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

### <span data-ttu-id="ee1f4-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="ee1f4-158">-StepId</span></span>
<span data-ttu-id="ee1f4-159">Die Schritt-ID</span><span class="sxs-lookup"><span data-stu-id="ee1f4-159">The step id</span></span>

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

### <span data-ttu-id="ee1f4-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1f4-160">-TargetGroupName</span></span>
<span data-ttu-id="ee1f4-161">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="ee1f4-161">The target group name</span></span>

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

### <span data-ttu-id="ee1f4-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="ee1f4-162">-TimeoutSeconds</span></span>
<span data-ttu-id="ee1f4-163">Die Sekunden für das Zeit out</span><span class="sxs-lookup"><span data-stu-id="ee1f4-163">The time out seconds</span></span>

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

### <span data-ttu-id="ee1f4-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee1f4-164">-Confirm</span></span>
<span data-ttu-id="ee1f4-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1f4-166">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ee1f4-166">-WhatIf</span></span>
<span data-ttu-id="ee1f4-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1f4-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1f4-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1f4-169">CommonParameters</span></span>
<span data-ttu-id="ee1f4-170">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1f4-171">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee1f4-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1f4-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ee1f4-172">INPUTS</span></span>

### <span data-ttu-id="ee1f4-173">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="ee1f4-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ee1f4-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ee1f4-174">OUTPUTS</span></span>

### <span data-ttu-id="ee1f4-175">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="ee1f4-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ee1f4-176">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ee1f4-176">NOTES</span></span>

## <span data-ttu-id="ee1f4-177">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ee1f4-177">RELATED LINKS</span></span>
