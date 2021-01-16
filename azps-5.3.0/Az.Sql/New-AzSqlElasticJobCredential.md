---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460711"
---
# <span data-ttu-id="b0420-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="b0420-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="b0420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0420-102">SYNOPSIS</span></span>
<span data-ttu-id="b0420-103">Erstellt anmeldeinformationen für einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="b0420-103">Creates a new job credential</span></span>

## <span data-ttu-id="b0420-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0420-104">SYNTAX</span></span>

### <span data-ttu-id="b0420-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0420-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0420-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b0420-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0420-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b0420-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0420-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0420-108">DESCRIPTION</span></span>
<span data-ttu-id="b0420-109">Das cmdlet New-AzSqlElasticJobCredential A0 erstellt neue Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="b0420-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="b0420-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0420-110">EXAMPLES</span></span>

### <span data-ttu-id="b0420-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0420-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="b0420-112">Erstellt anmeldeinformationen für einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="b0420-112">Creates a new job credential</span></span>

## <span data-ttu-id="b0420-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0420-113">PARAMETERS</span></span>

### <span data-ttu-id="b0420-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b0420-114">-AgentName</span></span>
<span data-ttu-id="b0420-115">Der Name des Agents</span><span class="sxs-lookup"><span data-stu-id="b0420-115">The agent name</span></span>

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

### <span data-ttu-id="b0420-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="b0420-116">-Credential</span></span>
<span data-ttu-id="b0420-117">Die Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="b0420-117">The credential</span></span>

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

### <span data-ttu-id="b0420-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0420-118">-DefaultProfile</span></span>
<span data-ttu-id="b0420-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0420-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0420-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b0420-120">-Name</span></span>
<span data-ttu-id="b0420-121">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="b0420-121">The job credential name</span></span>

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

### <span data-ttu-id="b0420-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b0420-122">-ParentObject</span></span>
<span data-ttu-id="b0420-123">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="b0420-123">The agent object</span></span>

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

### <span data-ttu-id="b0420-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b0420-124">-ParentResourceId</span></span>
<span data-ttu-id="b0420-125">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b0420-125">The agent resource id</span></span>

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

### <span data-ttu-id="b0420-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0420-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0420-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b0420-127">The resource group name</span></span>

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

### <span data-ttu-id="b0420-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0420-128">-ServerName</span></span>
<span data-ttu-id="b0420-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="b0420-129">The server name</span></span>

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

### <span data-ttu-id="b0420-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0420-130">-Confirm</span></span>
<span data-ttu-id="b0420-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0420-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0420-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b0420-132">-WhatIf</span></span>
<span data-ttu-id="b0420-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0420-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0420-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0420-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0420-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0420-135">CommonParameters</span></span>
<span data-ttu-id="b0420-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0420-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0420-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0420-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0420-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0420-138">INPUTS</span></span>

### <span data-ttu-id="b0420-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="b0420-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="b0420-140">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b0420-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b0420-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0420-141">OUTPUTS</span></span>

### <span data-ttu-id="b0420-142">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="b0420-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="b0420-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0420-143">NOTES</span></span>

## <span data-ttu-id="b0420-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0420-144">RELATED LINKS</span></span>
