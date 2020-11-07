---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: aaf2063d82e0140e9abe07b7343a2c314e2fbd7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659290"
---
# <span data-ttu-id="fcce9-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fcce9-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="fcce9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcce9-102">SYNOPSIS</span></span>
<span data-ttu-id="fcce9-103">Fügt eine oder mehrere Datenbanken zu einer Azure SQL-Daten Bank Failover-Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="fcce9-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="fcce9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcce9-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcce9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcce9-105">DESCRIPTION</span></span>
<span data-ttu-id="fcce9-106">Fügt eine oder mehrere Datenbanken auf dem primären Server einer Azure SQL-Datenbankfailover-Gruppe zu dieser failovergruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="fcce9-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="fcce9-107">Die Datenbanken dürfen keine sekundären Datenbanken in vorhandenen Replikationsbeziehungen sein.</span><span class="sxs-lookup"><span data-stu-id="fcce9-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="fcce9-108">Mit dem Befehl wird die Geo-Replikation aller hinzugefügten Datenbanken zum sekundären Server der Failover-Gruppe gestartet.</span><span class="sxs-lookup"><span data-stu-id="fcce9-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="fcce9-109">Verwenden Sie zum Abrufen von Datenbankobjekten, mit denen der "-Database"-Parameter gefüllt werden soll, das Get-AzSqlDatabase-Cmdlet (zum Beispiel).</span><span class="sxs-lookup"><span data-stu-id="fcce9-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="fcce9-110">Der primäre Server der failovergruppe muss verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fcce9-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="fcce9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcce9-111">EXAMPLES</span></span>

### <span data-ttu-id="fcce9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcce9-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="fcce9-113">Mit diesem Befehl wird eine Datenbank zu einer failovergruppe hinzugefügt, indem Sie in verrohrt wird.</span><span class="sxs-lookup"><span data-stu-id="fcce9-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="fcce9-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fcce9-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="fcce9-115">Mit diesem Befehl werden alle Datenbanken auf einem Server zu einer failovergruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fcce9-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="fcce9-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fcce9-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="fcce9-117">Mit diesem Befehl werden alle Datenbanken in einem elastischen Pool zu einer failovergruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fcce9-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="fcce9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcce9-118">PARAMETERS</span></span>

### <span data-ttu-id="fcce9-119">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="fcce9-119">-Database</span></span>
<span data-ttu-id="fcce9-120">Eine oder mehrere Azure SQL-Datenbanken auf dem primären Server der failovergruppe, die der Gruppe Failover hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fcce9-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="fcce9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcce9-121">-DefaultProfile</span></span>
<span data-ttu-id="fcce9-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fcce9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcce9-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="fcce9-123">-FailoverGroupName</span></span>
<span data-ttu-id="fcce9-124">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fcce9-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="fcce9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcce9-125">-ResourceGroupName</span></span>
<span data-ttu-id="fcce9-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fcce9-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="fcce9-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="fcce9-127">-ServerName</span></span>
<span data-ttu-id="fcce9-128">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="fcce9-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="fcce9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcce9-129">CommonParameters</span></span>
<span data-ttu-id="fcce9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcce9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcce9-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcce9-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcce9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcce9-132">INPUTS</span></span>

### <span data-ttu-id="fcce9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fcce9-133">System.String</span></span>

### <span data-ttu-id="fcce9-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. Cmdlets. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fcce9-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fcce9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcce9-135">OUTPUTS</span></span>

### <span data-ttu-id="fcce9-136">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="fcce9-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="fcce9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcce9-137">NOTES</span></span>

## <span data-ttu-id="fcce9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcce9-138">RELATED LINKS</span></span>

[<span data-ttu-id="fcce9-139">Neu – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fcce9-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fcce9-140">Satz-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fcce9-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fcce9-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fcce9-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fcce9-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fcce9-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="fcce9-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fcce9-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fcce9-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fcce9-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fcce9-145">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="fcce9-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
