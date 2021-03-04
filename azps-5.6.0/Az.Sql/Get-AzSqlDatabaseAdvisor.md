---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: d946b6b324247a46760f762c4631419b6c6aac59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926387"
---
# <span data-ttu-id="6d85f-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="6d85f-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="6d85f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d85f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d85f-103">Ruft einen oder mehrere Berater für eine Azure-SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="6d85f-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="6d85f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d85f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d85f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d85f-105">DESCRIPTION</span></span>
<span data-ttu-id="6d85f-106">Das **Get-AzSqlDatabaseAdvisor-Cmdlet** ruft mindestens einen Azure SQL-Datenbankratgeber für eine Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="6d85f-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="6d85f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d85f-107">EXAMPLES</span></span>

### <span data-ttu-id="6d85f-108">Beispiel 1: Auflisten aller Berater für die angegebene Datenbank</span><span class="sxs-lookup"><span data-stu-id="6d85f-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="6d85f-109">Dieser Befehl ruft alle Berater für die Datenbank mit dem Namen WIRunner ab, die zu dem Server mit dem Namen wi-runner-australia-east gehört.</span><span class="sxs-lookup"><span data-stu-id="6d85f-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="6d85f-110">Beispiel 2: Einen einzigen Berater für die angegebene Datenbank erhalten</span><span class="sxs-lookup"><span data-stu-id="6d85f-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="6d85f-111">Dieser Befehl ruft den Berater mit dem Namen CreateIndex für die Datenbank mit dem Namen WIRunner ab.</span><span class="sxs-lookup"><span data-stu-id="6d85f-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="6d85f-112">Beispiel 3: Listen Sie alle Berater mit ihren empfohlenen Aktionen auf, die in der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6d85f-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="6d85f-113">Dieser Befehl ruft alle Berater für die Datenbank mit dem Namen "WIRunner" ab, deren empfohlene Aktionen in der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6d85f-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="6d85f-114">Da der Befehl den *Parameter ExpandRecommendedActions* verwendet, ruft das Cmdlet die empfohlenen Aktionen mit der Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="6d85f-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="6d85f-115">Beispiel 4: Erhalten eines einzelnen Beraters mit den empfohlenen Aktionen, die in der Antwort enthalten sind</span><span class="sxs-lookup"><span data-stu-id="6d85f-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="6d85f-116">Dieser Befehl ruft den Berater mit dem Namen CreateIndex aus der Datenbank mit dem Namen WIRunner mit den empfohlenen Aktionen ab, die in der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6d85f-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="6d85f-117">Da der Befehl den *Parameter ExpandRecommendedActions* verwendet, ruft das Cmdlet die empfohlenen Aktionen mit der Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="6d85f-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="6d85f-118">Beispiel 5: List all the advisors for the specified database using filtering</span><span class="sxs-lookup"><span data-stu-id="6d85f-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="6d85f-119">Dieser Befehl ruft alle Berater für die Datenbank namens WIRunner auf, die zum Server mit dem Namen wi-runner-australia-east gehört und mit dem Buchstaben "d" beginnen.</span><span class="sxs-lookup"><span data-stu-id="6d85f-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="6d85f-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6d85f-120">PARAMETERS</span></span>

### <span data-ttu-id="6d85f-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="6d85f-121">-AdvisorName</span></span>
<span data-ttu-id="6d85f-122">Gibt den Namen des Beraters an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6d85f-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6d85f-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6d85f-123">-DatabaseName</span></span>
<span data-ttu-id="6d85f-124">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Berater anfordert.</span><span class="sxs-lookup"><span data-stu-id="6d85f-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="6d85f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d85f-125">-DefaultProfile</span></span>
<span data-ttu-id="6d85f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6d85f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d85f-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="6d85f-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="6d85f-128">Gibt an, dass dieses Cmdlet die empfohlenen Aktionen mit der Antwort erhält.</span><span class="sxs-lookup"><span data-stu-id="6d85f-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d85f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d85f-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d85f-130">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="6d85f-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="6d85f-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="6d85f-131">-ServerName</span></span>
<span data-ttu-id="6d85f-132">Gibt den Namen des Servers an, der die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="6d85f-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="6d85f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d85f-133">CommonParameters</span></span>
<span data-ttu-id="6d85f-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d85f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d85f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d85f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d85f-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d85f-136">INPUTS</span></span>

### <span data-ttu-id="6d85f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6d85f-137">System.String</span></span>

### <span data-ttu-id="6d85f-138">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6d85f-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6d85f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d85f-139">OUTPUTS</span></span>

### <span data-ttu-id="6d85f-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="6d85f-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="6d85f-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6d85f-141">NOTES</span></span>
* <span data-ttu-id="6d85f-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="6d85f-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="6d85f-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6d85f-143">RELATED LINKS</span></span>

[<span data-ttu-id="6d85f-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="6d85f-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="6d85f-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="6d85f-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="6d85f-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="6d85f-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="6d85f-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6d85f-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="6d85f-148">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="6d85f-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
