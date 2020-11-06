---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 992dc949ec4c17529415beeeb2cf2a831d4d2a68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480765"
---
# <span data-ttu-id="63eb3-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="63eb3-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="63eb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="63eb3-103">Aktualisiert den Zustand eines Azure SQL-elastischen Pools Empfohlene Aktion.</span><span class="sxs-lookup"><span data-stu-id="63eb3-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63eb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63eb3-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63eb3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="63eb3-106">Das Cmdlet " **Satz-AzureRmSqlElasticPoolRecommendedActionState** " aktualisiert den Zustand eines Azure SQL-elastischen Pools als empfohlene Aktion.</span><span class="sxs-lookup"><span data-stu-id="63eb3-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="63eb3-107">Dieses Cmdlet wendet eine empfohlene Aktion an, die auf Grundlage des neuen Zustands zurückgesetzt oder verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="63eb3-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="63eb3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63eb3-108">EXAMPLES</span></span>

### <span data-ttu-id="63eb3-109">Beispiel 1: Aktualisieren des Zustands einer empfohlenen Aktion in Ausstehend</span><span class="sxs-lookup"><span data-stu-id="63eb3-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="63eb3-110">Mit diesem Befehl wird der Zustand der empfohlenen elastischen Pool Aktion mit dem Namen IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 auf Ausstehend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="63eb3-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="63eb3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="63eb3-111">PARAMETERS</span></span>

### <span data-ttu-id="63eb3-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="63eb3-112">-AdvisorName</span></span>
<span data-ttu-id="63eb3-113">Gibt den Namen des Beraters an, zu dem diese empfohlene Aktion gehört.</span><span class="sxs-lookup"><span data-stu-id="63eb3-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63eb3-114">-DefaultProfile</span></span>
<span data-ttu-id="63eb3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="63eb3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="63eb3-116">-ElasticPoolName</span></span>
<span data-ttu-id="63eb3-117">Gibt den Namen des elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="63eb3-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="63eb3-118">-RecommendedActionName</span></span>
<span data-ttu-id="63eb3-119">Gibt den Namen der empfohlenen Aktion an, für die dieses Cmdlet den Zustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="63eb3-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63eb3-120">-ResourceGroupName</span></span>
<span data-ttu-id="63eb3-121">Gibt den Namen der Ressourcengruppe des Servers an, der diesen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="63eb3-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="63eb3-122">-ServerName</span></span>
<span data-ttu-id="63eb3-123">Gibt den Namen des Servers an, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="63eb3-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-124">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="63eb3-124">-State</span></span>
<span data-ttu-id="63eb3-125">Gibt den Wert an, zu dem dieses Cmdlet den empfohlenen Aktionszustand aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="63eb3-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="63eb3-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="63eb3-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63eb3-127">Active</span><span class="sxs-lookup"><span data-stu-id="63eb3-127">Active</span></span>
- <span data-ttu-id="63eb3-128">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="63eb3-128">Pending</span></span>
- <span data-ttu-id="63eb3-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="63eb3-129">PendingRevert</span></span>
- <span data-ttu-id="63eb3-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="63eb3-130">RevertCancelled</span></span>
- <span data-ttu-id="63eb3-131">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="63eb3-131">Ignored</span></span>
- <span data-ttu-id="63eb3-132">Gelöst</span><span class="sxs-lookup"><span data-stu-id="63eb3-132">Resolved</span></span>

```yaml
Type: RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63eb3-133">-Confirm</span></span>
<span data-ttu-id="63eb3-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63eb3-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63eb3-135">-WhatIf</span></span>
<span data-ttu-id="63eb3-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63eb3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63eb3-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63eb3-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63eb3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63eb3-138">CommonParameters</span></span>
<span data-ttu-id="63eb3-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63eb3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63eb3-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63eb3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63eb3-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63eb3-141">INPUTS</span></span>

### <span data-ttu-id="63eb3-142">Keine</span><span class="sxs-lookup"><span data-stu-id="63eb3-142">None</span></span>
<span data-ttu-id="63eb3-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="63eb3-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63eb3-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63eb3-144">OUTPUTS</span></span>

## <span data-ttu-id="63eb3-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="63eb3-145">NOTES</span></span>
* <span data-ttu-id="63eb3-146">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, empfohlenes</span><span class="sxs-lookup"><span data-stu-id="63eb3-146">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="63eb3-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63eb3-147">RELATED LINKS</span></span>

[<span data-ttu-id="63eb3-148">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="63eb3-148">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="63eb3-149">Satz-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="63eb3-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="63eb3-150">Satz-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="63eb3-150">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="63eb3-151">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="63eb3-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
