---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166835"
---
# <span data-ttu-id="3d535-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="3d535-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="3d535-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d535-102">SYNOPSIS</span></span>
<span data-ttu-id="3d535-103">Ruft mindestens eine Anmeldeinformation ab</span><span class="sxs-lookup"><span data-stu-id="3d535-103">Gets one or more credentials</span></span>

## <span data-ttu-id="3d535-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d535-104">SYNTAX</span></span>

### <span data-ttu-id="3d535-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d535-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d535-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3d535-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d535-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3d535-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d535-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d535-108">DESCRIPTION</span></span>
<span data-ttu-id="3d535-109">Das Get-AzSqlElasticJobCredential-Cmdlet ruft mindestens eine Auftrags Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="3d535-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="3d535-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d535-110">EXAMPLES</span></span>

### <span data-ttu-id="3d535-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d535-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="3d535-112">Ruft eine Auftrags Anmeldeinformationen ab</span><span class="sxs-lookup"><span data-stu-id="3d535-112">Gets a job credential</span></span>

## <span data-ttu-id="3d535-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d535-113">PARAMETERS</span></span>

### <span data-ttu-id="3d535-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="3d535-114">-AgentName</span></span>
<span data-ttu-id="3d535-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="3d535-115">The agent name</span></span>

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

### <span data-ttu-id="3d535-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d535-116">-DefaultProfile</span></span>
<span data-ttu-id="3d535-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d535-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d535-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3d535-118">-Name</span></span>
<span data-ttu-id="3d535-119">Der Name des Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="3d535-119">The job credential name</span></span>

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

### <span data-ttu-id="3d535-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3d535-120">-ParentObject</span></span>
<span data-ttu-id="3d535-121">Das Agent-Objekt</span><span class="sxs-lookup"><span data-stu-id="3d535-121">The agent object</span></span>

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

### <span data-ttu-id="3d535-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3d535-122">-ParentResourceId</span></span>
<span data-ttu-id="3d535-123">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3d535-123">The agent resource id</span></span>

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

### <span data-ttu-id="3d535-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d535-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d535-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3d535-125">The resource group name</span></span>

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

### <span data-ttu-id="3d535-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="3d535-126">-ServerName</span></span>
<span data-ttu-id="3d535-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="3d535-127">The server name</span></span>

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

### <span data-ttu-id="3d535-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d535-128">CommonParameters</span></span>
<span data-ttu-id="3d535-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d535-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d535-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d535-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d535-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d535-131">INPUTS</span></span>

### <span data-ttu-id="3d535-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3d535-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3d535-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d535-133">OUTPUTS</span></span>

### <span data-ttu-id="3d535-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="3d535-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3d535-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d535-135">NOTES</span></span>

## <span data-ttu-id="3d535-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d535-136">RELATED LINKS</span></span>
