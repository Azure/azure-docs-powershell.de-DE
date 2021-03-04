---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa181dcb171a1842c2b6158078e60b717b33d579
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919107"
---
# <span data-ttu-id="5148d-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5148d-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="5148d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5148d-102">SYNOPSIS</span></span>
<span data-ttu-id="5148d-103">Aktualisiert den Status der automatischen Ausführung eines Azure SQL -Poolratgebers.</span><span class="sxs-lookup"><span data-stu-id="5148d-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="5148d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5148d-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5148d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5148d-105">DESCRIPTION</span></span>
<span data-ttu-id="5148d-106">Das **Cmdlet Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** legt die Eigenschaft für die automatische Ausführung für einen Azure SQL -Poolratgeber fest.</span><span class="sxs-lookup"><span data-stu-id="5148d-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="5148d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5148d-107">EXAMPLES</span></span>

### <span data-ttu-id="5148d-108">Beispiel 1: Aktivieren der automatischen Ausführung für einen Berater</span><span class="sxs-lookup"><span data-stu-id="5148d-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="5148d-109">Mit diesem Befehl wird der Status der automatischen Ausführung eines Beraters namens CreateIndex aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5148d-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="5148d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5148d-110">PARAMETERS</span></span>

### <span data-ttu-id="5148d-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="5148d-111">-AdvisorName</span></span>
<span data-ttu-id="5148d-112">Gibt den Namen des Beraters an, für den dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5148d-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="5148d-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5148d-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="5148d-114">Gibt einen neuen Wert an, auf den dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5148d-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="5148d-115">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5148d-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5148d-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="5148d-116">Enabled</span></span>
- <span data-ttu-id="5148d-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="5148d-117">Disabled</span></span>
- <span data-ttu-id="5148d-118">Standard</span><span class="sxs-lookup"><span data-stu-id="5148d-118">Default</span></span>

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

### <span data-ttu-id="5148d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5148d-119">-DefaultProfile</span></span>
<span data-ttu-id="5148d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5148d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5148d-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5148d-121">-ElasticPoolName</span></span>
<span data-ttu-id="5148d-122">Gibt den Namen des Pool für den Flexiblen Pool an.</span><span class="sxs-lookup"><span data-stu-id="5148d-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="5148d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5148d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5148d-124">Gibt den Namen der Ressourcengruppe des Servers an, der diesen Pool für den Flexiblen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="5148d-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="5148d-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="5148d-125">-ServerName</span></span>
<span data-ttu-id="5148d-126">Gibt den Namen des Servers an, in dem sich der Pool für den Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="5148d-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="5148d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5148d-127">-Confirm</span></span>
<span data-ttu-id="5148d-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5148d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5148d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5148d-129">-WhatIf</span></span>
<span data-ttu-id="5148d-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5148d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5148d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5148d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5148d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5148d-132">CommonParameters</span></span>
<span data-ttu-id="5148d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5148d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5148d-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5148d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5148d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5148d-135">INPUTS</span></span>

### <span data-ttu-id="5148d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5148d-136">System.String</span></span>

### <span data-ttu-id="5148d-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5148d-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="5148d-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5148d-138">OUTPUTS</span></span>

### <span data-ttu-id="5148d-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="5148d-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="5148d-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5148d-140">NOTES</span></span>
* <span data-ttu-id="5148d-141">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="5148d-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="5148d-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5148d-142">RELATED LINKS</span></span>

[<span data-ttu-id="5148d-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="5148d-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="5148d-144">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="5148d-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
