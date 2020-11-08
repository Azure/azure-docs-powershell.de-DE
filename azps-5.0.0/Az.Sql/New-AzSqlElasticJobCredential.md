---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176881"
---
# <span data-ttu-id="9eac6-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="9eac6-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="9eac6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9eac6-102">SYNOPSIS</span></span>
<span data-ttu-id="9eac6-103">Erstellt eine neue Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9eac6-103">Creates a new job credential</span></span>

## <span data-ttu-id="9eac6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eac6-104">SYNTAX</span></span>

### <span data-ttu-id="9eac6-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="9eac6-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eac6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9eac6-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eac6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9eac6-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eac6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9eac6-108">DESCRIPTION</span></span>
<span data-ttu-id="9eac6-109">Das New-AzSqlElasticJobCredential-Cmdlet erstellt eine neue Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9eac6-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="9eac6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9eac6-110">EXAMPLES</span></span>

### <span data-ttu-id="9eac6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9eac6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="9eac6-112">Erstellt eine neue Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9eac6-112">Creates a new job credential</span></span>

## <span data-ttu-id="9eac6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eac6-113">PARAMETERS</span></span>

### <span data-ttu-id="9eac6-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="9eac6-114">-AgentName</span></span>
<span data-ttu-id="9eac6-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="9eac6-115">The agent name</span></span>

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

### <span data-ttu-id="9eac6-116">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9eac6-116">-Credential</span></span>
<span data-ttu-id="9eac6-117">Die Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9eac6-117">The credential</span></span>

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

### <span data-ttu-id="9eac6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eac6-118">-DefaultProfile</span></span>
<span data-ttu-id="9eac6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9eac6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eac6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9eac6-120">-Name</span></span>
<span data-ttu-id="9eac6-121">Der Name des Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9eac6-121">The job credential name</span></span>

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

### <span data-ttu-id="9eac6-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9eac6-122">-ParentObject</span></span>
<span data-ttu-id="9eac6-123">Das Agent-Objekt</span><span class="sxs-lookup"><span data-stu-id="9eac6-123">The agent object</span></span>

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

### <span data-ttu-id="9eac6-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9eac6-124">-ParentResourceId</span></span>
<span data-ttu-id="9eac6-125">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="9eac6-125">The agent resource id</span></span>

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

### <span data-ttu-id="9eac6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eac6-126">-ResourceGroupName</span></span>
<span data-ttu-id="9eac6-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9eac6-127">The resource group name</span></span>

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

### <span data-ttu-id="9eac6-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="9eac6-128">-ServerName</span></span>
<span data-ttu-id="9eac6-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="9eac6-129">The server name</span></span>

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

### <span data-ttu-id="9eac6-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9eac6-130">-Confirm</span></span>
<span data-ttu-id="9eac6-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9eac6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eac6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eac6-132">-WhatIf</span></span>
<span data-ttu-id="9eac6-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9eac6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eac6-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9eac6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eac6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eac6-135">CommonParameters</span></span>
<span data-ttu-id="9eac6-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eac6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eac6-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9eac6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eac6-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9eac6-138">INPUTS</span></span>

### <span data-ttu-id="9eac6-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9eac6-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="9eac6-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="9eac6-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9eac6-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9eac6-141">OUTPUTS</span></span>

### <span data-ttu-id="9eac6-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="9eac6-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9eac6-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="9eac6-143">NOTES</span></span>

## <span data-ttu-id="9eac6-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9eac6-144">RELATED LINKS</span></span>
