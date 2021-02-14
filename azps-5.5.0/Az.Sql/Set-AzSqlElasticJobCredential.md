---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163201"
---
# <span data-ttu-id="f245e-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="f245e-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="f245e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f245e-102">SYNOPSIS</span></span>
<span data-ttu-id="f245e-103">Aktualisiert die Anmeldeinformationen für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f245e-103">Updates a job credential</span></span>

## <span data-ttu-id="f245e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f245e-104">SYNTAX</span></span>

### <span data-ttu-id="f245e-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f245e-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f245e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f245e-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f245e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f245e-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f245e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f245e-108">DESCRIPTION</span></span>
<span data-ttu-id="f245e-109">Das Set-AzSqlElasticJobCredential cmdlet aktualisiert die Anmeldeinformationen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="f245e-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="f245e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f245e-110">EXAMPLES</span></span>

### <span data-ttu-id="f245e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f245e-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="f245e-112">Aktualisiert die Anmeldeinformationen für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f245e-112">Updates a job credential</span></span>

## <span data-ttu-id="f245e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f245e-113">PARAMETERS</span></span>

### <span data-ttu-id="f245e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f245e-114">-AgentName</span></span>
<span data-ttu-id="f245e-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="f245e-115">The agent name</span></span>

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

### <span data-ttu-id="f245e-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="f245e-116">-Credential</span></span>
<span data-ttu-id="f245e-117">Die Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f245e-117">The credential</span></span>

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

### <span data-ttu-id="f245e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f245e-118">-DefaultProfile</span></span>
<span data-ttu-id="f245e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f245e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f245e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f245e-120">-InputObject</span></span>
<span data-ttu-id="f245e-121">Das Objekt mit den Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f245e-121">The job credential object</span></span>

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

### <span data-ttu-id="f245e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f245e-122">-Name</span></span>
<span data-ttu-id="f245e-123">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="f245e-123">The job credential name</span></span>

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

### <span data-ttu-id="f245e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f245e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f245e-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f245e-125">The resource group name</span></span>

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

### <span data-ttu-id="f245e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f245e-126">-ResourceId</span></span>
<span data-ttu-id="f245e-127">Die Ressourcen-ID der Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f245e-127">The job credential resource id</span></span>

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

### <span data-ttu-id="f245e-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f245e-128">-ServerName</span></span>
<span data-ttu-id="f245e-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="f245e-129">The server name</span></span>

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

### <span data-ttu-id="f245e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f245e-130">-Confirm</span></span>
<span data-ttu-id="f245e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f245e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f245e-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f245e-132">-WhatIf</span></span>
<span data-ttu-id="f245e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f245e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f245e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f245e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f245e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f245e-135">CommonParameters</span></span>
<span data-ttu-id="f245e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f245e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f245e-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f245e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f245e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f245e-138">INPUTS</span></span>

### <span data-ttu-id="f245e-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="f245e-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="f245e-140">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="f245e-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="f245e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f245e-141">OUTPUTS</span></span>

### <span data-ttu-id="f245e-142">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="f245e-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="f245e-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f245e-143">NOTES</span></span>

## <span data-ttu-id="f245e-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f245e-144">RELATED LINKS</span></span>
