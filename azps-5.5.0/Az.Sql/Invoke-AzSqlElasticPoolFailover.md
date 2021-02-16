---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144132"
---
# <span data-ttu-id="2fbeb-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="2fbeb-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="2fbeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fbeb-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbeb-103">Failover eines Poolpools.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="2fbeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fbeb-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fbeb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fbeb-105">DESCRIPTION</span></span>
<span data-ttu-id="2fbeb-106">Das Invoke-AzSqlElasticPoolFailover über ein Cmdlet über einen Pool im Pool.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="2fbeb-107">Nach dem Ausführen dieses Cmdlets erfolgt der Failover für alle Datenbanken im Pool des Pool.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="2fbeb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fbeb-108">EXAMPLES</span></span>

### <span data-ttu-id="2fbeb-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fbeb-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2fbeb-110">Mit diesem Befehl wird ein Failover des Pool mit dem Namen "FailoverPool01" auf dem Server "Server01" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="2fbeb-111">Dies bedeutet, dass der Failover für alle Datenbanken im Pool mit dem Namen "FailoverPool01" erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="2fbeb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fbeb-112">PARAMETERS</span></span>

### <span data-ttu-id="2fbeb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fbeb-113">-AsJob</span></span>
<span data-ttu-id="2fbeb-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2fbeb-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbeb-115">-DefaultProfile</span></span>
<span data-ttu-id="2fbeb-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fbeb-117">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2fbeb-117">-ElasticPoolName</span></span>
<span data-ttu-id="2fbeb-118">Der Name des azure SQL Pool, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbeb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2fbeb-119">-Force</span></span>
<span data-ttu-id="2fbeb-120">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="2fbeb-120">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbeb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fbeb-121">-PassThru</span></span>
<span data-ttu-id="2fbeb-122">Bei erfolgreicher Ausführung wird "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="2fbeb-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbeb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbeb-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fbeb-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2fbeb-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2fbeb-126">-ServerName</span></span>
<span data-ttu-id="2fbeb-127">Der Name des Azure SQL Server, in dem sich der Pool "Pool" befindet.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbeb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fbeb-128">-Confirm</span></span>
<span data-ttu-id="2fbeb-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbeb-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2fbeb-130">-WhatIf</span></span>
<span data-ttu-id="2fbeb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fbeb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbeb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbeb-133">CommonParameters</span></span>
<span data-ttu-id="2fbeb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fbeb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbeb-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fbeb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbeb-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fbeb-136">INPUTS</span></span>

### <span data-ttu-id="2fbeb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2fbeb-137">System.String</span></span>

## <span data-ttu-id="2fbeb-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fbeb-138">OUTPUTS</span></span>

## <span data-ttu-id="2fbeb-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fbeb-139">NOTES</span></span>

## <span data-ttu-id="2fbeb-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fbeb-140">RELATED LINKS</span></span>

[<span data-ttu-id="2fbeb-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2fbeb-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="2fbeb-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2fbeb-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="2fbeb-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2fbeb-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="2fbeb-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="2fbeb-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="2fbeb-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2fbeb-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="2fbeb-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2fbeb-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="2fbeb-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2fbeb-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="2fbeb-148">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="2fbeb-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)