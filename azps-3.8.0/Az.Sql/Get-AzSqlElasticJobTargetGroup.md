---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847423"
---
# <span data-ttu-id="a277b-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="a277b-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="a277b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a277b-102">SYNOPSIS</span></span>
<span data-ttu-id="a277b-103">Ruft mindestens eine Auftragsziel Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a277b-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="a277b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a277b-104">SYNTAX</span></span>

### <span data-ttu-id="a277b-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="a277b-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a277b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a277b-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a277b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a277b-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a277b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a277b-108">DESCRIPTION</span></span>
<span data-ttu-id="a277b-109">Das Get-AzSqlElasticJobTargetGroup-Cmdlet ruft eine Zielgruppe und ihre Ziele ab.</span><span class="sxs-lookup"><span data-stu-id="a277b-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="a277b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a277b-110">EXAMPLES</span></span>

### <span data-ttu-id="a277b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a277b-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="a277b-112">Ruft eine Zielgruppe und ihre Ziele ab</span><span class="sxs-lookup"><span data-stu-id="a277b-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="a277b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a277b-113">PARAMETERS</span></span>

### <span data-ttu-id="a277b-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="a277b-114">-AgentName</span></span>
<span data-ttu-id="a277b-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="a277b-115">The agent name</span></span>

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

### <span data-ttu-id="a277b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a277b-116">-DefaultProfile</span></span>
<span data-ttu-id="a277b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a277b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a277b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a277b-118">-Name</span></span>
<span data-ttu-id="a277b-119">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="a277b-119">The target group name</span></span>

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

### <span data-ttu-id="a277b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a277b-120">-ParentObject</span></span>
<span data-ttu-id="a277b-121">Das Agent-Objekt</span><span class="sxs-lookup"><span data-stu-id="a277b-121">The agent object</span></span>

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

### <span data-ttu-id="a277b-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a277b-122">-ParentResourceId</span></span>
<span data-ttu-id="a277b-123">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a277b-123">The agent resource id</span></span>

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

### <span data-ttu-id="a277b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a277b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a277b-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a277b-125">The resource group name</span></span>

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

### <span data-ttu-id="a277b-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="a277b-126">-ServerName</span></span>
<span data-ttu-id="a277b-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="a277b-127">The server name</span></span>

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

### <span data-ttu-id="a277b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a277b-128">CommonParameters</span></span>
<span data-ttu-id="a277b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a277b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a277b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a277b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a277b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a277b-131">INPUTS</span></span>

### <span data-ttu-id="a277b-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a277b-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a277b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a277b-133">OUTPUTS</span></span>

### <span data-ttu-id="a277b-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="a277b-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="a277b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a277b-135">NOTES</span></span>

## <span data-ttu-id="a277b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a277b-136">RELATED LINKS</span></span>
