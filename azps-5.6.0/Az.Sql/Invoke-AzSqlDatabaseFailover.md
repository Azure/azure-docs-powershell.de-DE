---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 23df8f00c91cfabf4ad01b5dd641069f159eb064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936611"
---
# <span data-ttu-id="b7c2d-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="b7c2d-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="b7c2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c2d-103">Failover einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-103">Failovers a database.</span></span>

## <span data-ttu-id="b7c2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7c2d-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c2d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c2d-106">Das Invoke-AzSqlDatabaseFailover-Cmdlet failovert eine Azure-SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="b7c2d-107">Wenn sich die Datenbank in einem Pool mit einem flexiblen Pool befindet, wird mit diesem Befehl ein Failover für die angegebene Datenbank ausgeführt, ohne dass dies Auswirkungen auf die anderen Datenbanken im gleichen Pool hat.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="b7c2d-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7c2d-108">EXAMPLES</span></span>

### <span data-ttu-id="b7c2d-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7c2d-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b7c2d-110">Mit diesem Befehl wird das primäre Replikat der Datenbank mit dem Namen "Database01" auf dem Server mit dem Namen "Server01" failovern.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="b7c2d-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b7c2d-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="b7c2d-112">Mit diesem Befehl wird das lesbare sekundäre Replikat der Datenbank mit dem Namen "Database01" auf dem Server mit dem Namen "Server01" failovern.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="b7c2d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b7c2d-113">PARAMETERS</span></span>

### <span data-ttu-id="b7c2d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7c2d-114">-AsJob</span></span>
<span data-ttu-id="b7c2d-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b7c2d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7c2d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7c2d-116">-DatabaseName</span></span>
<span data-ttu-id="b7c2d-117">Der Name der Azure SQL- und Failoverdatenbank.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="b7c2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c2d-118">-DefaultProfile</span></span>
<span data-ttu-id="b7c2d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c2d-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b7c2d-120">-Force</span></span>
<span data-ttu-id="b7c2d-121">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="b7c2d-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b7c2d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7c2d-122">-PassThru</span></span>
<span data-ttu-id="b7c2d-123">Gibt bei erfolgreicher Ausführung den Wert "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="b7c2d-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7c2d-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="b7c2d-125">-ReadableSecondary</span></span>
<span data-ttu-id="b7c2d-126">Failover des lesbaren sekundären Replikats anstelle des primären Standardreplikates</span><span class="sxs-lookup"><span data-stu-id="b7c2d-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="b7c2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7c2d-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7c2d-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="b7c2d-129">-ServerName</span></span>
<span data-ttu-id="b7c2d-130">Der Name des Azure SQL Datenbankservers, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="b7c2d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7c2d-131">-Confirm</span></span>
<span data-ttu-id="b7c2d-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c2d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c2d-133">-WhatIf</span></span>
<span data-ttu-id="b7c2d-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7c2d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c2d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c2d-136">CommonParameters</span></span>
<span data-ttu-id="b7c2d-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c2d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c2d-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7c2d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c2d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7c2d-139">INPUTS</span></span>

### <span data-ttu-id="b7c2d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b7c2d-140">System.String</span></span>

## <span data-ttu-id="b7c2d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7c2d-141">OUTPUTS</span></span>

## <span data-ttu-id="b7c2d-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b7c2d-142">NOTES</span></span>

## <span data-ttu-id="b7c2d-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b7c2d-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7c2d-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7c2d-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b7c2d-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="b7c2d-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="b7c2d-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7c2d-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="b7c2d-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7c2d-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="b7c2d-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7c2d-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="b7c2d-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7c2d-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="b7c2d-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7c2d-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="b7c2d-151">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="b7c2d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
