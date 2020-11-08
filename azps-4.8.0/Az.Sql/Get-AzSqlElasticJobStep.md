---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166828"
---
# <span data-ttu-id="4eae4-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="4eae4-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="4eae4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4eae4-102">SYNOPSIS</span></span>
<span data-ttu-id="4eae4-103">Ruft mindestens einen Auftragsschritt ab.</span><span class="sxs-lookup"><span data-stu-id="4eae4-103">Gets one or more job steps</span></span>

## <span data-ttu-id="4eae4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eae4-104">SYNTAX</span></span>

### <span data-ttu-id="4eae4-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="4eae4-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eae4-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="4eae4-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eae4-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4eae4-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eae4-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="4eae4-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eae4-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4eae4-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eae4-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4eae4-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eae4-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4eae4-111">DESCRIPTION</span></span>
<span data-ttu-id="4eae4-112">Das Get-AzSqlElasticJobStep-Cmdlet ruft einen oder mehrere Auftragsschritte von einem Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="4eae4-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="4eae4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4eae4-113">EXAMPLES</span></span>

### <span data-ttu-id="4eae4-114">Beispiel 1: Abrufen eines Auftragsschritts aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="4eae4-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="4eae4-115">Ruft einen Auftragsschritt aus einem Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="4eae4-115">Gets a job step from a job</span></span>

## <span data-ttu-id="4eae4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eae4-116">PARAMETERS</span></span>

### <span data-ttu-id="4eae4-117">-Agentname</span><span class="sxs-lookup"><span data-stu-id="4eae4-117">-AgentName</span></span>
<span data-ttu-id="4eae4-118">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="4eae4-118">The agent name</span></span>

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

### <span data-ttu-id="4eae4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eae4-119">-DefaultProfile</span></span>
<span data-ttu-id="4eae4-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4eae4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eae4-121">-Jobname</span><span class="sxs-lookup"><span data-stu-id="4eae4-121">-JobName</span></span>
<span data-ttu-id="4eae4-122">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="4eae4-122">The job name</span></span>

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

### <span data-ttu-id="4eae4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4eae4-123">-Name</span></span>
<span data-ttu-id="4eae4-124">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="4eae4-124">The job step name</span></span>

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

### <span data-ttu-id="4eae4-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4eae4-125">-ParentObject</span></span>
<span data-ttu-id="4eae4-126">Das Auftragseingabe Objekt</span><span class="sxs-lookup"><span data-stu-id="4eae4-126">The job input object</span></span>

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

### <span data-ttu-id="4eae4-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4eae4-127">-ParentResourceId</span></span>
<span data-ttu-id="4eae4-128">Die Projekt Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4eae4-128">The job resource id</span></span>

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

### <span data-ttu-id="4eae4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eae4-129">-ResourceGroupName</span></span>
<span data-ttu-id="4eae4-130">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4eae4-130">The resource group name</span></span>

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

### <span data-ttu-id="4eae4-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="4eae4-131">-ServerName</span></span>
<span data-ttu-id="4eae4-132">Der Servername</span><span class="sxs-lookup"><span data-stu-id="4eae4-132">The server name</span></span>

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

### <span data-ttu-id="4eae4-133">-Version</span><span class="sxs-lookup"><span data-stu-id="4eae4-133">-Version</span></span>
<span data-ttu-id="4eae4-134">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="4eae4-134">The job step name</span></span>

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

### <span data-ttu-id="4eae4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eae4-135">CommonParameters</span></span>
<span data-ttu-id="4eae4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eae4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eae4-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eae4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eae4-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4eae4-138">INPUTS</span></span>

### <span data-ttu-id="4eae4-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="4eae4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4eae4-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4eae4-140">OUTPUTS</span></span>

### <span data-ttu-id="4eae4-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4eae4-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4eae4-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4eae4-142">NOTES</span></span>

## <span data-ttu-id="4eae4-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4eae4-143">RELATED LINKS</span></span>
