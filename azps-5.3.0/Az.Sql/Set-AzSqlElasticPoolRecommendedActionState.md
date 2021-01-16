---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468071"
---
# <span data-ttu-id="4f8ec-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4f8ec-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="4f8ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8ec-103">Aktualisiert den Zustand einer empfohlenen Aktion SQL Azure SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="4f8ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f8ec-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f8ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f8ec-105">DESCRIPTION</span></span>
<span data-ttu-id="4f8ec-106">Das **Cmdlet "Set-AzSqlElasticPoolRecommendedActionState"** aktualisiert den Status einer empfohlenen Aktion SQL Azure SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="4f8ec-107">Dieses Cmdlet wendet eine empfohlene Aktion basierend auf dem neuen Zustand an, wird zurückgesetzt oder verworfen.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="4f8ec-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f8ec-108">EXAMPLES</span></span>

### <span data-ttu-id="4f8ec-109">Beispiel 1: Aktualisieren des Status einer empfohlenen Aktion auf "Ausstehend"</span><span class="sxs-lookup"><span data-stu-id="4f8ec-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="4f8ec-110">Mit diesem Befehl wird der Status der empfohlenen Aktion des Pool "IR_ \[ test_schema \] _ \[ test_table_0.0361551 \] _6C7AE8CC9C87E7FD5893 "Ausstehend" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="4f8ec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f8ec-111">PARAMETERS</span></span>

### <span data-ttu-id="4f8ec-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="4f8ec-112">-AdvisorName</span></span>
<span data-ttu-id="4f8ec-113">Gibt den Namen des Beraters an, zu dem diese empfohlene Aktion gehört.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8ec-114">-DefaultProfile</span></span>
<span data-ttu-id="4f8ec-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4f8ec-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f8ec-116">-PoolName</span><span class="sxs-lookup"><span data-stu-id="4f8ec-116">-ElasticPoolName</span></span>
<span data-ttu-id="4f8ec-117">Gibt den Namen des Poolpools an.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ec-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="4f8ec-118">-RecommendedActionName</span></span>
<span data-ttu-id="4f8ec-119">Gibt den Namen der empfohlenen Aktion an, für die dieses Cmdlet den Zustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f8ec-121">Gibt den Namen der Ressourcengruppe des Servers an, der diesen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ec-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f8ec-122">-ServerName</span></span>
<span data-ttu-id="4f8ec-123">Gibt den Namen des Servers an, auf dem sich der Pool des Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ec-124">-State</span><span class="sxs-lookup"><span data-stu-id="4f8ec-124">-State</span></span>
<span data-ttu-id="4f8ec-125">Gibt den Wert an, mit dem dieses Cmdlet den empfohlenen Aktionszustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="4f8ec-126">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4f8ec-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f8ec-127">Aktiv</span><span class="sxs-lookup"><span data-stu-id="4f8ec-127">Active</span></span>
- <span data-ttu-id="4f8ec-128">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="4f8ec-128">Pending</span></span>
- <span data-ttu-id="4f8ec-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="4f8ec-129">PendingRevert</span></span>
- <span data-ttu-id="4f8ec-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="4f8ec-130">RevertCancelled</span></span>
- <span data-ttu-id="4f8ec-131">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="4f8ec-131">Ignored</span></span>
- <span data-ttu-id="4f8ec-132">Aufgelöst</span><span class="sxs-lookup"><span data-stu-id="4f8ec-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8ec-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f8ec-133">-Confirm</span></span>
<span data-ttu-id="4f8ec-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8ec-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f8ec-135">-WhatIf</span></span>
<span data-ttu-id="4f8ec-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f8ec-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8ec-138">CommonParameters</span></span>
<span data-ttu-id="4f8ec-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8ec-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f8ec-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8ec-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8ec-141">INPUTS</span></span>

### <span data-ttu-id="4f8ec-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4f8ec-142">System.String</span></span>

### <span data-ttu-id="4f8ec-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4f8ec-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="4f8ec-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8ec-144">OUTPUTS</span></span>

### <span data-ttu-id="4f8ec-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="4f8ec-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="4f8ec-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f8ec-146">NOTES</span></span>
* <span data-ttu-id="4f8ec-147">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql,pool, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="4f8ec-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="4f8ec-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f8ec-148">RELATED LINKS</span></span>

[<span data-ttu-id="4f8ec-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="4f8ec-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="4f8ec-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4f8ec-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="4f8ec-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4f8ec-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="4f8ec-152">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="4f8ec-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
