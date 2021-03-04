---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: f68aed09a0aef5e6edb83933bcef9827bd98420c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926272"
---
# <span data-ttu-id="191bb-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="191bb-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="191bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="191bb-102">SYNOPSIS</span></span>
<span data-ttu-id="191bb-103">Aktualisiert den Status einer empfohlenen Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="191bb-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="191bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="191bb-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="191bb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="191bb-105">DESCRIPTION</span></span>
<span data-ttu-id="191bb-106">Das **Cmdlet Set-AzSqlDatabaseRecommendedActionState** aktualisiert den Zustand einer empfohlenen Azure SQL-Datenbankaktion.</span><span class="sxs-lookup"><span data-stu-id="191bb-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="191bb-107">Dadurch kann eine empfohlene Aktion basierend auf dem neuen Zustand angewendet, zurückgesetzt oder verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="191bb-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="191bb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="191bb-108">EXAMPLES</span></span>

### <span data-ttu-id="191bb-109">Beispiel 1: Anwenden eines empfohlenen Aktionszustands auf Ausstehend</span><span class="sxs-lookup"><span data-stu-id="191bb-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

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

<span data-ttu-id="191bb-110">Mit diesem Befehl wird der Status der empfohlenen Aktion mit dem Namen IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 aktualisiert, die zur Datenbank mit dem Namen \] WIRunner zu Ausstehend gehört.</span><span class="sxs-lookup"><span data-stu-id="191bb-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="191bb-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="191bb-111">PARAMETERS</span></span>

### <span data-ttu-id="191bb-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="191bb-112">-AdvisorName</span></span>
<span data-ttu-id="191bb-113">Gibt den Namen des Beraters an, zu dem diese empfohlene Aktion gehört.</span><span class="sxs-lookup"><span data-stu-id="191bb-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="191bb-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="191bb-114">-DatabaseName</span></span>
<span data-ttu-id="191bb-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet den empfohlenen Aktionszustand legt.</span><span class="sxs-lookup"><span data-stu-id="191bb-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="191bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191bb-116">-DefaultProfile</span></span>
<span data-ttu-id="191bb-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="191bb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="191bb-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="191bb-118">-RecommendedActionName</span></span>
<span data-ttu-id="191bb-119">Gibt den Namen der empfohlenen Aktion an, für die der Zustand aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="191bb-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="191bb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="191bb-120">-ResourceGroupName</span></span>
<span data-ttu-id="191bb-121">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="191bb-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="191bb-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="191bb-122">-ServerName</span></span>
<span data-ttu-id="191bb-123">Gibt den Namen des Servers an, auf dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="191bb-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="191bb-124">-State</span><span class="sxs-lookup"><span data-stu-id="191bb-124">-State</span></span>
<span data-ttu-id="191bb-125">Gibt den neuen Wert an, auf den dieses Cmdlet den empfohlenen Aktionszustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="191bb-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="191bb-126">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="191bb-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="191bb-127">Aktiv</span><span class="sxs-lookup"><span data-stu-id="191bb-127">Active</span></span>
- <span data-ttu-id="191bb-128">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="191bb-128">Pending</span></span>
- <span data-ttu-id="191bb-129">AusstehendRevert</span><span class="sxs-lookup"><span data-stu-id="191bb-129">PendingRevert</span></span>
- <span data-ttu-id="191bb-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="191bb-130">RevertCancelled</span></span>
- <span data-ttu-id="191bb-131">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="191bb-131">Ignored</span></span>
- <span data-ttu-id="191bb-132">Aufgelöst</span><span class="sxs-lookup"><span data-stu-id="191bb-132">Resolved</span></span>

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

### <span data-ttu-id="191bb-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="191bb-133">-Confirm</span></span>
<span data-ttu-id="191bb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="191bb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="191bb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="191bb-135">-WhatIf</span></span>
<span data-ttu-id="191bb-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="191bb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="191bb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="191bb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="191bb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191bb-138">CommonParameters</span></span>
<span data-ttu-id="191bb-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191bb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191bb-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="191bb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191bb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="191bb-141">INPUTS</span></span>

### <span data-ttu-id="191bb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="191bb-142">System.String</span></span>

### <span data-ttu-id="191bb-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="191bb-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="191bb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="191bb-144">OUTPUTS</span></span>

### <span data-ttu-id="191bb-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="191bb-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="191bb-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="191bb-146">NOTES</span></span>
* <span data-ttu-id="191bb-147">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="191bb-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="191bb-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="191bb-148">RELATED LINKS</span></span>

[<span data-ttu-id="191bb-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="191bb-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="191bb-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="191bb-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="191bb-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="191bb-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="191bb-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="191bb-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="191bb-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="191bb-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="191bb-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="191bb-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="191bb-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="191bb-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="191bb-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="191bb-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="191bb-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="191bb-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="191bb-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="191bb-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="191bb-159">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="191bb-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
