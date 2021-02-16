---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144060"
---
# <span data-ttu-id="2d775-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="2d775-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="2d775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d775-102">SYNOPSIS</span></span>
<span data-ttu-id="2d775-103">Entfernt die Anmeldeinformationen für den Job aus dem Job.</span><span class="sxs-lookup"><span data-stu-id="2d775-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="2d775-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d775-104">SYNTAX</span></span>

### <span data-ttu-id="2d775-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d775-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d775-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2d775-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d775-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2d775-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d775-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d775-108">DESCRIPTION</span></span>
<span data-ttu-id="2d775-109">Das Remove-AzSqlElasticJobCredential cmdlet entfernt die Anmeldeinformationen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="2d775-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="2d775-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d775-110">EXAMPLES</span></span>

### <span data-ttu-id="2d775-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d775-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="2d775-112">Entfernt die Anmeldeinformationen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="2d775-112">Removes a job credential</span></span>

## <span data-ttu-id="2d775-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d775-113">PARAMETERS</span></span>

### <span data-ttu-id="2d775-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2d775-114">-AgentName</span></span>
<span data-ttu-id="2d775-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="2d775-115">The agent name</span></span>

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

### <span data-ttu-id="2d775-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d775-116">-DefaultProfile</span></span>
<span data-ttu-id="2d775-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d775-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d775-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d775-118">-InputObject</span></span>
<span data-ttu-id="2d775-119">Das Objekt mit den Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="2d775-119">The job credential object</span></span>

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

### <span data-ttu-id="2d775-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2d775-120">-Name</span></span>
<span data-ttu-id="2d775-121">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="2d775-121">The job credential name</span></span>

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

### <span data-ttu-id="2d775-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d775-122">-ResourceGroupName</span></span>
<span data-ttu-id="2d775-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2d775-123">The resource group name</span></span>

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

### <span data-ttu-id="2d775-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d775-124">-ResourceId</span></span>
<span data-ttu-id="2d775-125">Die Ressourcen-ID der Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="2d775-125">The job credential resource id</span></span>

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

### <span data-ttu-id="2d775-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2d775-126">-ServerName</span></span>
<span data-ttu-id="2d775-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="2d775-127">The server name</span></span>

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

### <span data-ttu-id="2d775-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d775-128">-Confirm</span></span>
<span data-ttu-id="2d775-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d775-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d775-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2d775-130">-WhatIf</span></span>
<span data-ttu-id="2d775-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d775-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d775-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d775-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d775-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d775-133">CommonParameters</span></span>
<span data-ttu-id="2d775-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d775-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d775-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d775-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d775-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d775-136">INPUTS</span></span>

### <span data-ttu-id="2d775-137">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="2d775-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="2d775-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d775-138">OUTPUTS</span></span>

### <span data-ttu-id="2d775-139">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="2d775-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="2d775-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d775-140">NOTES</span></span>

## <span data-ttu-id="2d775-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d775-141">RELATED LINKS</span></span>
