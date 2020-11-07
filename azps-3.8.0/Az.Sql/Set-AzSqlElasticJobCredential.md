---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846599"
---
# <span data-ttu-id="5cac9-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="5cac9-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="5cac9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cac9-102">SYNOPSIS</span></span>
<span data-ttu-id="5cac9-103">Aktualisieren einer Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5cac9-103">Updates a job credential</span></span>

## <span data-ttu-id="5cac9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cac9-104">SYNTAX</span></span>

### <span data-ttu-id="5cac9-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cac9-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cac9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5cac9-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cac9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5cac9-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cac9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cac9-108">DESCRIPTION</span></span>
<span data-ttu-id="5cac9-109">Das Set-AzSqlElasticJobCredential-Cmdlet aktualisiert eine Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5cac9-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="5cac9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cac9-110">EXAMPLES</span></span>

### <span data-ttu-id="5cac9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cac9-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="5cac9-112">Aktualisieren einer Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5cac9-112">Updates a job credential</span></span>

## <span data-ttu-id="5cac9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cac9-113">PARAMETERS</span></span>

### <span data-ttu-id="5cac9-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="5cac9-114">-AgentName</span></span>
<span data-ttu-id="5cac9-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="5cac9-115">The agent name</span></span>

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

### <span data-ttu-id="5cac9-116">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5cac9-116">-Credential</span></span>
<span data-ttu-id="5cac9-117">Die Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5cac9-117">The credential</span></span>

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

### <span data-ttu-id="5cac9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cac9-118">-DefaultProfile</span></span>
<span data-ttu-id="5cac9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cac9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cac9-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5cac9-120">-InputObject</span></span>
<span data-ttu-id="5cac9-121">Das Auftrags Anmeldeinformationsobjekt</span><span class="sxs-lookup"><span data-stu-id="5cac9-121">The job credential object</span></span>

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

### <span data-ttu-id="5cac9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5cac9-122">-Name</span></span>
<span data-ttu-id="5cac9-123">Der Name des Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5cac9-123">The job credential name</span></span>

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

### <span data-ttu-id="5cac9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cac9-124">-ResourceGroupName</span></span>
<span data-ttu-id="5cac9-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5cac9-125">The resource group name</span></span>

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

### <span data-ttu-id="5cac9-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5cac9-126">-ResourceId</span></span>
<span data-ttu-id="5cac9-127">Die Ressourcen-ID des Job-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5cac9-127">The job credential resource id</span></span>

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

### <span data-ttu-id="5cac9-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="5cac9-128">-ServerName</span></span>
<span data-ttu-id="5cac9-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="5cac9-129">The server name</span></span>

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

### <span data-ttu-id="5cac9-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cac9-130">-Confirm</span></span>
<span data-ttu-id="5cac9-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cac9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cac9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cac9-132">-WhatIf</span></span>
<span data-ttu-id="5cac9-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cac9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cac9-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cac9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cac9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cac9-135">CommonParameters</span></span>
<span data-ttu-id="5cac9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cac9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cac9-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cac9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cac9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cac9-138">INPUTS</span></span>

### <span data-ttu-id="5cac9-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5cac9-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="5cac9-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="5cac9-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="5cac9-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cac9-141">OUTPUTS</span></span>

### <span data-ttu-id="5cac9-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="5cac9-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="5cac9-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cac9-143">NOTES</span></span>

## <span data-ttu-id="5cac9-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cac9-144">RELATED LINKS</span></span>
