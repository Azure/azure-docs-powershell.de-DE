---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156196"
---
# <span data-ttu-id="d75a7-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d75a7-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="d75a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d75a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d75a7-103">Fügt eine oder mehrere Datenbanken zu einer Azure SQL-Datenbank-Failovergruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="d75a7-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="d75a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d75a7-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d75a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d75a7-105">DESCRIPTION</span></span>
<span data-ttu-id="d75a7-106">Fügt eine oder mehrere Datenbanken auf einer Azure SQL Datenbank failover group als primären Server zu dieser Failovergruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="d75a7-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="d75a7-107">Die Datenbanken dürfen keine sekundären Datenbanken in vorhandenen Replikationsbeziehungen sein.</span><span class="sxs-lookup"><span data-stu-id="d75a7-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="d75a7-108">Der Befehl startet die Georeplikation aller hinzugefügten Datenbanken auf dem sekundären Server der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="d75a7-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="d75a7-109">Zum Abrufen von Datenbankobjekten, mit denen der Parameter "-Database" auffüllt werden soll, verwenden Sie (beispielsweise) das Get-AzSqlDatabase Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75a7-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="d75a7-110">Der primäre Server der Failovergruppe muss zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d75a7-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="d75a7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d75a7-111">EXAMPLES</span></span>

### <span data-ttu-id="d75a7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d75a7-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="d75a7-113">Dieser Befehl fügt einer Failovergruppe eine Datenbank hinzu, indem er sie einfügt.</span><span class="sxs-lookup"><span data-stu-id="d75a7-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="d75a7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d75a7-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="d75a7-115">Mit diesem Befehl werden alle Datenbanken auf einem Server einer Failovergruppe hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d75a7-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="d75a7-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d75a7-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="d75a7-117">Mit diesem Befehl werden alle Datenbanken in einem Pool mit Bändern zu einer Failovergruppe addiert.</span><span class="sxs-lookup"><span data-stu-id="d75a7-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="d75a7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d75a7-118">PARAMETERS</span></span>

### <span data-ttu-id="d75a7-119">-Database</span><span class="sxs-lookup"><span data-stu-id="d75a7-119">-Database</span></span>
<span data-ttu-id="d75a7-120">Mindestens eine Azure SQL Datenbanken auf dem primären Server der Failovergruppe, der der Failovergruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d75a7-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="d75a7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75a7-121">-DefaultProfile</span></span>
<span data-ttu-id="d75a7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d75a7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d75a7-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d75a7-123">-FailoverGroupName</span></span>
<span data-ttu-id="d75a7-124">Der Name der Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="d75a7-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="d75a7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d75a7-125">-ResourceGroupName</span></span>
<span data-ttu-id="d75a7-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d75a7-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d75a7-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d75a7-127">-ServerName</span></span>
<span data-ttu-id="d75a7-128">Der Name des primären Azure SQL Datenbankservers der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="d75a7-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="d75a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75a7-129">CommonParameters</span></span>
<span data-ttu-id="d75a7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75a7-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d75a7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75a7-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d75a7-132">INPUTS</span></span>

### <span data-ttu-id="d75a7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d75a7-133">System.String</span></span>

### <span data-ttu-id="d75a7-134">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d75a7-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d75a7-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d75a7-135">OUTPUTS</span></span>

### <span data-ttu-id="d75a7-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d75a7-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="d75a7-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d75a7-137">NOTES</span></span>

## <span data-ttu-id="d75a7-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d75a7-138">RELATED LINKS</span></span>

[<span data-ttu-id="d75a7-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d75a7-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d75a7-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d75a7-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d75a7-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d75a7-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d75a7-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d75a7-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d75a7-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d75a7-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d75a7-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d75a7-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d75a7-145">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="d75a7-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
