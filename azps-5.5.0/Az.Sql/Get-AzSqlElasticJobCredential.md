---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145692"
---
# <span data-ttu-id="4e6b1-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="4e6b1-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="4e6b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6b1-103">Ruft mindestens eine Anmeldeinformationen ab</span><span class="sxs-lookup"><span data-stu-id="4e6b1-103">Gets one or more credentials</span></span>

## <span data-ttu-id="4e6b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e6b1-104">SYNTAX</span></span>

### <span data-ttu-id="4e6b1-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e6b1-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6b1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e6b1-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6b1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4e6b1-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e6b1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e6b1-108">DESCRIPTION</span></span>
<span data-ttu-id="4e6b1-109">Das Get-AzSqlElasticJobCredential-Cmdlet erhält eine oder mehrere Anmeldeinformationen für Aufgaben</span><span class="sxs-lookup"><span data-stu-id="4e6b1-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="4e6b1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e6b1-110">EXAMPLES</span></span>

### <span data-ttu-id="4e6b1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e6b1-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="4e6b1-112">Ruft Anmeldeinformationen für einen Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="4e6b1-112">Gets a job credential</span></span>

## <span data-ttu-id="4e6b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e6b1-113">PARAMETERS</span></span>

### <span data-ttu-id="4e6b1-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4e6b1-114">-AgentName</span></span>
<span data-ttu-id="4e6b1-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="4e6b1-115">The agent name</span></span>

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

### <span data-ttu-id="4e6b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6b1-116">-DefaultProfile</span></span>
<span data-ttu-id="4e6b1-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e6b1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4e6b1-118">-Name</span></span>
<span data-ttu-id="4e6b1-119">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e6b1-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6b1-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4e6b1-120">-ParentObject</span></span>
<span data-ttu-id="4e6b1-121">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="4e6b1-121">The agent object</span></span>

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

### <span data-ttu-id="4e6b1-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4e6b1-122">-ParentResourceId</span></span>
<span data-ttu-id="4e6b1-123">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4e6b1-123">The agent resource id</span></span>

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

### <span data-ttu-id="4e6b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e6b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e6b1-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4e6b1-125">The resource group name</span></span>

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

### <span data-ttu-id="4e6b1-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e6b1-126">-ServerName</span></span>
<span data-ttu-id="4e6b1-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="4e6b1-127">The server name</span></span>

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

### <span data-ttu-id="4e6b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6b1-128">CommonParameters</span></span>
<span data-ttu-id="4e6b1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6b1-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e6b1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6b1-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e6b1-131">INPUTS</span></span>

### <span data-ttu-id="4e6b1-132">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4e6b1-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4e6b1-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e6b1-133">OUTPUTS</span></span>

### <span data-ttu-id="4e6b1-134">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="4e6b1-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="4e6b1-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e6b1-135">NOTES</span></span>

## <span data-ttu-id="4e6b1-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e6b1-136">RELATED LINKS</span></span>
