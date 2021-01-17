---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362170"
---
# <span data-ttu-id="34579-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="34579-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="34579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34579-102">SYNOPSIS</span></span>
<span data-ttu-id="34579-103">Erstellt eine neue Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="34579-103">Creates a new target group</span></span>

## <span data-ttu-id="34579-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34579-104">SYNTAX</span></span>

### <span data-ttu-id="34579-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="34579-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34579-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="34579-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34579-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="34579-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34579-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34579-108">DESCRIPTION</span></span>
<span data-ttu-id="34579-109">Das New-AzSqlElasticJobTargetGroup erstellt eine neue Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="34579-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="34579-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34579-110">EXAMPLES</span></span>

### <span data-ttu-id="34579-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34579-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="34579-112">Erstellt eine leere Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="34579-112">Creates an empty target group</span></span>

## <span data-ttu-id="34579-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34579-113">PARAMETERS</span></span>

### <span data-ttu-id="34579-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="34579-114">-AgentName</span></span>
<span data-ttu-id="34579-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="34579-115">The agent name</span></span>

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

### <span data-ttu-id="34579-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34579-116">-DefaultProfile</span></span>
<span data-ttu-id="34579-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34579-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34579-118">-Name</span><span class="sxs-lookup"><span data-stu-id="34579-118">-Name</span></span>
<span data-ttu-id="34579-119">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="34579-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34579-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34579-120">-ParentObject</span></span>
<span data-ttu-id="34579-121">Das Agenteingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="34579-121">The agent input object</span></span>

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

### <span data-ttu-id="34579-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="34579-122">-ParentResourceId</span></span>
<span data-ttu-id="34579-123">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="34579-123">The agent resource id</span></span>

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

### <span data-ttu-id="34579-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34579-124">-ResourceGroupName</span></span>
<span data-ttu-id="34579-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="34579-125">The resource group name</span></span>

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

### <span data-ttu-id="34579-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34579-126">-ServerName</span></span>
<span data-ttu-id="34579-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="34579-127">The server name</span></span>

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

### <span data-ttu-id="34579-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34579-128">-Confirm</span></span>
<span data-ttu-id="34579-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34579-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34579-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="34579-130">-WhatIf</span></span>
<span data-ttu-id="34579-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34579-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34579-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34579-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34579-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34579-133">CommonParameters</span></span>
<span data-ttu-id="34579-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34579-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34579-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34579-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34579-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34579-136">INPUTS</span></span>

### <span data-ttu-id="34579-137">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="34579-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="34579-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34579-138">OUTPUTS</span></span>

### <span data-ttu-id="34579-139">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="34579-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="34579-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="34579-140">NOTES</span></span>

## <span data-ttu-id="34579-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="34579-141">RELATED LINKS</span></span>
