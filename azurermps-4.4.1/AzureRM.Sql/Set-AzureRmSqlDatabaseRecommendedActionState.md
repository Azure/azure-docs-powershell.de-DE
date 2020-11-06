---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: d31af9321a474c1261b2ed75138696d9f1a45461
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481442"
---
# <span data-ttu-id="d8338-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="d8338-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="d8338-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8338-102">SYNOPSIS</span></span>
<span data-ttu-id="d8338-103">Aktualisiert den Zustand einer Azure SQL-Datenbank Empfohlene Aktion.</span><span class="sxs-lookup"><span data-stu-id="d8338-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8338-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8338-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8338-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8338-105">DESCRIPTION</span></span>
<span data-ttu-id="d8338-106">Das Cmdlet " **Satz-AzureRmSqlDatabaseRecommendedActionState** " aktualisiert den Zustand einer Azure SQL-Datenbank-empfohlenen Aktion.</span><span class="sxs-lookup"><span data-stu-id="d8338-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="d8338-107">Dadurch kann eine empfohlene Aktion auf Grundlage des neuen Zustands angewendet, zurückgesetzt oder verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="d8338-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="d8338-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8338-108">EXAMPLES</span></span>

### <span data-ttu-id="d8338-109">Beispiel 1: Anwenden eines empfohlenen Aktionszustands auf "Ausstehend"</span><span class="sxs-lookup"><span data-stu-id="d8338-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="d8338-110">Dieser Befehl aktualisiert den Zustand der empfohlenen Aktion mit dem Namen IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893, die zu der Datenbank mit dem Namen WIRunner to Pending gehört.</span><span class="sxs-lookup"><span data-stu-id="d8338-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="d8338-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8338-111">PARAMETERS</span></span>

### <span data-ttu-id="d8338-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="d8338-112">-AdvisorName</span></span>
<span data-ttu-id="d8338-113">Gibt den Namen des Beraters an, zu dem diese empfohlene Aktion gehört.</span><span class="sxs-lookup"><span data-stu-id="d8338-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="d8338-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8338-114">-DatabaseName</span></span>
<span data-ttu-id="d8338-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet den empfohlenen Aktionszustand festlegt.</span><span class="sxs-lookup"><span data-stu-id="d8338-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="d8338-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="d8338-116">-RecommendedActionName</span></span>
<span data-ttu-id="d8338-117">Gibt den Namen der empfohlenen Aktion an, für die der Zustand aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d8338-117">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="d8338-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8338-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8338-119">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="d8338-119">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d8338-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="d8338-120">-ServerName</span></span>
<span data-ttu-id="d8338-121">Gibt den Namen des Servers an, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="d8338-121">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="d8338-122">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="d8338-122">-State</span></span>
<span data-ttu-id="d8338-123">Gibt den neuen Wert an, mit dem dieses Cmdlet den empfohlenen Aktionszustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d8338-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="d8338-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d8338-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8338-125">Active</span><span class="sxs-lookup"><span data-stu-id="d8338-125">Active</span></span>
- <span data-ttu-id="d8338-126">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="d8338-126">Pending</span></span>
- <span data-ttu-id="d8338-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="d8338-127">PendingRevert</span></span>
- <span data-ttu-id="d8338-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="d8338-128">RevertCancelled</span></span>
- <span data-ttu-id="d8338-129">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="d8338-129">Ignored</span></span>
- <span data-ttu-id="d8338-130">Gelöst</span><span class="sxs-lookup"><span data-stu-id="d8338-130">Resolved</span></span>

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

### <span data-ttu-id="d8338-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8338-131">-Confirm</span></span>
<span data-ttu-id="d8338-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8338-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8338-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8338-133">-WhatIf</span></span>
<span data-ttu-id="d8338-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8338-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8338-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8338-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8338-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8338-136">-DefaultProfile</span></span>
<span data-ttu-id="d8338-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8338-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8338-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8338-138">CommonParameters</span></span>
<span data-ttu-id="d8338-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8338-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8338-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8338-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8338-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8338-141">INPUTS</span></span>

## <span data-ttu-id="d8338-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8338-142">OUTPUTS</span></span>

### <span data-ttu-id="d8338-143">Microsoft. Azure. Commands. SQL. recommendive. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="d8338-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="d8338-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8338-144">NOTES</span></span>
* <span data-ttu-id="d8338-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL, Ratgeber, empfohlenes</span><span class="sxs-lookup"><span data-stu-id="d8338-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="d8338-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8338-146">RELATED LINKS</span></span>

[<span data-ttu-id="d8338-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="d8338-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="d8338-148">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="d8338-148">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="d8338-149">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="d8338-149">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="d8338-150">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="d8338-150">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="d8338-151">Satz-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="d8338-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="d8338-152">Satz-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d8338-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="d8338-153">Satz-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="d8338-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="d8338-154">Satz-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="d8338-154">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="d8338-155">Satz-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d8338-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="d8338-156">Satz-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d8338-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="d8338-157">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d8338-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
