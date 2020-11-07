---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 49ea5796e8f2b03fe67a6c40ab42dc7f1c2481e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658997"
---
# <span data-ttu-id="614e9-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="614e9-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="614e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="614e9-102">SYNOPSIS</span></span>
<span data-ttu-id="614e9-103">Aktualisiert den Zustand einer Azure SQL-Datenbank Empfohlene Aktion.</span><span class="sxs-lookup"><span data-stu-id="614e9-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="614e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="614e9-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="614e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="614e9-105">DESCRIPTION</span></span>
<span data-ttu-id="614e9-106">Das Cmdlet " **Satz-AzSqlDatabaseRecommendedActionState** " aktualisiert den Zustand einer Azure SQL-Datenbank-empfohlenen Aktion.</span><span class="sxs-lookup"><span data-stu-id="614e9-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="614e9-107">Dadurch kann eine empfohlene Aktion auf Grundlage des neuen Zustands angewendet, zurückgesetzt oder verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="614e9-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="614e9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="614e9-108">EXAMPLES</span></span>

### <span data-ttu-id="614e9-109">Beispiel 1: Anwenden eines empfohlenen Aktionszustands auf "Ausstehend"</span><span class="sxs-lookup"><span data-stu-id="614e9-109">Example 1: Apply a recommended action state to pending</span></span>
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

<span data-ttu-id="614e9-110">Dieser Befehl aktualisiert den Zustand der empfohlenen Aktion mit dem Namen IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893, die zu der Datenbank mit dem Namen WIRunner to Pending gehört.</span><span class="sxs-lookup"><span data-stu-id="614e9-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="614e9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="614e9-111">PARAMETERS</span></span>

### <span data-ttu-id="614e9-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="614e9-112">-AdvisorName</span></span>
<span data-ttu-id="614e9-113">Gibt den Namen des Beraters an, zu dem diese empfohlene Aktion gehört.</span><span class="sxs-lookup"><span data-stu-id="614e9-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="614e9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="614e9-114">-DatabaseName</span></span>
<span data-ttu-id="614e9-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet den empfohlenen Aktionszustand festlegt.</span><span class="sxs-lookup"><span data-stu-id="614e9-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="614e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614e9-116">-DefaultProfile</span></span>
<span data-ttu-id="614e9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="614e9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="614e9-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="614e9-118">-RecommendedActionName</span></span>
<span data-ttu-id="614e9-119">Gibt den Namen der empfohlenen Aktion an, für die der Zustand aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="614e9-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="614e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="614e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="614e9-121">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="614e9-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="614e9-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="614e9-122">-ServerName</span></span>
<span data-ttu-id="614e9-123">Gibt den Namen des Servers an, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="614e9-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="614e9-124">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="614e9-124">-State</span></span>
<span data-ttu-id="614e9-125">Gibt den neuen Wert an, mit dem dieses Cmdlet den empfohlenen Aktionszustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="614e9-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="614e9-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="614e9-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="614e9-127">Active</span><span class="sxs-lookup"><span data-stu-id="614e9-127">Active</span></span>
- <span data-ttu-id="614e9-128">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="614e9-128">Pending</span></span>
- <span data-ttu-id="614e9-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="614e9-129">PendingRevert</span></span>
- <span data-ttu-id="614e9-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="614e9-130">RevertCancelled</span></span>
- <span data-ttu-id="614e9-131">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="614e9-131">Ignored</span></span>
- <span data-ttu-id="614e9-132">Gelöst</span><span class="sxs-lookup"><span data-stu-id="614e9-132">Resolved</span></span>

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

### <span data-ttu-id="614e9-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="614e9-133">-Confirm</span></span>
<span data-ttu-id="614e9-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="614e9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="614e9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="614e9-135">-WhatIf</span></span>
<span data-ttu-id="614e9-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="614e9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="614e9-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="614e9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="614e9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614e9-138">CommonParameters</span></span>
<span data-ttu-id="614e9-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614e9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614e9-140">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="614e9-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614e9-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="614e9-141">INPUTS</span></span>

### <span data-ttu-id="614e9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="614e9-142">System.String</span></span>

### <span data-ttu-id="614e9-143">Microsoft. Azure. Commands. SQL. recommended. Cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="614e9-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="614e9-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="614e9-144">OUTPUTS</span></span>

### <span data-ttu-id="614e9-145">Microsoft. Azure. Commands. SQL. recommendive. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="614e9-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="614e9-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="614e9-146">NOTES</span></span>
* <span data-ttu-id="614e9-147">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL, Ratgeber, empfohlenes</span><span class="sxs-lookup"><span data-stu-id="614e9-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="614e9-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="614e9-148">RELATED LINKS</span></span>

[<span data-ttu-id="614e9-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="614e9-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="614e9-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="614e9-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="614e9-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="614e9-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="614e9-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="614e9-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="614e9-153">Satz-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="614e9-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="614e9-154">Satz-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="614e9-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="614e9-155">Satz-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="614e9-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="614e9-156">Satz-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="614e9-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="614e9-157">Satz-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="614e9-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="614e9-158">Satz-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="614e9-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="614e9-159">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="614e9-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
