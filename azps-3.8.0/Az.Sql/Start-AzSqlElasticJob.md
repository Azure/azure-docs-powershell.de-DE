---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846532"
---
# <span data-ttu-id="31b80-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="31b80-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="31b80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31b80-102">SYNOPSIS</span></span>
<span data-ttu-id="31b80-103">Startet einen Auftrag und gibt eine Auftrags Ausführungs-ID zurück, die abgefragt werden kann, um den Status anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="31b80-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="31b80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31b80-104">SYNTAX</span></span>

### <span data-ttu-id="31b80-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="31b80-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31b80-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="31b80-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b80-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31b80-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b80-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31b80-108">DESCRIPTION</span></span>
<span data-ttu-id="31b80-109">Das Start-AzSqlElasticJob-Cmdlet startet einen Auftrag, der eine neue Auftragsausführung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="31b80-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="31b80-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31b80-110">EXAMPLES</span></span>

### <span data-ttu-id="31b80-111">Beispiel 1 – startet einen Auftrag, der eine neue Auftragsausführung zurückgibt</span><span class="sxs-lookup"><span data-stu-id="31b80-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="31b80-112">Startet einen Auftrag, der eine neue Auftragsausführung zurückgibt</span><span class="sxs-lookup"><span data-stu-id="31b80-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="31b80-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="31b80-113">PARAMETERS</span></span>

### <span data-ttu-id="31b80-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="31b80-114">-AgentName</span></span>
<span data-ttu-id="31b80-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="31b80-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31b80-116">-AsJob</span></span>
<span data-ttu-id="31b80-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="31b80-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b80-118">-DefaultProfile</span></span>
<span data-ttu-id="31b80-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31b80-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b80-120">-Jobname</span><span class="sxs-lookup"><span data-stu-id="31b80-120">-JobName</span></span>
<span data-ttu-id="31b80-121">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="31b80-121">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="31b80-122">-ParentObject</span></span>
<span data-ttu-id="31b80-123">Das Auftragsobjekt</span><span class="sxs-lookup"><span data-stu-id="31b80-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="31b80-124">-ParentResourceId</span></span>
<span data-ttu-id="31b80-125">Die Projekt Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="31b80-125">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b80-126">-ResourceGroupName</span></span>
<span data-ttu-id="31b80-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="31b80-127">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="31b80-128">-ServerName</span></span>
<span data-ttu-id="31b80-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="31b80-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="31b80-130">-Wait</span></span>
<span data-ttu-id="31b80-131">Das Wait-Flag, um anzugeben, dass gewartet werden soll, bis die Ausführung des Auftrags erfolgt ist</span><span class="sxs-lookup"><span data-stu-id="31b80-131">The wait flag to indicate to wait until the job's execution is done</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b80-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31b80-132">-Confirm</span></span>
<span data-ttu-id="31b80-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31b80-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b80-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b80-134">-WhatIf</span></span>
<span data-ttu-id="31b80-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31b80-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b80-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31b80-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b80-137">CommonParameters</span></span>
<span data-ttu-id="31b80-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b80-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31b80-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b80-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31b80-140">INPUTS</span></span>

### <span data-ttu-id="31b80-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="31b80-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="31b80-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31b80-142">OUTPUTS</span></span>

### <span data-ttu-id="31b80-143">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="31b80-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="31b80-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="31b80-144">NOTES</span></span>

## <span data-ttu-id="31b80-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31b80-145">RELATED LINKS</span></span>
