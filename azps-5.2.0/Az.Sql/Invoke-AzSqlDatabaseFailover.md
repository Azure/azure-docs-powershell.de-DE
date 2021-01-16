---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364312"
---
# <span data-ttu-id="19866-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="19866-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="19866-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19866-102">SYNOPSIS</span></span>
<span data-ttu-id="19866-103">Failover einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="19866-103">Failovers a database.</span></span>

## <span data-ttu-id="19866-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19866-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19866-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19866-105">DESCRIPTION</span></span>
<span data-ttu-id="19866-106">Das Invoke-AzSqlDatabaseFailover-Cmdlet-Failover einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="19866-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="19866-107">Befindet sich die Datenbank in einem Pool mit Beeinträchtigungen, erfolgt mit diesem Befehl ein Failover der angegebenen Datenbank, ohne dass dies Auswirkungen auf die anderen Datenbanken im gleichen Pool hat.</span><span class="sxs-lookup"><span data-stu-id="19866-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="19866-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19866-108">EXAMPLES</span></span>

### <span data-ttu-id="19866-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19866-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="19866-110">Mit diesem Befehl wird ein Failover des primären Replikats der Datenbank mit dem Namen "Database01" auf dem Server "Server01" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19866-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="19866-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="19866-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="19866-112">Mit diesem Befehl wird ein Failover der lesbaren sekundären Replikate der Datenbank mit dem Namen "Database01" auf dem Server "Server01" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19866-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="19866-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19866-113">PARAMETERS</span></span>

### <span data-ttu-id="19866-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19866-114">-AsJob</span></span>
<span data-ttu-id="19866-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="19866-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19866-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19866-116">-DatabaseName</span></span>
<span data-ttu-id="19866-117">Der Name der Azure-SQL-Datenbank für den Failover.</span><span class="sxs-lookup"><span data-stu-id="19866-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="19866-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19866-118">-DefaultProfile</span></span>
<span data-ttu-id="19866-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19866-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19866-120">-Force</span><span class="sxs-lookup"><span data-stu-id="19866-120">-Force</span></span>
<span data-ttu-id="19866-121">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="19866-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="19866-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19866-122">-PassThru</span></span>
<span data-ttu-id="19866-123">Bei erfolgreicher Ausführung wird "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19866-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="19866-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="19866-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19866-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="19866-125">-ReadableSecondary</span></span>
<span data-ttu-id="19866-126">Failover der lesbaren sekundären Replikate anstelle der primären Standardreplikate</span><span class="sxs-lookup"><span data-stu-id="19866-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="19866-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19866-127">-ResourceGroupName</span></span>
<span data-ttu-id="19866-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="19866-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="19866-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="19866-129">-ServerName</span></span>
<span data-ttu-id="19866-130">Der Name des Azure SQL Datenbankservers, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="19866-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="19866-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19866-131">-Confirm</span></span>
<span data-ttu-id="19866-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19866-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19866-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="19866-133">-WhatIf</span></span>
<span data-ttu-id="19866-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19866-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19866-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19866-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19866-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19866-136">CommonParameters</span></span>
<span data-ttu-id="19866-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19866-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19866-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19866-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19866-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19866-139">INPUTS</span></span>

### <span data-ttu-id="19866-140">System.String</span><span class="sxs-lookup"><span data-stu-id="19866-140">System.String</span></span>

## <span data-ttu-id="19866-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19866-141">OUTPUTS</span></span>

## <span data-ttu-id="19866-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="19866-142">NOTES</span></span>

## <span data-ttu-id="19866-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="19866-143">RELATED LINKS</span></span>

[<span data-ttu-id="19866-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19866-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="19866-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="19866-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="19866-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19866-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="19866-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19866-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="19866-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19866-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="19866-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19866-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="19866-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19866-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="19866-151">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="19866-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
