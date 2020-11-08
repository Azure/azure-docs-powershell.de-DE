---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166019"
---
# <span data-ttu-id="de957-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="de957-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="de957-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de957-102">SYNOPSIS</span></span>
<span data-ttu-id="de957-103">Entfernt den Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="de957-103">Removes the job step</span></span>

## <span data-ttu-id="de957-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de957-104">SYNTAX</span></span>

### <span data-ttu-id="de957-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="de957-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de957-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="de957-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de957-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="de957-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de957-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de957-108">DESCRIPTION</span></span>
<span data-ttu-id="de957-109">Das Remove-AzSqlElasticJobStep-Cmdlet entfernt einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="de957-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="de957-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de957-110">EXAMPLES</span></span>

### <span data-ttu-id="de957-111">Beispiel 1: Entfernen eines Auftragsschritts aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="de957-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="de957-112">Entfernt einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="de957-112">Removes a job step from a job</span></span>

### <span data-ttu-id="de957-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="de957-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="de957-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="de957-114">PARAMETERS</span></span>

### <span data-ttu-id="de957-115">-Agentname</span><span class="sxs-lookup"><span data-stu-id="de957-115">-AgentName</span></span>
<span data-ttu-id="de957-116">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="de957-116">The agent name</span></span>

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

### <span data-ttu-id="de957-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de957-117">-DefaultProfile</span></span>
<span data-ttu-id="de957-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de957-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de957-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de957-119">-InputObject</span></span>
<span data-ttu-id="de957-120">Das Eingabeobjekt des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="de957-120">The job step input object</span></span>

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

### <span data-ttu-id="de957-121">-Jobname</span><span class="sxs-lookup"><span data-stu-id="de957-121">-JobName</span></span>
<span data-ttu-id="de957-122">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="de957-122">The job name</span></span>

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

### <span data-ttu-id="de957-123">-Name</span><span class="sxs-lookup"><span data-stu-id="de957-123">-Name</span></span>
<span data-ttu-id="de957-124">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="de957-124">The job step name</span></span>

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

### <span data-ttu-id="de957-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de957-125">-ResourceGroupName</span></span>
<span data-ttu-id="de957-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="de957-126">The resource group name</span></span>

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

### <span data-ttu-id="de957-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="de957-127">-ResourceId</span></span>
<span data-ttu-id="de957-128">Die Ressourcen-ID des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="de957-128">The job step resource id</span></span>

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

### <span data-ttu-id="de957-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="de957-129">-ServerName</span></span>
<span data-ttu-id="de957-130">Der Servername</span><span class="sxs-lookup"><span data-stu-id="de957-130">The server name</span></span>

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

### <span data-ttu-id="de957-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de957-131">-Confirm</span></span>
<span data-ttu-id="de957-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de957-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de957-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de957-133">-WhatIf</span></span>
<span data-ttu-id="de957-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de957-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de957-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de957-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de957-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de957-136">CommonParameters</span></span>
<span data-ttu-id="de957-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de957-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de957-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de957-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de957-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de957-139">INPUTS</span></span>

### <span data-ttu-id="de957-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="de957-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="de957-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de957-141">OUTPUTS</span></span>

### <span data-ttu-id="de957-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="de957-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="de957-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="de957-143">NOTES</span></span>

## <span data-ttu-id="de957-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de957-144">RELATED LINKS</span></span>
