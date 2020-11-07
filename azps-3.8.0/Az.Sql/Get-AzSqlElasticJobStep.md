---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 2b202fd2cff8ae12425c1e41807126798eb9944e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847436"
---
# <span data-ttu-id="12a04-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="12a04-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="12a04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12a04-102">SYNOPSIS</span></span>
<span data-ttu-id="12a04-103">Ruft mindestens einen Auftragsschritt ab.</span><span class="sxs-lookup"><span data-stu-id="12a04-103">Gets one or more job steps</span></span>

## <span data-ttu-id="12a04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a04-104">SYNTAX</span></span>

### <span data-ttu-id="12a04-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="12a04-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a04-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="12a04-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12a04-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="12a04-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a04-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="12a04-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a04-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12a04-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a04-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="12a04-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a04-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12a04-111">DESCRIPTION</span></span>
<span data-ttu-id="12a04-112">Das Get-AzSqlElasticJobStep-Cmdlet ruft einen oder mehrere Auftragsschritte von einem Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="12a04-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="12a04-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12a04-113">EXAMPLES</span></span>

### <span data-ttu-id="12a04-114">Beispiel 1 – Ruft einen Auftragsschritt von einem Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="12a04-114">Example 1 - Gets a job step from a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="12a04-115">Ruft einen Auftragsschritt aus einem Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="12a04-115">Gets a job step from a job</span></span>

## <span data-ttu-id="12a04-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="12a04-116">PARAMETERS</span></span>

### <span data-ttu-id="12a04-117">-Agentname</span><span class="sxs-lookup"><span data-stu-id="12a04-117">-AgentName</span></span>
<span data-ttu-id="12a04-118">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="12a04-118">The agent name</span></span>

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

### <span data-ttu-id="12a04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a04-119">-DefaultProfile</span></span>
<span data-ttu-id="12a04-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12a04-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a04-121">-Jobname</span><span class="sxs-lookup"><span data-stu-id="12a04-121">-JobName</span></span>
<span data-ttu-id="12a04-122">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="12a04-122">The job name</span></span>

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

### <span data-ttu-id="12a04-123">-Name</span><span class="sxs-lookup"><span data-stu-id="12a04-123">-Name</span></span>
<span data-ttu-id="12a04-124">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="12a04-124">The job step name</span></span>

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

### <span data-ttu-id="12a04-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="12a04-125">-ParentObject</span></span>
<span data-ttu-id="12a04-126">Das Auftragseingabe Objekt</span><span class="sxs-lookup"><span data-stu-id="12a04-126">The job input object</span></span>

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

### <span data-ttu-id="12a04-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="12a04-127">-ParentResourceId</span></span>
<span data-ttu-id="12a04-128">Die Projekt Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="12a04-128">The job resource id</span></span>

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

### <span data-ttu-id="12a04-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a04-129">-ResourceGroupName</span></span>
<span data-ttu-id="12a04-130">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12a04-130">The resource group name</span></span>

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

### <span data-ttu-id="12a04-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="12a04-131">-ServerName</span></span>
<span data-ttu-id="12a04-132">Der Servername</span><span class="sxs-lookup"><span data-stu-id="12a04-132">The server name</span></span>

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

### <span data-ttu-id="12a04-133">-Version</span><span class="sxs-lookup"><span data-stu-id="12a04-133">-Version</span></span>
<span data-ttu-id="12a04-134">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="12a04-134">The job step name</span></span>

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

### <span data-ttu-id="12a04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a04-135">CommonParameters</span></span>
<span data-ttu-id="12a04-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a04-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12a04-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a04-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12a04-138">INPUTS</span></span>

### <span data-ttu-id="12a04-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="12a04-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="12a04-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12a04-140">OUTPUTS</span></span>

### <span data-ttu-id="12a04-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="12a04-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="12a04-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="12a04-142">NOTES</span></span>

## <span data-ttu-id="12a04-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12a04-143">RELATED LINKS</span></span>
