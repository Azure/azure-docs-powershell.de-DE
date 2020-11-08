---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173490"
---
# <span data-ttu-id="4a053-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a053-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="4a053-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a053-102">SYNOPSIS</span></span>
<span data-ttu-id="4a053-103">Fügt eine oder mehrere Datenbanken zu einer Azure SQL-Daten Bank Failover-Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="4a053-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="4a053-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a053-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a053-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a053-105">DESCRIPTION</span></span>
<span data-ttu-id="4a053-106">Fügt eine oder mehrere Datenbanken auf dem primären Server einer Azure SQL-Datenbankfailover-Gruppe zu dieser failovergruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="4a053-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="4a053-107">Die Datenbanken dürfen keine sekundären Datenbanken in vorhandenen Replikationsbeziehungen sein.</span><span class="sxs-lookup"><span data-stu-id="4a053-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="4a053-108">Mit dem Befehl wird die Geo-Replikation aller hinzugefügten Datenbanken zum sekundären Server der Failover-Gruppe gestartet.</span><span class="sxs-lookup"><span data-stu-id="4a053-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="4a053-109">Verwenden Sie zum Abrufen von Datenbankobjekten, mit denen der "-Database"-Parameter gefüllt werden soll, das Get-AzSqlDatabase-Cmdlet (zum Beispiel).</span><span class="sxs-lookup"><span data-stu-id="4a053-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="4a053-110">Der primäre Server der failovergruppe muss verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4a053-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="4a053-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a053-111">EXAMPLES</span></span>

### <span data-ttu-id="4a053-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a053-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="4a053-113">Mit diesem Befehl wird eine Datenbank zu einer failovergruppe hinzugefügt, indem Sie in verrohrt wird.</span><span class="sxs-lookup"><span data-stu-id="4a053-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="4a053-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4a053-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="4a053-115">Mit diesem Befehl werden alle Datenbanken auf einem Server zu einer failovergruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4a053-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="4a053-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4a053-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="4a053-117">Mit diesem Befehl werden alle Datenbanken in einem elastischen Pool zu einer failovergruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4a053-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="4a053-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a053-118">PARAMETERS</span></span>

### <span data-ttu-id="4a053-119">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="4a053-119">-Database</span></span>
<span data-ttu-id="4a053-120">Eine oder mehrere Azure SQL-Datenbanken auf dem primären Server der failovergruppe, die der Gruppe Failover hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a053-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="4a053-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a053-121">-DefaultProfile</span></span>
<span data-ttu-id="4a053-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4a053-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a053-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4a053-123">-FailoverGroupName</span></span>
<span data-ttu-id="4a053-124">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4a053-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4a053-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a053-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a053-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a053-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a053-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="4a053-127">-ServerName</span></span>
<span data-ttu-id="4a053-128">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="4a053-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4a053-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a053-129">CommonParameters</span></span>
<span data-ttu-id="4a053-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a053-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a053-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a053-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a053-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a053-132">INPUTS</span></span>

### <span data-ttu-id="4a053-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a053-133">System.String</span></span>

### <span data-ttu-id="4a053-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. Cmdlets. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4a053-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4a053-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a053-135">OUTPUTS</span></span>

### <span data-ttu-id="4a053-136">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4a053-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4a053-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a053-137">NOTES</span></span>

## <span data-ttu-id="4a053-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a053-138">RELATED LINKS</span></span>

[<span data-ttu-id="4a053-139">Neu – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a053-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a053-140">Satz-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a053-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a053-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a053-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a053-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a053-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4a053-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a053-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a053-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a053-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a053-145">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="4a053-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
