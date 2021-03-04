---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 0af12c967dbbc65b37619ed837da1b8f778ab1db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931483"
---
# <span data-ttu-id="f1a2b-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="f1a2b-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="f1a2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a2b-103">Failover für einen Pool mit einem Flexiblen Pool.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="f1a2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1a2b-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a2b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a2b-106">Das Invoke-AzSqlElasticPoolFailover-Cmdlet failovert einen Pool mit einem Flexiblen Pool.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="f1a2b-107">Nach dem Ausführen dieses Cmdlets tritt ein Failover für alle Datenbanken im Pool für den Bänder auf.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="f1a2b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1a2b-108">EXAMPLES</span></span>

### <span data-ttu-id="f1a2b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1a2b-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f1a2b-110">Dieser Befehl über failovert den Pool mit dem Namen "ElasticPool01" auf dem Server mit dem Namen "Server01".</span><span class="sxs-lookup"><span data-stu-id="f1a2b-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="f1a2b-111">Dies bedeutet, dass ein Failover für alle Datenbanken im Pool mit dem Namen "ElasticPool01" erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="f1a2b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1a2b-112">PARAMETERS</span></span>

### <span data-ttu-id="f1a2b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1a2b-113">-AsJob</span></span>
<span data-ttu-id="f1a2b-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1a2b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1a2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a2b-115">-DefaultProfile</span></span>
<span data-ttu-id="f1a2b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a2b-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f1a2b-117">-ElasticPoolName</span></span>
<span data-ttu-id="f1a2b-118">Der Name des zu entfernen SQL Azure-Pool.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="f1a2b-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f1a2b-119">-Force</span></span>
<span data-ttu-id="f1a2b-120">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="f1a2b-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f1a2b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1a2b-121">-PassThru</span></span>
<span data-ttu-id="f1a2b-122">Gibt bei erfolgreicher Ausführung den Wert "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="f1a2b-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1a2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1a2b-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1a2b-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="f1a2b-126">-ServerName</span></span>
<span data-ttu-id="f1a2b-127">Der Name des Azure-SQL Server der "Pool für den flexiblen Pool" ist in.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="f1a2b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1a2b-128">-Confirm</span></span>
<span data-ttu-id="f1a2b-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a2b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a2b-130">-WhatIf</span></span>
<span data-ttu-id="f1a2b-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1a2b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a2b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a2b-133">CommonParameters</span></span>
<span data-ttu-id="f1a2b-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a2b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a2b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1a2b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a2b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1a2b-136">INPUTS</span></span>

### <span data-ttu-id="f1a2b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f1a2b-137">System.String</span></span>

## <span data-ttu-id="f1a2b-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1a2b-138">OUTPUTS</span></span>

## <span data-ttu-id="f1a2b-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1a2b-139">NOTES</span></span>

## <span data-ttu-id="f1a2b-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1a2b-140">RELATED LINKS</span></span>

[<span data-ttu-id="f1a2b-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1a2b-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="f1a2b-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f1a2b-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="f1a2b-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f1a2b-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="f1a2b-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="f1a2b-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="f1a2b-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1a2b-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="f1a2b-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1a2b-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="f1a2b-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1a2b-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="f1a2b-148">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="f1a2b-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)