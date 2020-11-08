---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166018"
---
# <span data-ttu-id="69be6-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="69be6-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="69be6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69be6-102">SYNOPSIS</span></span>
<span data-ttu-id="69be6-103">Entfernt die Anmeldeinformationen für elastische Aufträge</span><span class="sxs-lookup"><span data-stu-id="69be6-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="69be6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69be6-104">SYNTAX</span></span>

### <span data-ttu-id="69be6-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="69be6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69be6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="69be6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69be6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="69be6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69be6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69be6-108">DESCRIPTION</span></span>
<span data-ttu-id="69be6-109">Das Remove-AzSqlElasticJobCredential-Cmdlet entfernt eine Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69be6-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="69be6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69be6-110">EXAMPLES</span></span>

### <span data-ttu-id="69be6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69be6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="69be6-112">Entfernt eine Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69be6-112">Removes a job credential</span></span>

## <span data-ttu-id="69be6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="69be6-113">PARAMETERS</span></span>

### <span data-ttu-id="69be6-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="69be6-114">-AgentName</span></span>
<span data-ttu-id="69be6-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="69be6-115">The agent name</span></span>

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

### <span data-ttu-id="69be6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69be6-116">-DefaultProfile</span></span>
<span data-ttu-id="69be6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69be6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69be6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69be6-118">-InputObject</span></span>
<span data-ttu-id="69be6-119">Das Auftrags Anmeldeinformationsobjekt</span><span class="sxs-lookup"><span data-stu-id="69be6-119">The job credential object</span></span>

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

### <span data-ttu-id="69be6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="69be6-120">-Name</span></span>
<span data-ttu-id="69be6-121">Der Name des Auftrags Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69be6-121">The job credential name</span></span>

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

### <span data-ttu-id="69be6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69be6-122">-ResourceGroupName</span></span>
<span data-ttu-id="69be6-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="69be6-123">The resource group name</span></span>

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

### <span data-ttu-id="69be6-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="69be6-124">-ResourceId</span></span>
<span data-ttu-id="69be6-125">Die Ressourcen-ID des Job-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69be6-125">The job credential resource id</span></span>

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

### <span data-ttu-id="69be6-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="69be6-126">-ServerName</span></span>
<span data-ttu-id="69be6-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="69be6-127">The server name</span></span>

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

### <span data-ttu-id="69be6-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69be6-128">-Confirm</span></span>
<span data-ttu-id="69be6-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69be6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69be6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69be6-130">-WhatIf</span></span>
<span data-ttu-id="69be6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69be6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69be6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69be6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69be6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69be6-133">CommonParameters</span></span>
<span data-ttu-id="69be6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69be6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69be6-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69be6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69be6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69be6-136">INPUTS</span></span>

### <span data-ttu-id="69be6-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="69be6-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="69be6-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69be6-138">OUTPUTS</span></span>

### <span data-ttu-id="69be6-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="69be6-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="69be6-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="69be6-140">NOTES</span></span>

## <span data-ttu-id="69be6-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69be6-141">RELATED LINKS</span></span>
