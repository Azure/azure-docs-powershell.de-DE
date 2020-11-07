---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 676464cd13d253d152a2a5390c291c59d2ff086b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825852"
---
# <span data-ttu-id="95c05-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="95c05-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="95c05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95c05-102">SYNOPSIS</span></span>
<span data-ttu-id="95c05-103">Aktualisiert den automatischen Ausführungsstatus eines Azure SQL Elastic Pool Advisor.</span><span class="sxs-lookup"><span data-stu-id="95c05-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="95c05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95c05-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95c05-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95c05-105">DESCRIPTION</span></span>
<span data-ttu-id="95c05-106">Das Cmdlet " **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** " legt die Auto Execute-Eigenschaft für einen Azure SQL Elastic Pool Advisor fest.</span><span class="sxs-lookup"><span data-stu-id="95c05-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="95c05-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95c05-107">EXAMPLES</span></span>

### <span data-ttu-id="95c05-108">Beispiel 1: Aktivieren der automatischen Ausführung für einen Ratgeber</span><span class="sxs-lookup"><span data-stu-id="95c05-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="95c05-109">Dieser Befehl legt den automatischen Ausführungsstatus eines Ratgebers mit dem Namen CreateIndex auf Enabled fest.</span><span class="sxs-lookup"><span data-stu-id="95c05-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="95c05-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95c05-110">PARAMETERS</span></span>

### <span data-ttu-id="95c05-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="95c05-111">-AdvisorName</span></span>
<span data-ttu-id="95c05-112">Gibt den Namen des Beraters an, für den das Cmdlet den automatischen Ausführungsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="95c05-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="95c05-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="95c05-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="95c05-114">Gibt einen neuen Wert an, mit dem dieses Cmdlet den automatischen Ausführungsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="95c05-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="95c05-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="95c05-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95c05-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="95c05-116">Enabled</span></span>
- <span data-ttu-id="95c05-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="95c05-117">Disabled</span></span>
- <span data-ttu-id="95c05-118">Standard</span><span class="sxs-lookup"><span data-stu-id="95c05-118">Default</span></span>

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

### <span data-ttu-id="95c05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c05-119">-DefaultProfile</span></span>
<span data-ttu-id="95c05-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="95c05-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95c05-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="95c05-121">-ElasticPoolName</span></span>
<span data-ttu-id="95c05-122">Gibt den Namen des elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="95c05-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="95c05-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c05-123">-ResourceGroupName</span></span>
<span data-ttu-id="95c05-124">Gibt den Namen der Ressourcengruppe des Servers an, der diesen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="95c05-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="95c05-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="95c05-125">-ServerName</span></span>
<span data-ttu-id="95c05-126">Gibt den Namen des Servers an, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="95c05-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="95c05-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95c05-127">-Confirm</span></span>
<span data-ttu-id="95c05-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95c05-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95c05-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c05-129">-WhatIf</span></span>
<span data-ttu-id="95c05-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95c05-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95c05-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95c05-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95c05-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c05-132">CommonParameters</span></span>
<span data-ttu-id="95c05-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c05-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c05-134">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95c05-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c05-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95c05-135">INPUTS</span></span>

### <span data-ttu-id="95c05-136">System. String</span><span class="sxs-lookup"><span data-stu-id="95c05-136">System.String</span></span>

### <span data-ttu-id="95c05-137">Microsoft. Azure. Commands. SQL. Advisor. Cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="95c05-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="95c05-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95c05-138">OUTPUTS</span></span>

### <span data-ttu-id="95c05-139">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="95c05-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="95c05-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="95c05-140">NOTES</span></span>
* <span data-ttu-id="95c05-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Elastic Pool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="95c05-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="95c05-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95c05-142">RELATED LINKS</span></span>

[<span data-ttu-id="95c05-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="95c05-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="95c05-144">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="95c05-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
