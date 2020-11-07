---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: b3e3aa1414b24324278f4191fd53a28a75d0cfab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825740"
---
# <span data-ttu-id="71514-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="71514-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="71514-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71514-102">SYNOPSIS</span></span>
<span data-ttu-id="71514-103">Aktualisieren einer Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71514-103">Updates a job credential</span></span>

## <span data-ttu-id="71514-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71514-104">SYNTAX</span></span>

### <span data-ttu-id="71514-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="71514-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71514-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="71514-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71514-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="71514-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71514-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71514-108">DESCRIPTION</span></span>
<span data-ttu-id="71514-109">Das Set-AzSqlElasticJobCredential-Cmdlet aktualisiert eine Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71514-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="71514-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71514-110">EXAMPLES</span></span>

### <span data-ttu-id="71514-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71514-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="71514-112">Aktualisieren einer Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71514-112">Updates a job credential</span></span>

## <span data-ttu-id="71514-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="71514-113">PARAMETERS</span></span>

### <span data-ttu-id="71514-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="71514-114">-AgentName</span></span>
<span data-ttu-id="71514-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="71514-115">The agent name</span></span>

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

### <span data-ttu-id="71514-116">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71514-116">-Credential</span></span>
<span data-ttu-id="71514-117">Die Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71514-117">The credential</span></span>

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

### <span data-ttu-id="71514-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71514-118">-DefaultProfile</span></span>
<span data-ttu-id="71514-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71514-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71514-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71514-120">-InputObject</span></span>
<span data-ttu-id="71514-121">Das Auftrags Anmeldeinformationsobjekt</span><span class="sxs-lookup"><span data-stu-id="71514-121">The job credential object</span></span>

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

### <span data-ttu-id="71514-122">-Name</span><span class="sxs-lookup"><span data-stu-id="71514-122">-Name</span></span>
<span data-ttu-id="71514-123">Der Name des Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71514-123">The job credential name</span></span>

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

### <span data-ttu-id="71514-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71514-124">-ResourceGroupName</span></span>
<span data-ttu-id="71514-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="71514-125">The resource group name</span></span>

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

### <span data-ttu-id="71514-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="71514-126">-ResourceId</span></span>
<span data-ttu-id="71514-127">Die Ressourcen-ID des Job-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71514-127">The job credential resource id</span></span>

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

### <span data-ttu-id="71514-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="71514-128">-ServerName</span></span>
<span data-ttu-id="71514-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="71514-129">The server name</span></span>

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

### <span data-ttu-id="71514-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71514-130">-Confirm</span></span>
<span data-ttu-id="71514-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71514-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71514-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71514-132">-WhatIf</span></span>
<span data-ttu-id="71514-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71514-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71514-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71514-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71514-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71514-135">CommonParameters</span></span>
<span data-ttu-id="71514-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71514-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71514-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71514-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71514-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71514-138">INPUTS</span></span>

### <span data-ttu-id="71514-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="71514-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="71514-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="71514-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="71514-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71514-141">OUTPUTS</span></span>

### <span data-ttu-id="71514-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="71514-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="71514-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="71514-143">NOTES</span></span>

## <span data-ttu-id="71514-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71514-144">RELATED LINKS</span></span>
