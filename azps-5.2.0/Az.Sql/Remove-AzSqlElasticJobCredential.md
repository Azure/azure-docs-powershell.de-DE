---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306867"
---
# <span data-ttu-id="d2f38-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="d2f38-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="d2f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f38-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f38-103">Entfernt die Anmeldeinformationen für den Job aus dem Job.</span><span class="sxs-lookup"><span data-stu-id="d2f38-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="d2f38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2f38-104">SYNTAX</span></span>

### <span data-ttu-id="d2f38-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2f38-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f38-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d2f38-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f38-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d2f38-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f38-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2f38-108">DESCRIPTION</span></span>
<span data-ttu-id="d2f38-109">Das Remove-AzSqlElasticJobCredential cmdlet entfernt die Anmeldeinformationen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="d2f38-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="d2f38-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2f38-110">EXAMPLES</span></span>

### <span data-ttu-id="d2f38-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2f38-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="d2f38-112">Entfernt die Anmeldeinformationen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="d2f38-112">Removes a job credential</span></span>

## <span data-ttu-id="d2f38-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2f38-113">PARAMETERS</span></span>

### <span data-ttu-id="d2f38-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d2f38-114">-AgentName</span></span>
<span data-ttu-id="d2f38-115">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="d2f38-115">The agent name</span></span>

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

### <span data-ttu-id="d2f38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f38-116">-DefaultProfile</span></span>
<span data-ttu-id="d2f38-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2f38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f38-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2f38-118">-InputObject</span></span>
<span data-ttu-id="d2f38-119">Das Objekt mit den Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d2f38-119">The job credential object</span></span>

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

### <span data-ttu-id="d2f38-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d2f38-120">-Name</span></span>
<span data-ttu-id="d2f38-121">Der Name der Anmeldeinformationen für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="d2f38-121">The job credential name</span></span>

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

### <span data-ttu-id="d2f38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f38-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2f38-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d2f38-123">The resource group name</span></span>

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

### <span data-ttu-id="d2f38-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2f38-124">-ResourceId</span></span>
<span data-ttu-id="d2f38-125">Die Ressourcen-ID der Auftragsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d2f38-125">The job credential resource id</span></span>

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

### <span data-ttu-id="d2f38-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2f38-126">-ServerName</span></span>
<span data-ttu-id="d2f38-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="d2f38-127">The server name</span></span>

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

### <span data-ttu-id="d2f38-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2f38-128">-Confirm</span></span>
<span data-ttu-id="d2f38-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2f38-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f38-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d2f38-130">-WhatIf</span></span>
<span data-ttu-id="d2f38-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f38-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f38-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2f38-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f38-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f38-133">CommonParameters</span></span>
<span data-ttu-id="d2f38-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f38-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f38-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2f38-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f38-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2f38-136">INPUTS</span></span>

### <span data-ttu-id="d2f38-137">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="d2f38-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="d2f38-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2f38-138">OUTPUTS</span></span>

### <span data-ttu-id="d2f38-139">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="d2f38-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="d2f38-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2f38-140">NOTES</span></span>

## <span data-ttu-id="d2f38-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2f38-141">RELATED LINKS</span></span>
