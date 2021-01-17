---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374644"
---
# <span data-ttu-id="4a2da-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a2da-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="4a2da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a2da-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2da-103">Entfernt eine oder mehrere Datenbanken aus einer Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4a2da-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="4a2da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a2da-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a2da-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a2da-105">DESCRIPTION</span></span>
<span data-ttu-id="4a2da-106">Entfernt eine oder mehrere Datenbanken aus der angegebenen Azure SQL-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4a2da-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="4a2da-107">Die Datenbanken und Replikationsbeziehungen bleiben intakt, sind aber nicht mehr über die Failovergruppenendpunkte zugänglich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="4a2da-108">Zum Abrufen von Datenbankobjekten, mit denen der Parameter "-Database" auffüllt werden soll, verwenden Sie (beispielsweise) das Get-AzSqlDatabase Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a2da-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="4a2da-109">Der primäre Server der Failovergruppe muss zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a2da-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="4a2da-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a2da-110">EXAMPLES</span></span>

### <span data-ttu-id="4a2da-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a2da-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="4a2da-112">Mit diesem Befehl wird eine Datenbank aus einer Failovergruppe entfernt, indem sie in die Datenbank einpipeniert wird.</span><span class="sxs-lookup"><span data-stu-id="4a2da-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="4a2da-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4a2da-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="4a2da-114">Mit diesem Befehl werden alle Datenbanken aus einer Failovergruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="4a2da-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="4a2da-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4a2da-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="4a2da-116">Mit diesem Befehl werden alle Datenbanken in einem Pool mit Bändern aus einer Failovergruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="4a2da-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="4a2da-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a2da-117">PARAMETERS</span></span>

### <span data-ttu-id="4a2da-118">-Database</span><span class="sxs-lookup"><span data-stu-id="4a2da-118">-Database</span></span>
<span data-ttu-id="4a2da-119">Mindestens eine Azure SQL Datenbanken auf dem primären Server der Failovergruppe, der aus der Failovergruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a2da-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a2da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a2da-120">-DefaultProfile</span></span>
<span data-ttu-id="4a2da-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4a2da-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a2da-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4a2da-122">-FailoverGroupName</span></span>
<span data-ttu-id="4a2da-123">Der Name der Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4a2da-123">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a2da-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4a2da-124">-Force</span></span>
<span data-ttu-id="4a2da-125">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="4a2da-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="4a2da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a2da-126">-ResourceGroupName</span></span>
<span data-ttu-id="4a2da-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a2da-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a2da-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a2da-128">-ServerName</span></span>
<span data-ttu-id="4a2da-129">Der Name des primären Azure SQL Datenbankservers der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4a2da-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4a2da-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a2da-130">-Confirm</span></span>
<span data-ttu-id="4a2da-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a2da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a2da-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a2da-132">-WhatIf</span></span>
<span data-ttu-id="4a2da-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a2da-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a2da-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a2da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a2da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2da-135">CommonParameters</span></span>
<span data-ttu-id="4a2da-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a2da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2da-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a2da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2da-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a2da-138">INPUTS</span></span>

### <span data-ttu-id="4a2da-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4a2da-139">System.String</span></span>

### <span data-ttu-id="4a2da-140">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4a2da-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4a2da-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a2da-141">OUTPUTS</span></span>

### <span data-ttu-id="4a2da-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4a2da-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4a2da-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a2da-143">NOTES</span></span>

## <span data-ttu-id="4a2da-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a2da-144">RELATED LINKS</span></span>

[<span data-ttu-id="4a2da-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a2da-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a2da-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a2da-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a2da-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a2da-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a2da-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a2da-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4a2da-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a2da-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a2da-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a2da-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a2da-151">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="4a2da-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
