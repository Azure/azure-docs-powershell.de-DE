---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 60dac0ad09f30f339da82d84cf6200a44fe11859
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996217"
---
# <span data-ttu-id="85d07-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="85d07-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="85d07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85d07-102">SYNOPSIS</span></span>
<span data-ttu-id="85d07-103">Ruft einen oder mehrere Aufträge ab</span><span class="sxs-lookup"><span data-stu-id="85d07-103">Gets one or more jobs</span></span>

## <span data-ttu-id="85d07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85d07-104">SYNTAX</span></span>

### <span data-ttu-id="85d07-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="85d07-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85d07-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="85d07-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85d07-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="85d07-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85d07-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85d07-108">DESCRIPTION</span></span>
<span data-ttu-id="85d07-109">Das Get-AzSqlElasticJob-Cmdlet ruft einen oder mehrere Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="85d07-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="85d07-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85d07-110">EXAMPLES</span></span>

### <span data-ttu-id="85d07-111">Beispiel 1 – Ruft einen Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="85d07-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="85d07-112">Ruft einen Job ab</span><span class="sxs-lookup"><span data-stu-id="85d07-112">Gets a job</span></span>

## <span data-ttu-id="85d07-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="85d07-113">PARAMETERS</span></span>

### <span data-ttu-id="85d07-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="85d07-114">-AgentName</span></span>
<span data-ttu-id="85d07-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="85d07-115">The agent name</span></span>

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

### <span data-ttu-id="85d07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d07-116">-DefaultProfile</span></span>
<span data-ttu-id="85d07-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85d07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85d07-118">-Name</span><span class="sxs-lookup"><span data-stu-id="85d07-118">-Name</span></span>
<span data-ttu-id="85d07-119">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="85d07-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d07-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="85d07-120">-ParentObject</span></span>
<span data-ttu-id="85d07-121">Das Eingabeobjekt des Agents</span><span class="sxs-lookup"><span data-stu-id="85d07-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85d07-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="85d07-122">-ParentResourceId</span></span>
<span data-ttu-id="85d07-123">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="85d07-123">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d07-124">-ResourceGroupName</span></span>
<span data-ttu-id="85d07-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="85d07-125">The resource group name</span></span>

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

### <span data-ttu-id="85d07-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="85d07-126">-ServerName</span></span>
<span data-ttu-id="85d07-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="85d07-127">The server name</span></span>

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

### <span data-ttu-id="85d07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d07-128">CommonParameters</span></span>
<span data-ttu-id="85d07-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d07-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85d07-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d07-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85d07-131">INPUTS</span></span>

### <span data-ttu-id="85d07-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="85d07-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="85d07-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85d07-133">OUTPUTS</span></span>

### <span data-ttu-id="85d07-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="85d07-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="85d07-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="85d07-135">NOTES</span></span>

## <span data-ttu-id="85d07-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85d07-136">RELATED LINKS</span></span>
