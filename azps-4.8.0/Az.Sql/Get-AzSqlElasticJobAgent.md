---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010452"
---
# <span data-ttu-id="79d17-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="79d17-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="79d17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79d17-102">SYNOPSIS</span></span>
<span data-ttu-id="79d17-103">Ruft einen Azure SQL Elastic-Auftrags-Agent ab</span><span class="sxs-lookup"><span data-stu-id="79d17-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="79d17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79d17-104">SYNTAX</span></span>

### <span data-ttu-id="79d17-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="79d17-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79d17-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="79d17-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79d17-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79d17-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79d17-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79d17-108">DESCRIPTION</span></span>
<span data-ttu-id="79d17-109">Das Get-AzSqlElasticJobAgent-Cmdlet ruft einen oder mehrere elastische Auftrags-Agents ab.</span><span class="sxs-lookup"><span data-stu-id="79d17-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="79d17-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79d17-110">EXAMPLES</span></span>

### <span data-ttu-id="79d17-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79d17-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="79d17-112">Ruft einen elastischen Job-Agent ab</span><span class="sxs-lookup"><span data-stu-id="79d17-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="79d17-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="79d17-113">PARAMETERS</span></span>

### <span data-ttu-id="79d17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d17-114">-DefaultProfile</span></span>
<span data-ttu-id="79d17-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79d17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79d17-116">-Name</span><span class="sxs-lookup"><span data-stu-id="79d17-116">-Name</span></span>
<span data-ttu-id="79d17-117">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="79d17-117">The agent name</span></span>

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

### <span data-ttu-id="79d17-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79d17-118">-ParentObject</span></span>
<span data-ttu-id="79d17-119">Das Server Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="79d17-119">The server input object</span></span>

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

### <span data-ttu-id="79d17-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79d17-120">-ParentResourceId</span></span>
<span data-ttu-id="79d17-121">Die Serverressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="79d17-121">The server resource id</span></span>

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

### <span data-ttu-id="79d17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79d17-122">-ResourceGroupName</span></span>
<span data-ttu-id="79d17-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="79d17-123">The resource group name</span></span>

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

### <span data-ttu-id="79d17-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="79d17-124">-ServerName</span></span>
<span data-ttu-id="79d17-125">Der Servername</span><span class="sxs-lookup"><span data-stu-id="79d17-125">The server name</span></span>

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

### <span data-ttu-id="79d17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d17-126">CommonParameters</span></span>
<span data-ttu-id="79d17-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d17-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79d17-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d17-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79d17-129">INPUTS</span></span>

### <span data-ttu-id="79d17-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="79d17-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="79d17-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79d17-131">OUTPUTS</span></span>

### <span data-ttu-id="79d17-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="79d17-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="79d17-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="79d17-133">NOTES</span></span>

## <span data-ttu-id="79d17-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79d17-134">RELATED LINKS</span></span>
