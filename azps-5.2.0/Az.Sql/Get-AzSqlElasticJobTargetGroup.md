---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295643"
---
# <span data-ttu-id="5c58e-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="5c58e-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="5c58e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c58e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c58e-103">Ruft eine oder mehrere Zielgruppen für Aufgaben ab</span><span class="sxs-lookup"><span data-stu-id="5c58e-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="5c58e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c58e-104">SYNTAX</span></span>

### <span data-ttu-id="5c58e-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c58e-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c58e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c58e-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c58e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5c58e-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c58e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c58e-108">DESCRIPTION</span></span>
<span data-ttu-id="5c58e-109">Das Get-AzSqlElasticJobTargetGroup cmdlet ruft eine Zielgruppe und die Zielgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5c58e-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="5c58e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c58e-110">EXAMPLES</span></span>

### <span data-ttu-id="5c58e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c58e-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="5c58e-112">Ruft eine Zielgruppe und deren Ziele ab</span><span class="sxs-lookup"><span data-stu-id="5c58e-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="5c58e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c58e-113">PARAMETERS</span></span>

### <span data-ttu-id="5c58e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5c58e-114">-AgentName</span></span>
<span data-ttu-id="5c58e-115">Der Name des Agents</span><span class="sxs-lookup"><span data-stu-id="5c58e-115">The agent name</span></span>

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

### <span data-ttu-id="5c58e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c58e-116">-DefaultProfile</span></span>
<span data-ttu-id="5c58e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c58e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c58e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5c58e-118">-Name</span></span>
<span data-ttu-id="5c58e-119">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="5c58e-119">The target group name</span></span>

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

### <span data-ttu-id="5c58e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5c58e-120">-ParentObject</span></span>
<span data-ttu-id="5c58e-121">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="5c58e-121">The agent object</span></span>

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

### <span data-ttu-id="5c58e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5c58e-122">-ParentResourceId</span></span>
<span data-ttu-id="5c58e-123">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5c58e-123">The agent resource id</span></span>

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

### <span data-ttu-id="5c58e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c58e-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c58e-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5c58e-125">The resource group name</span></span>

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

### <span data-ttu-id="5c58e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c58e-126">-ServerName</span></span>
<span data-ttu-id="5c58e-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="5c58e-127">The server name</span></span>

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

### <span data-ttu-id="5c58e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c58e-128">CommonParameters</span></span>
<span data-ttu-id="5c58e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c58e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c58e-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c58e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c58e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c58e-131">INPUTS</span></span>

### <span data-ttu-id="5c58e-132">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5c58e-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5c58e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c58e-133">OUTPUTS</span></span>

### <span data-ttu-id="5c58e-134">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="5c58e-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="5c58e-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c58e-135">NOTES</span></span>

## <span data-ttu-id="5c58e-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c58e-136">RELATED LINKS</span></span>
