---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3FC9E586-3962-437E-B89F-BB4EA1FBF403
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendedAction.md
ms.openlocfilehash: 83abaaceffd58ea3e1d6277cc0142bf36deb2cae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995968"
---
# <span data-ttu-id="1e044-101">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1e044-101">Get-AzSqlElasticPoolRecommendedAction</span></span>

## <span data-ttu-id="1e044-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e044-102">SYNOPSIS</span></span>
<span data-ttu-id="1e044-103">Ruft eine oder mehrere Empfohlene Aktionen für einen Azure SQL Elastic Pool Advisor ab.</span><span class="sxs-lookup"><span data-stu-id="1e044-103">Gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="1e044-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e044-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e044-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e044-105">DESCRIPTION</span></span>
<span data-ttu-id="1e044-106">Das Cmdlet " **Get-AzSqlElasticPoolRecommendedAction** " Ruft eine oder mehrere Empfohlene Aktionen für einen Azure SQL Elastic Pool Advisor ab.</span><span class="sxs-lookup"><span data-stu-id="1e044-106">The **Get-AzSqlElasticPoolRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="1e044-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e044-107">EXAMPLES</span></span>

### <span data-ttu-id="1e044-108">Beispiel 1: Auflisten aller empfohlenen Aktionen für einen Berater</span><span class="sxs-lookup"><span data-stu-id="1e044-108">Example 1: List all recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM

ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="1e044-109">Dieser Befehl ruft eine Liste aller empfohlenen Aktionen des Ratgebers mit dem Namen CreateIndex ab, die für den elastischen Pool mit dem Namen WIRunnerPool verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1e044-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="1e044-110">Beispiel 2: Abrufen einer einzelnen empfohlenen Aktion für einen Berater</span><span class="sxs-lookup"><span data-stu-id="1e044-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="1e044-111">Dieser Befehl ruft die empfohlene Aktion mit dem Namen IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 des Ratgebers mit dem Namen CreateIndex ab.</span><span class="sxs-lookup"><span data-stu-id="1e044-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="1e044-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e044-112">PARAMETERS</span></span>

### <span data-ttu-id="1e044-113">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="1e044-113">-AdvisorName</span></span>
<span data-ttu-id="1e044-114">Gibt den Namen des Beraters an, für den dieses Cmdlet Empfohlene Aktionen anfordert.</span><span class="sxs-lookup"><span data-stu-id="1e044-114">Specifies the name of the advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="1e044-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e044-115">-DefaultProfile</span></span>
<span data-ttu-id="1e044-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1e044-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e044-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1e044-117">-ElasticPoolName</span></span>
<span data-ttu-id="1e044-118">Gibt den Namen des elastischen Pools an, für den dieses Cmdlet Empfohlene Aktionen anfordert.</span><span class="sxs-lookup"><span data-stu-id="1e044-118">Specifies the name of the elastic pool for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="1e044-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="1e044-119">-RecommendedActionName</span></span>
<span data-ttu-id="1e044-120">Gibt den Namen der empfohlenen Aktion an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1e044-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e044-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e044-121">-ResourceGroupName</span></span>
<span data-ttu-id="1e044-122">Gibt den Namen der Ressourcengruppe des Servers an, der diesen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="1e044-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="1e044-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="1e044-123">-ServerName</span></span>
<span data-ttu-id="1e044-124">Gibt den Namen des Servers an, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="1e044-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="1e044-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e044-125">CommonParameters</span></span>
<span data-ttu-id="1e044-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e044-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e044-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e044-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e044-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e044-128">INPUTS</span></span>

### <span data-ttu-id="1e044-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1e044-129">System.String</span></span>

## <span data-ttu-id="1e044-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e044-130">OUTPUTS</span></span>

### <span data-ttu-id="1e044-131">Microsoft. Azure. Commands. SQL. recommendive. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="1e044-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="1e044-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e044-132">NOTES</span></span>
* <span data-ttu-id="1e044-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, empfohlenes</span><span class="sxs-lookup"><span data-stu-id="1e044-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="1e044-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e044-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e044-135">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1e044-135">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="1e044-136">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="1e044-136">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="1e044-137">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1e044-137">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="1e044-138">Satz-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1e044-138">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="1e044-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1e044-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
