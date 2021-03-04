---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: d5ee112af595ba88672a26d0f8f64590ea670706
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923283"
---
# <span data-ttu-id="4b8d8-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="4b8d8-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="4b8d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8d8-103">Entfernt die Anmeldeinformationen für den flexiblen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4b8d8-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="4b8d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b8d8-104">SYNTAX</span></span>

### <span data-ttu-id="4b8d8-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b8d8-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8d8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4b8d8-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8d8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4b8d8-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b8d8-108">DESCRIPTION</span></span>
<span data-ttu-id="4b8d8-109">Das Remove-AzSqlElasticJobCredential cmdlet entfernt eine Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4b8d8-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="4b8d8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b8d8-110">EXAMPLES</span></span>

### <span data-ttu-id="4b8d8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b8d8-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="4b8d8-112">Entfernt anmeldeinformationen für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4b8d8-112">Removes a job credential</span></span>

## <span data-ttu-id="4b8d8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4b8d8-113">PARAMETERS</span></span>

### <span data-ttu-id="4b8d8-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4b8d8-114">-AgentName</span></span>
<span data-ttu-id="4b8d8-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="4b8d8-115">The agent name</span></span>

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

### <span data-ttu-id="4b8d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8d8-116">-DefaultProfile</span></span>
<span data-ttu-id="4b8d8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b8d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b8d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b8d8-118">-InputObject</span></span>
<span data-ttu-id="4b8d8-119">Das Anmeldeinformationsobjekt für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="4b8d8-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8d8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4b8d8-120">-Name</span></span>
<span data-ttu-id="4b8d8-121">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="4b8d8-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b8d8-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4b8d8-123">The resource group name</span></span>

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

### <span data-ttu-id="4b8d8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b8d8-124">-ResourceId</span></span>
<span data-ttu-id="4b8d8-125">Ressourcen-ID für Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4b8d8-125">The job credential resource id</span></span>

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

### <span data-ttu-id="4b8d8-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="4b8d8-126">-ServerName</span></span>
<span data-ttu-id="4b8d8-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="4b8d8-127">The server name</span></span>

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

### <span data-ttu-id="4b8d8-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b8d8-128">-Confirm</span></span>
<span data-ttu-id="4b8d8-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b8d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8d8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8d8-130">-WhatIf</span></span>
<span data-ttu-id="4b8d8-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b8d8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b8d8-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b8d8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8d8-133">CommonParameters</span></span>
<span data-ttu-id="4b8d8-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8d8-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b8d8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8d8-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b8d8-136">INPUTS</span></span>

### <span data-ttu-id="4b8d8-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="4b8d8-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="4b8d8-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b8d8-138">OUTPUTS</span></span>

### <span data-ttu-id="4b8d8-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="4b8d8-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="4b8d8-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4b8d8-140">NOTES</span></span>

## <span data-ttu-id="4b8d8-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4b8d8-141">RELATED LINKS</span></span>
