---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 83d5733144c07c229cf8b5321ee9d3417ab112ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825948"
---
# <span data-ttu-id="9413d-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="9413d-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="9413d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9413d-102">SYNOPSIS</span></span>
<span data-ttu-id="9413d-103">Entfernt den Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="9413d-103">Removes the job step</span></span>

## <span data-ttu-id="9413d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9413d-104">SYNTAX</span></span>

### <span data-ttu-id="9413d-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="9413d-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9413d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9413d-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9413d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9413d-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9413d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9413d-108">DESCRIPTION</span></span>
<span data-ttu-id="9413d-109">Das Remove-AzSqlElasticJobStep-Cmdlet entfernt einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="9413d-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="9413d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9413d-110">EXAMPLES</span></span>

### <span data-ttu-id="9413d-111">Beispiel 1: entfernt einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="9413d-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="9413d-112">Entfernt einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="9413d-112">Removes a job step from a job</span></span>

## <span data-ttu-id="9413d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9413d-113">PARAMETERS</span></span>

### <span data-ttu-id="9413d-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="9413d-114">-AgentName</span></span>
<span data-ttu-id="9413d-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="9413d-115">The agent name</span></span>

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

### <span data-ttu-id="9413d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9413d-116">-DefaultProfile</span></span>
<span data-ttu-id="9413d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9413d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9413d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9413d-118">-InputObject</span></span>
<span data-ttu-id="9413d-119">Das Eingabeobjekt des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="9413d-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9413d-120">-Jobname</span><span class="sxs-lookup"><span data-stu-id="9413d-120">-JobName</span></span>
<span data-ttu-id="9413d-121">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="9413d-121">The job name</span></span>

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

### <span data-ttu-id="9413d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9413d-122">-Name</span></span>
<span data-ttu-id="9413d-123">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="9413d-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9413d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9413d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9413d-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9413d-125">The resource group name</span></span>

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

### <span data-ttu-id="9413d-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9413d-126">-ResourceId</span></span>
<span data-ttu-id="9413d-127">Die Ressourcen-ID des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="9413d-127">The job step resource id</span></span>

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

### <span data-ttu-id="9413d-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="9413d-128">-ServerName</span></span>
<span data-ttu-id="9413d-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="9413d-129">The server name</span></span>

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

### <span data-ttu-id="9413d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9413d-130">-Confirm</span></span>
<span data-ttu-id="9413d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9413d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9413d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9413d-132">-WhatIf</span></span>
<span data-ttu-id="9413d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9413d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9413d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9413d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9413d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9413d-135">CommonParameters</span></span>
<span data-ttu-id="9413d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9413d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9413d-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9413d-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9413d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9413d-138">INPUTS</span></span>

### <span data-ttu-id="9413d-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="9413d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="9413d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9413d-140">OUTPUTS</span></span>

### <span data-ttu-id="9413d-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="9413d-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="9413d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="9413d-142">NOTES</span></span>

## <span data-ttu-id="9413d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9413d-143">RELATED LINKS</span></span>
