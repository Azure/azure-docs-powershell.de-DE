---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298603"
---
# <span data-ttu-id="15bc3-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="15bc3-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="15bc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="15bc3-103">Ruft einen oder mehrere Auftragsschritte ab</span><span class="sxs-lookup"><span data-stu-id="15bc3-103">Gets one or more job steps</span></span>

## <span data-ttu-id="15bc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15bc3-104">SYNTAX</span></span>

### <span data-ttu-id="15bc3-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="15bc3-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15bc3-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="15bc3-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15bc3-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="15bc3-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15bc3-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="15bc3-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15bc3-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="15bc3-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15bc3-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="15bc3-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15bc3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15bc3-111">DESCRIPTION</span></span>
<span data-ttu-id="15bc3-112">Das Get-AzSqlElasticJobStep-Cmdlet erhält eine oder mehrere Auftragsschritte aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="15bc3-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="15bc3-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15bc3-113">EXAMPLES</span></span>

### <span data-ttu-id="15bc3-114">Beispiel 1: Ruft einen Auftragsschritt aus einem Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="15bc3-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="15bc3-115">Ruft einen Auftragsschritt aus einem Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="15bc3-115">Gets a job step from a job</span></span>

## <span data-ttu-id="15bc3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15bc3-116">PARAMETERS</span></span>

### <span data-ttu-id="15bc3-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="15bc3-117">-AgentName</span></span>
<span data-ttu-id="15bc3-118">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="15bc3-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bc3-119">-DefaultProfile</span></span>
<span data-ttu-id="15bc3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15bc3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15bc3-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="15bc3-121">-JobName</span></span>
<span data-ttu-id="15bc3-122">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="15bc3-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="15bc3-123">-Name</span></span>
<span data-ttu-id="15bc3-124">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="15bc3-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15bc3-125">-ParentObject</span></span>
<span data-ttu-id="15bc3-126">Das Auftragseingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="15bc3-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="15bc3-127">-ParentResourceId</span></span>
<span data-ttu-id="15bc3-128">Die Auftragsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="15bc3-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15bc3-129">-ResourceGroupName</span></span>
<span data-ttu-id="15bc3-130">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="15bc3-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15bc3-131">-ServerName</span></span>
<span data-ttu-id="15bc3-132">Der Servername</span><span class="sxs-lookup"><span data-stu-id="15bc3-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-133">-Version</span><span class="sxs-lookup"><span data-stu-id="15bc3-133">-Version</span></span>
<span data-ttu-id="15bc3-134">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="15bc3-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bc3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bc3-135">CommonParameters</span></span>
<span data-ttu-id="15bc3-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15bc3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bc3-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15bc3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bc3-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15bc3-138">INPUTS</span></span>

### <span data-ttu-id="15bc3-139">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="15bc3-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="15bc3-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15bc3-140">OUTPUTS</span></span>

### <span data-ttu-id="15bc3-141">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="15bc3-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="15bc3-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15bc3-142">NOTES</span></span>

## <span data-ttu-id="15bc3-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15bc3-143">RELATED LINKS</span></span>
