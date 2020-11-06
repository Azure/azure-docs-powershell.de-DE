---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: c195215bb38152287e1aa65457a5a0ff4b5452cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497262"
---
# <span data-ttu-id="63440-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63440-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="63440-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63440-102">SYNOPSIS</span></span>
<span data-ttu-id="63440-103">Fügt eine oder mehrere Datenbanken zu einer Azure SQL-Daten Bank Failover-Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="63440-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63440-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63440-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63440-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63440-105">DESCRIPTION</span></span>
<span data-ttu-id="63440-106">Fügt eine oder mehrere Datenbanken auf dem primären Server einer Azure SQL-Datenbankfailover-Gruppe zu dieser failovergruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="63440-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="63440-107">Die Datenbanken dürfen keine sekundären Datenbanken in vorhandenen Replikationsbeziehungen sein.</span><span class="sxs-lookup"><span data-stu-id="63440-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="63440-108">Mit dem Befehl wird die Geo-Replikation aller hinzugefügten Datenbanken zum sekundären Server der Failover-Gruppe gestartet.</span><span class="sxs-lookup"><span data-stu-id="63440-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="63440-109">Verwenden Sie zum Abrufen von Datenbankobjekten, mit denen der "-Database"-Parameter gefüllt werden soll, das Get-AzureRmSqlDatabase-Cmdlet (zum Beispiel).</span><span class="sxs-lookup"><span data-stu-id="63440-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="63440-110">Der primäre Server der failovergruppe muss verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="63440-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="63440-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63440-111">EXAMPLES</span></span>

### <span data-ttu-id="63440-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63440-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="63440-113">Mit diesem Befehl wird eine Datenbank zu einer failovergruppe hinzugefügt, indem Sie in verrohrt wird.</span><span class="sxs-lookup"><span data-stu-id="63440-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="63440-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="63440-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="63440-115">Mit diesem Befehl werden alle Datenbanken auf einem Server zu einer failovergruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="63440-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="63440-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="63440-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="63440-117">Mit diesem Befehl werden alle Datenbanken in einem elastischen Pool zu einer failovergruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="63440-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="63440-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="63440-118">PARAMETERS</span></span>

### <span data-ttu-id="63440-119">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="63440-119">-Database</span></span>
<span data-ttu-id="63440-120">Eine oder mehrere Azure SQL-Datenbanken auf dem primären Server der failovergruppe, die der Gruppe Failover hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63440-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="63440-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63440-121">-DefaultProfile</span></span>
<span data-ttu-id="63440-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="63440-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63440-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="63440-123">-FailoverGroupName</span></span>
<span data-ttu-id="63440-124">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="63440-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="63440-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63440-125">-ResourceGroupName</span></span>
<span data-ttu-id="63440-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63440-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="63440-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="63440-127">-ServerName</span></span>
<span data-ttu-id="63440-128">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="63440-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="63440-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63440-129">CommonParameters</span></span>
<span data-ttu-id="63440-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63440-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63440-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63440-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63440-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63440-132">INPUTS</span></span>

### <span data-ttu-id="63440-133">System. String</span><span class="sxs-lookup"><span data-stu-id="63440-133">System.String</span></span>

### <span data-ttu-id="63440-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 4.11.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="63440-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="63440-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63440-135">OUTPUTS</span></span>

### <span data-ttu-id="63440-136">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="63440-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="63440-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="63440-137">NOTES</span></span>

## <span data-ttu-id="63440-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63440-138">RELATED LINKS</span></span>

[<span data-ttu-id="63440-139">Neu – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63440-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="63440-140">Satz-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63440-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="63440-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63440-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="63440-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63440-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="63440-143">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63440-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="63440-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63440-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="63440-145">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="63440-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
