---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374826"
---
# <span data-ttu-id="582d8-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="582d8-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="582d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="582d8-102">SYNOPSIS</span></span>
<span data-ttu-id="582d8-103">Ruft einen Mitarbeiter SQL Azure SQL Job ab</span><span class="sxs-lookup"><span data-stu-id="582d8-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="582d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="582d8-104">SYNTAX</span></span>

### <span data-ttu-id="582d8-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="582d8-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="582d8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="582d8-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="582d8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="582d8-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="582d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="582d8-108">DESCRIPTION</span></span>
<span data-ttu-id="582d8-109">Das Get-AzSqlElasticJobAgent cmdlet ruft einen oder mehrere Agents für Jobjobs ab</span><span class="sxs-lookup"><span data-stu-id="582d8-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="582d8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="582d8-110">EXAMPLES</span></span>

### <span data-ttu-id="582d8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="582d8-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="582d8-112">Ruft einen Jobcentermitarbeiter ab</span><span class="sxs-lookup"><span data-stu-id="582d8-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="582d8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="582d8-113">PARAMETERS</span></span>

### <span data-ttu-id="582d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582d8-114">-DefaultProfile</span></span>
<span data-ttu-id="582d8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="582d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="582d8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="582d8-116">-Name</span></span>
<span data-ttu-id="582d8-117">Der Name des Agents</span><span class="sxs-lookup"><span data-stu-id="582d8-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="582d8-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="582d8-118">-ParentObject</span></span>
<span data-ttu-id="582d8-119">Das Servereingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="582d8-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="582d8-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="582d8-120">-ParentResourceId</span></span>
<span data-ttu-id="582d8-121">Die Serverressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="582d8-121">The server resource id</span></span>

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

### <span data-ttu-id="582d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="582d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="582d8-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="582d8-123">The resource group name</span></span>

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

### <span data-ttu-id="582d8-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="582d8-124">-ServerName</span></span>
<span data-ttu-id="582d8-125">Der Servername</span><span class="sxs-lookup"><span data-stu-id="582d8-125">The server name</span></span>

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

### <span data-ttu-id="582d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582d8-126">CommonParameters</span></span>
<span data-ttu-id="582d8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582d8-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="582d8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582d8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="582d8-129">INPUTS</span></span>

### <span data-ttu-id="582d8-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="582d8-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="582d8-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="582d8-131">OUTPUTS</span></span>

### <span data-ttu-id="582d8-132">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="582d8-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="582d8-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="582d8-133">NOTES</span></span>

## <span data-ttu-id="582d8-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="582d8-134">RELATED LINKS</span></span>
