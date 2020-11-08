---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174060"
---
# <span data-ttu-id="e12de-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e12de-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="e12de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e12de-102">SYNOPSIS</span></span>
<span data-ttu-id="e12de-103">Aktualisiert den Zustand der empfohlenen Azure SQL Server-Aktion.</span><span class="sxs-lookup"><span data-stu-id="e12de-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="e12de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e12de-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e12de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e12de-105">DESCRIPTION</span></span>
<span data-ttu-id="e12de-106">Das Cmdlet " **Satz-AzSqlServerRecommendedActionState** " aktualisiert den Zustand einer Azure SQL Server-empfohlenen Aktion.</span><span class="sxs-lookup"><span data-stu-id="e12de-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="e12de-107">Dieses Cmdlet wendet die empfohlene Aktion auf der Grundlage des neuen Zustands an oder verwirft Sie.</span><span class="sxs-lookup"><span data-stu-id="e12de-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="e12de-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e12de-108">EXAMPLES</span></span>

### <span data-ttu-id="e12de-109">Beispiel1: Aktualisieren des Zustands der angegebenen empfohlenen Aktion in Ausstehend</span><span class="sxs-lookup"><span data-stu-id="e12de-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="e12de-110">Updatestatus der Server empfohlenen Aktion mit dem Namen "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" zu "Ausstehend"</span><span class="sxs-lookup"><span data-stu-id="e12de-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="e12de-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e12de-111">PARAMETERS</span></span>

### <span data-ttu-id="e12de-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="e12de-112">-AdvisorName</span></span>
<span data-ttu-id="e12de-113">Gibt den Namen des Ratgebers an, der die empfohlene Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="e12de-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="e12de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12de-114">-DefaultProfile</span></span>
<span data-ttu-id="e12de-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e12de-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e12de-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="e12de-116">-RecommendedActionName</span></span>
<span data-ttu-id="e12de-117">Gibt den Namen der empfohlenen Aktion an, für die dieses Cmdlet den Zustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e12de-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="e12de-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e12de-118">-ResourceGroupName</span></span>
<span data-ttu-id="e12de-119">Gibt den Namen der Ressourcengruppe des Servers an.</span><span class="sxs-lookup"><span data-stu-id="e12de-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="e12de-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="e12de-120">-ServerName</span></span>
<span data-ttu-id="e12de-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="e12de-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e12de-122">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="e12de-122">-State</span></span>
<span data-ttu-id="e12de-123">Gibt den neuen Wert an, mit dem dieses Cmdlet den empfohlenen Aktionszustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e12de-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="e12de-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e12de-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e12de-125">Active</span><span class="sxs-lookup"><span data-stu-id="e12de-125">Active</span></span>
- <span data-ttu-id="e12de-126">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="e12de-126">Pending</span></span>
- <span data-ttu-id="e12de-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="e12de-127">PendingRevert</span></span>
- <span data-ttu-id="e12de-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="e12de-128">RevertCancelled</span></span>
- <span data-ttu-id="e12de-129">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="e12de-129">Ignored</span></span>
- <span data-ttu-id="e12de-130">Gelöst</span><span class="sxs-lookup"><span data-stu-id="e12de-130">Resolved</span></span>

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

### <span data-ttu-id="e12de-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e12de-131">-Confirm</span></span>
<span data-ttu-id="e12de-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e12de-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e12de-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12de-133">-WhatIf</span></span>
<span data-ttu-id="e12de-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e12de-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e12de-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e12de-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e12de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12de-136">CommonParameters</span></span>
<span data-ttu-id="e12de-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12de-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e12de-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12de-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e12de-139">INPUTS</span></span>

### <span data-ttu-id="e12de-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e12de-140">System.String</span></span>

### <span data-ttu-id="e12de-141">Microsoft. Azure. Commands. SQL. recommended. Cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e12de-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="e12de-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e12de-142">OUTPUTS</span></span>

### <span data-ttu-id="e12de-143">Microsoft. Azure. Commands. SQL. recommendive. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="e12de-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="e12de-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e12de-144">NOTES</span></span>
* <span data-ttu-id="e12de-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Server, MSSQL, Advisor, empfohlenes</span><span class="sxs-lookup"><span data-stu-id="e12de-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="e12de-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e12de-146">RELATED LINKS</span></span>

[<span data-ttu-id="e12de-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e12de-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="e12de-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e12de-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="e12de-149">Satz-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e12de-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="e12de-150">Satz-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e12de-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="e12de-151">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="e12de-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
