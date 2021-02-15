---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143985"
---
# <span data-ttu-id="6c820-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6c820-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="6c820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c820-102">SYNOPSIS</span></span>
<span data-ttu-id="6c820-103">Aktualisiert den Status der automatischen Ausführung eines Azure SQL Poolratgebers.</span><span class="sxs-lookup"><span data-stu-id="6c820-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="6c820-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c820-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c820-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c820-105">DESCRIPTION</span></span>
<span data-ttu-id="6c820-106">Das **Cmdlet "Set-AzSqlElasticPoolAdvisorAutoExecuteStatus"** legt die Eigenschaft für die automatische Ausführung für einen Azure SQL Pool Advisor fest.</span><span class="sxs-lookup"><span data-stu-id="6c820-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="6c820-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c820-107">EXAMPLES</span></span>

### <span data-ttu-id="6c820-108">Beispiel 1: Aktivieren der automatischen Ausführung für einen Berater</span><span class="sxs-lookup"><span data-stu-id="6c820-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="6c820-109">Dieser Befehl legt den Status der automatischen Ausführung eines Beraters namens CreateIndex auf aktiviert fest.</span><span class="sxs-lookup"><span data-stu-id="6c820-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="6c820-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c820-110">PARAMETERS</span></span>

### <span data-ttu-id="6c820-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="6c820-111">-AdvisorName</span></span>
<span data-ttu-id="6c820-112">Gibt den Namen des Beraters an, für den dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6c820-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="6c820-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6c820-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="6c820-114">Gibt einen neuen Wert an, für den dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6c820-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="6c820-115">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6c820-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c820-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="6c820-116">Enabled</span></span>
- <span data-ttu-id="6c820-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="6c820-117">Disabled</span></span>
- <span data-ttu-id="6c820-118">Standard</span><span class="sxs-lookup"><span data-stu-id="6c820-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c820-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c820-119">-DefaultProfile</span></span>
<span data-ttu-id="6c820-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6c820-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c820-121">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6c820-121">-ElasticPoolName</span></span>
<span data-ttu-id="6c820-122">Gibt den Namen des Poolpools an.</span><span class="sxs-lookup"><span data-stu-id="6c820-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="6c820-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c820-123">-ResourceGroupName</span></span>
<span data-ttu-id="6c820-124">Gibt den Namen der Ressourcengruppe des Servers an, der diesen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="6c820-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="6c820-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c820-125">-ServerName</span></span>
<span data-ttu-id="6c820-126">Gibt den Namen des Servers an, auf dem sich der Pool des Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="6c820-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="6c820-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c820-127">-Confirm</span></span>
<span data-ttu-id="6c820-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c820-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c820-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6c820-129">-WhatIf</span></span>
<span data-ttu-id="6c820-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c820-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c820-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c820-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c820-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c820-132">CommonParameters</span></span>
<span data-ttu-id="6c820-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c820-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c820-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c820-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c820-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c820-135">INPUTS</span></span>

### <span data-ttu-id="6c820-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6c820-136">System.String</span></span>

### <span data-ttu-id="6c820-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6c820-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="6c820-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c820-138">OUTPUTS</span></span>

### <span data-ttu-id="6c820-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="6c820-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="6c820-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6c820-140">NOTES</span></span>
* <span data-ttu-id="6c820-141">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, pool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="6c820-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="6c820-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6c820-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c820-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="6c820-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="6c820-144">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="6c820-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
