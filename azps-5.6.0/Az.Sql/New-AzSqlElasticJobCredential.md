---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 8f82162b0f1e5b1f43852880c77d1be1427e3ca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927744"
---
# <span data-ttu-id="8be37-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="8be37-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="8be37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be37-102">SYNOPSIS</span></span>
<span data-ttu-id="8be37-103">Erstellt eine neue Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="8be37-103">Creates a new job credential</span></span>

## <span data-ttu-id="8be37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8be37-104">SYNTAX</span></span>

### <span data-ttu-id="8be37-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8be37-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8be37-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8be37-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8be37-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8be37-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be37-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8be37-108">DESCRIPTION</span></span>
<span data-ttu-id="8be37-109">Das New-AzSqlElasticJobCredential-Cmdlet erstellt eine neue Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="8be37-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="8be37-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8be37-110">EXAMPLES</span></span>

### <span data-ttu-id="8be37-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8be37-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="8be37-112">Erstellt eine neue Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="8be37-112">Creates a new job credential</span></span>

## <span data-ttu-id="8be37-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8be37-113">PARAMETERS</span></span>

### <span data-ttu-id="8be37-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8be37-114">-AgentName</span></span>
<span data-ttu-id="8be37-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="8be37-115">The agent name</span></span>

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

### <span data-ttu-id="8be37-116">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="8be37-116">-Credential</span></span>
<span data-ttu-id="8be37-117">Die Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="8be37-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be37-118">-DefaultProfile</span></span>
<span data-ttu-id="8be37-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8be37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be37-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8be37-120">-Name</span></span>
<span data-ttu-id="8be37-121">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="8be37-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be37-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8be37-122">-ParentObject</span></span>
<span data-ttu-id="8be37-123">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="8be37-123">The agent object</span></span>

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

### <span data-ttu-id="8be37-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8be37-124">-ParentResourceId</span></span>
<span data-ttu-id="8be37-125">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8be37-125">The agent resource id</span></span>

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

### <span data-ttu-id="8be37-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be37-126">-ResourceGroupName</span></span>
<span data-ttu-id="8be37-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8be37-127">The resource group name</span></span>

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

### <span data-ttu-id="8be37-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="8be37-128">-ServerName</span></span>
<span data-ttu-id="8be37-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="8be37-129">The server name</span></span>

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

### <span data-ttu-id="8be37-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8be37-130">-Confirm</span></span>
<span data-ttu-id="8be37-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8be37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be37-132">-WhatIf</span></span>
<span data-ttu-id="8be37-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8be37-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be37-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8be37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be37-135">CommonParameters</span></span>
<span data-ttu-id="8be37-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be37-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8be37-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be37-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8be37-138">INPUTS</span></span>

### <span data-ttu-id="8be37-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="8be37-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="8be37-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="8be37-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8be37-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8be37-141">OUTPUTS</span></span>

### <span data-ttu-id="8be37-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="8be37-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="8be37-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8be37-143">NOTES</span></span>

## <span data-ttu-id="8be37-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8be37-144">RELATED LINKS</span></span>
