---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458263"
---
# <span data-ttu-id="af73d-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="af73d-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="af73d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af73d-102">SYNOPSIS</span></span>
<span data-ttu-id="af73d-103">Ruft eine oder mehrere Zielgruppen für Aufgaben ab</span><span class="sxs-lookup"><span data-stu-id="af73d-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="af73d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af73d-104">SYNTAX</span></span>

### <span data-ttu-id="af73d-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="af73d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af73d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="af73d-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af73d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af73d-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af73d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af73d-108">DESCRIPTION</span></span>
<span data-ttu-id="af73d-109">Das Get-AzSqlElasticJobTargetGroup cmdlet ruft eine Zielgruppe und die Zielgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="af73d-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="af73d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af73d-110">EXAMPLES</span></span>

### <span data-ttu-id="af73d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af73d-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="af73d-112">Ruft eine Zielgruppe und deren Ziele ab</span><span class="sxs-lookup"><span data-stu-id="af73d-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="af73d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af73d-113">PARAMETERS</span></span>

### <span data-ttu-id="af73d-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="af73d-114">-AgentName</span></span>
<span data-ttu-id="af73d-115">Der Name des Agents</span><span class="sxs-lookup"><span data-stu-id="af73d-115">The agent name</span></span>

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

### <span data-ttu-id="af73d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af73d-116">-DefaultProfile</span></span>
<span data-ttu-id="af73d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af73d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af73d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="af73d-118">-Name</span></span>
<span data-ttu-id="af73d-119">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="af73d-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af73d-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="af73d-120">-ParentObject</span></span>
<span data-ttu-id="af73d-121">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="af73d-121">The agent object</span></span>

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

### <span data-ttu-id="af73d-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="af73d-122">-ParentResourceId</span></span>
<span data-ttu-id="af73d-123">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="af73d-123">The agent resource id</span></span>

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

### <span data-ttu-id="af73d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af73d-124">-ResourceGroupName</span></span>
<span data-ttu-id="af73d-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="af73d-125">The resource group name</span></span>

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

### <span data-ttu-id="af73d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af73d-126">-ServerName</span></span>
<span data-ttu-id="af73d-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="af73d-127">The server name</span></span>

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

### <span data-ttu-id="af73d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af73d-128">CommonParameters</span></span>
<span data-ttu-id="af73d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af73d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af73d-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af73d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af73d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af73d-131">INPUTS</span></span>

### <span data-ttu-id="af73d-132">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="af73d-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="af73d-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af73d-133">OUTPUTS</span></span>

### <span data-ttu-id="af73d-134">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="af73d-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="af73d-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af73d-135">NOTES</span></span>

## <span data-ttu-id="af73d-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af73d-136">RELATED LINKS</span></span>
