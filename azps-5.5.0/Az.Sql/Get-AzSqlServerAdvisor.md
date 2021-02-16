---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144145"
---
# <span data-ttu-id="a7f62-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="a7f62-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="a7f62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7f62-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f62-103">Ruft einen oder mehrere Berater für eine Azure-SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a7f62-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="a7f62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7f62-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7f62-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f62-106">Das **Cmdlet Get-AzSqlServerAdvisor** erhält mindestens einen Azure SQL Server Berater für eine Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a7f62-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="a7f62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7f62-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f62-108">Beispiel 1: Auflisten aller Berater für den Server</span><span class="sxs-lookup"><span data-stu-id="a7f62-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="a7f62-109">Dieser Befehl ruft eine Liste aller Berater für den Server mit dem Namen "wi-runner-australia-east" ab, der zur Ressourcengruppe mit dem Namen "WI RunnersProd" gehört.</span><span class="sxs-lookup"><span data-stu-id="a7f62-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="a7f62-110">Beispiel 2: Einen einzigen Berater für den Server erhalten</span><span class="sxs-lookup"><span data-stu-id="a7f62-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="a7f62-111">Dieser Befehl ruft den Berater "CreateIndex" für den Server mit dem Namen "wi-runner-australia-east" ab.</span><span class="sxs-lookup"><span data-stu-id="a7f62-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="a7f62-112">Beispiel 3: Auflisten aller Berater mit den in der Antwort enthaltenen empfohlenen Aktionen</span><span class="sxs-lookup"><span data-stu-id="a7f62-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="a7f62-113">Dieser Befehl ruft alle Berater für den Server mit dem Namen "wi-runner-australia-east" ab.</span><span class="sxs-lookup"><span data-stu-id="a7f62-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="a7f62-114">Da der Befehl den *Parameter "ExpandRecommendedActions"* verwendet, ruft das Cmdlet die empfohlenen Aktionen der Berater in die Antwort auf.</span><span class="sxs-lookup"><span data-stu-id="a7f62-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="a7f62-115">Beispiel 4: Einen einzigen Berater mit den empfohlenen Aktionen in der Antwort erhalten</span><span class="sxs-lookup"><span data-stu-id="a7f62-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="a7f62-116">Dieser Befehl ruft den Berater "CreateIndex" vom Server "wi-runner-australia-east" ab, in dessen Antwort die empfohlenen Aktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a7f62-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="a7f62-117">Beispiel 5: Auflisten aller Berater für den Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="a7f62-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

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

<span data-ttu-id="a7f62-118">Dieser Befehl ruft eine Liste aller Berater für den Server mit dem Namen "wi-runner-australia-east" ab, der der Ressourcengruppe mit dem Namen "WI Durchlaufprod" angehört, die mit dem Buchstaben "d" beginnen.</span><span class="sxs-lookup"><span data-stu-id="a7f62-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="a7f62-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7f62-119">PARAMETERS</span></span>

### <span data-ttu-id="a7f62-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="a7f62-120">-AdvisorName</span></span>
<span data-ttu-id="a7f62-121">Gibt den Namen des Beraters an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a7f62-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7f62-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f62-122">-DefaultProfile</span></span>
<span data-ttu-id="a7f62-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a7f62-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7f62-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="a7f62-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="a7f62-125">Zeigt an, dass das Cmdlet die empfohlenen Aktionen der Berater enthält, die in der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a7f62-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="a7f62-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f62-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7f62-127">Gibt den Namen der Ressourcengruppe des Servers an.</span><span class="sxs-lookup"><span data-stu-id="a7f62-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="a7f62-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7f62-128">-ServerName</span></span>
<span data-ttu-id="a7f62-129">Gibt den Namen des Servers für den Berater an, den dieses Cmdlet anfordert.</span><span class="sxs-lookup"><span data-stu-id="a7f62-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="a7f62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f62-130">CommonParameters</span></span>
<span data-ttu-id="a7f62-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f62-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7f62-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f62-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7f62-133">INPUTS</span></span>

### <span data-ttu-id="a7f62-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a7f62-134">System.String</span></span>

### <span data-ttu-id="a7f62-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a7f62-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7f62-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7f62-136">OUTPUTS</span></span>

### <span data-ttu-id="a7f62-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="a7f62-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="a7f62-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a7f62-138">NOTES</span></span>
* <span data-ttu-id="a7f62-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="a7f62-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="a7f62-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a7f62-140">RELATED LINKS</span></span>

[<span data-ttu-id="a7f62-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="a7f62-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="a7f62-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="a7f62-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="a7f62-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="a7f62-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="a7f62-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a7f62-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="a7f62-145">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="a7f62-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

