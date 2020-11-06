---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: bc66e944a71cdd354bd102969ed2914c496bcfe8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503922"
---
# <span data-ttu-id="e506a-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e506a-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="e506a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e506a-102">SYNOPSIS</span></span>
<span data-ttu-id="e506a-103">Ruft mindestens einen Ratgeber für eine Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="e506a-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e506a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e506a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e506a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e506a-105">DESCRIPTION</span></span>
<span data-ttu-id="e506a-106">Das Cmdlet " **Get-AzureRmSqlDatabaseAdvisor** " Ruft einen oder mehrere Azure SQL-Daten Bank Ratgeber für eine Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="e506a-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="e506a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e506a-107">EXAMPLES</span></span>

### <span data-ttu-id="e506a-108">Beispiel 1: Auflisten aller Ratgeber für die angegebene Datenbank</span><span class="sxs-lookup"><span data-stu-id="e506a-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="e506a-109">Dieser Befehl ruft alle Ratgeber für die Datenbank mit dem Namen WIRunner auf, die zum Server namens "Wi-Runner-Australia-East" gehört.</span><span class="sxs-lookup"><span data-stu-id="e506a-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="e506a-110">Beispiel 2: Abrufen eines einzelnen Ratgebers für die angegebene Datenbank</span><span class="sxs-lookup"><span data-stu-id="e506a-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="e506a-111">Dieser Befehl ruft den Berater mit dem Namen CreateIndex für die Datenbank mit dem Namen WIRunner ab.</span><span class="sxs-lookup"><span data-stu-id="e506a-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="e506a-112">Beispiel 3: Auflisten aller Ratgeber, deren empfohlene Aktionen in der Antwort enthalten sind</span><span class="sxs-lookup"><span data-stu-id="e506a-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="e506a-113">Dieser Befehl ruft alle Ratgeber für die Datenbank mit dem Namen "WIRunner" ab, wobei die empfohlenen Aktionen in der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e506a-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="e506a-114">Da der Befehl den *ExpandRecommendedActions* -Parameter verwendet, ruft das Cmdlet die empfohlenen Aktionen mit der Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="e506a-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="e506a-115">Beispiel 4: Abrufen eines einzelnen Ratgebers mit den empfohlenen Aktionen, die in der Antwort enthalten sind</span><span class="sxs-lookup"><span data-stu-id="e506a-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="e506a-116">Dieser Befehl ruft den Berater mit dem Namen CreateIndex aus der Datenbank mit dem Namen WIRunner mit den empfohlenen Aktionen ab, die in der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e506a-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="e506a-117">Da der Befehl den *ExpandRecommendedActions* -Parameter verwendet, ruft das Cmdlet die empfohlenen Aktionen mit der Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="e506a-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="e506a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e506a-118">PARAMETERS</span></span>

### <span data-ttu-id="e506a-119">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="e506a-119">-AdvisorName</span></span>
<span data-ttu-id="e506a-120">Gibt den Namen des Beraters an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e506a-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e506a-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e506a-121">-DatabaseName</span></span>
<span data-ttu-id="e506a-122">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Ratgeber anfordert.</span><span class="sxs-lookup"><span data-stu-id="e506a-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="e506a-123">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="e506a-123">-ExpandRecommendedActions</span></span>
<span data-ttu-id="e506a-124">Gibt an, dass dieses Cmdlet die empfohlenen Aktionen mit der Antwort abruft.</span><span class="sxs-lookup"><span data-stu-id="e506a-124">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="e506a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e506a-125">-ResourceGroupName</span></span>
<span data-ttu-id="e506a-126">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="e506a-126">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="e506a-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="e506a-127">-ServerName</span></span>
<span data-ttu-id="e506a-128">Gibt den Namen des Servers an, der die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="e506a-128">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="e506a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e506a-129">-DefaultProfile</span></span>
<span data-ttu-id="e506a-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e506a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e506a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e506a-131">CommonParameters</span></span>
<span data-ttu-id="e506a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e506a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e506a-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e506a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e506a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e506a-134">INPUTS</span></span>

## <span data-ttu-id="e506a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e506a-135">OUTPUTS</span></span>

### <span data-ttu-id="e506a-136">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e506a-136">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="e506a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e506a-137">NOTES</span></span>
* <span data-ttu-id="e506a-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL, Ratgeber</span><span class="sxs-lookup"><span data-stu-id="e506a-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="e506a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e506a-139">RELATED LINKS</span></span>

[<span data-ttu-id="e506a-140">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e506a-140">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="e506a-141">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e506a-141">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="e506a-142">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e506a-142">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="e506a-143">Satz-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e506a-143">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="e506a-144">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="e506a-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
