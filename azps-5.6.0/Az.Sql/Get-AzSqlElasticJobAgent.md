---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 6ff5bdb6a3de7b1704ee41de0b6ff0b0f736ec5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949912"
---
# <span data-ttu-id="e0fa6-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="e0fa6-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="e0fa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fa6-103">Ruft einen Azure SQL -Mitarbeiter für den flexiblen Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="e0fa6-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="e0fa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0fa6-104">SYNTAX</span></span>

### <span data-ttu-id="e0fa6-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0fa6-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0fa6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e0fa6-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0fa6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e0fa6-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0fa6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0fa6-108">DESCRIPTION</span></span>
<span data-ttu-id="e0fa6-109">Das Get-AzSqlElasticJobAgent-Cmdlet erhält einen oder mehrere "Flexible Job"-Agents.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="e0fa6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0fa6-110">EXAMPLES</span></span>

### <span data-ttu-id="e0fa6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0fa6-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="e0fa6-112">Ruft einen Mitarbeiter für einen flexiblen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="e0fa6-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0fa6-113">PARAMETERS</span></span>

### <span data-ttu-id="e0fa6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0fa6-114">-DefaultProfile</span></span>
<span data-ttu-id="e0fa6-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0fa6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e0fa6-116">-Name</span></span>
<span data-ttu-id="e0fa6-117">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="e0fa6-117">The agent name</span></span>

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

### <span data-ttu-id="e0fa6-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e0fa6-118">-ParentObject</span></span>
<span data-ttu-id="e0fa6-119">Das Servereingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="e0fa6-119">The server input object</span></span>

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

### <span data-ttu-id="e0fa6-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e0fa6-120">-ParentResourceId</span></span>
<span data-ttu-id="e0fa6-121">Die Serverressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e0fa6-121">The server resource id</span></span>

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

### <span data-ttu-id="e0fa6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0fa6-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0fa6-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e0fa6-123">The resource group name</span></span>

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

### <span data-ttu-id="e0fa6-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="e0fa6-124">-ServerName</span></span>
<span data-ttu-id="e0fa6-125">Der Servername</span><span class="sxs-lookup"><span data-stu-id="e0fa6-125">The server name</span></span>

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

### <span data-ttu-id="e0fa6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fa6-126">CommonParameters</span></span>
<span data-ttu-id="e0fa6-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fa6-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0fa6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fa6-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0fa6-129">INPUTS</span></span>

### <span data-ttu-id="e0fa6-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e0fa6-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e0fa6-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0fa6-131">OUTPUTS</span></span>

### <span data-ttu-id="e0fa6-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e0fa6-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e0fa6-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e0fa6-133">NOTES</span></span>

## <span data-ttu-id="e0fa6-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e0fa6-134">RELATED LINKS</span></span>
