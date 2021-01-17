---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371228"
---
# <span data-ttu-id="69bb1-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="69bb1-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="69bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="69bb1-103">Aktualisiert die Anmeldeinformationen für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="69bb1-103">Updates a job credential</span></span>

## <span data-ttu-id="69bb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69bb1-104">SYNTAX</span></span>

### <span data-ttu-id="69bb1-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69bb1-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69bb1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="69bb1-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69bb1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="69bb1-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69bb1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69bb1-108">DESCRIPTION</span></span>
<span data-ttu-id="69bb1-109">Das Set-AzSqlElasticJobCredential cmdlet aktualisiert die Anmeldeinformationen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="69bb1-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="69bb1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69bb1-110">EXAMPLES</span></span>

### <span data-ttu-id="69bb1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69bb1-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="69bb1-112">Aktualisiert die Anmeldeinformationen für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="69bb1-112">Updates a job credential</span></span>

## <span data-ttu-id="69bb1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69bb1-113">PARAMETERS</span></span>

### <span data-ttu-id="69bb1-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="69bb1-114">-AgentName</span></span>
<span data-ttu-id="69bb1-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="69bb1-115">The agent name</span></span>

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

### <span data-ttu-id="69bb1-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="69bb1-116">-Credential</span></span>
<span data-ttu-id="69bb1-117">Die Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69bb1-117">The credential</span></span>

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

### <span data-ttu-id="69bb1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bb1-118">-DefaultProfile</span></span>
<span data-ttu-id="69bb1-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69bb1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69bb1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69bb1-120">-InputObject</span></span>
<span data-ttu-id="69bb1-121">Das Objekt mit den Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69bb1-121">The job credential object</span></span>

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

### <span data-ttu-id="69bb1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="69bb1-122">-Name</span></span>
<span data-ttu-id="69bb1-123">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="69bb1-123">The job credential name</span></span>

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

### <span data-ttu-id="69bb1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69bb1-124">-ResourceGroupName</span></span>
<span data-ttu-id="69bb1-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="69bb1-125">The resource group name</span></span>

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

### <span data-ttu-id="69bb1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69bb1-126">-ResourceId</span></span>
<span data-ttu-id="69bb1-127">Die Ressourcen-ID der Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69bb1-127">The job credential resource id</span></span>

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

### <span data-ttu-id="69bb1-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69bb1-128">-ServerName</span></span>
<span data-ttu-id="69bb1-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="69bb1-129">The server name</span></span>

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

### <span data-ttu-id="69bb1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69bb1-130">-Confirm</span></span>
<span data-ttu-id="69bb1-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69bb1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69bb1-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="69bb1-132">-WhatIf</span></span>
<span data-ttu-id="69bb1-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69bb1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bb1-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69bb1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69bb1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bb1-135">CommonParameters</span></span>
<span data-ttu-id="69bb1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bb1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bb1-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69bb1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bb1-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69bb1-138">INPUTS</span></span>

### <span data-ttu-id="69bb1-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="69bb1-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="69bb1-140">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="69bb1-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="69bb1-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69bb1-141">OUTPUTS</span></span>

### <span data-ttu-id="69bb1-142">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="69bb1-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="69bb1-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69bb1-143">NOTES</span></span>

## <span data-ttu-id="69bb1-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69bb1-144">RELATED LINKS</span></span>
