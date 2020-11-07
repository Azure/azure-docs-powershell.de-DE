---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 4652774b07ca3ae58baf29b614bd63519d537a0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825943"
---
# <span data-ttu-id="6f036-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="6f036-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="6f036-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f036-102">SYNOPSIS</span></span>
<span data-ttu-id="6f036-103">Entfernt die Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="6f036-103">Removes the target group</span></span>

## <span data-ttu-id="6f036-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f036-104">SYNTAX</span></span>

### <span data-ttu-id="6f036-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f036-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f036-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f036-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f036-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f036-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f036-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f036-108">DESCRIPTION</span></span>
<span data-ttu-id="6f036-109">Das Remove-AzSqlElasticJobTargetGroup-Cmdlet entfernt eine Zielgruppe und ihre Ziele</span><span class="sxs-lookup"><span data-stu-id="6f036-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="6f036-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f036-110">EXAMPLES</span></span>

### <span data-ttu-id="6f036-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f036-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="6f036-112">Entfernt eine Zielgruppe und ihre Ziele</span><span class="sxs-lookup"><span data-stu-id="6f036-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="6f036-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f036-113">PARAMETERS</span></span>

### <span data-ttu-id="6f036-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="6f036-114">-AgentName</span></span>
<span data-ttu-id="6f036-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="6f036-115">The agent name</span></span>

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

### <span data-ttu-id="6f036-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f036-116">-DefaultProfile</span></span>
<span data-ttu-id="6f036-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f036-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f036-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6f036-118">-Force</span></span>
<span data-ttu-id="6f036-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="6f036-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f036-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6f036-120">-InputObject</span></span>
<span data-ttu-id="6f036-121">Das Zielgruppen Objekt</span><span class="sxs-lookup"><span data-stu-id="6f036-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f036-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6f036-122">-Name</span></span>
<span data-ttu-id="6f036-123">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="6f036-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f036-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f036-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f036-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6f036-125">The resource group name</span></span>

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

### <span data-ttu-id="6f036-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6f036-126">-ResourceId</span></span>
<span data-ttu-id="6f036-127">Die Ressourcen-ID der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="6f036-127">The target group resource id</span></span>

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

### <span data-ttu-id="6f036-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="6f036-128">-ServerName</span></span>
<span data-ttu-id="6f036-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="6f036-129">The server name</span></span>

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

### <span data-ttu-id="6f036-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f036-130">-Confirm</span></span>
<span data-ttu-id="6f036-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f036-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f036-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f036-132">-WhatIf</span></span>
<span data-ttu-id="6f036-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f036-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f036-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f036-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f036-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f036-135">CommonParameters</span></span>
<span data-ttu-id="6f036-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f036-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f036-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f036-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f036-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f036-138">INPUTS</span></span>

### <span data-ttu-id="6f036-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="6f036-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="6f036-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f036-140">OUTPUTS</span></span>

### <span data-ttu-id="6f036-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="6f036-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="6f036-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f036-142">NOTES</span></span>

## <span data-ttu-id="6f036-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f036-143">RELATED LINKS</span></span>
