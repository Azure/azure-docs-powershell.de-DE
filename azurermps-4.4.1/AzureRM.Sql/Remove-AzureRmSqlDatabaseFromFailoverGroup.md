---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: b796d1247d1f8a49316431ca944ac6cd1fb77d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665256"
---
# <span data-ttu-id="95815-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95815-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="95815-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95815-102">SYNOPSIS</span></span>
<span data-ttu-id="95815-103">Entfernt mindestens eine Datenbank aus einer Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="95815-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95815-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95815-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95815-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95815-105">DESCRIPTION</span></span>
<span data-ttu-id="95815-106">Entfernt mindestens eine Datenbank aus der angegebenen Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="95815-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="95815-107">Die Datenbanken und Replikationsbeziehungen bleiben intakt, werden aber nicht mehr über die Failovercluster-Endpunkte zugänglich sein.</span><span class="sxs-lookup"><span data-stu-id="95815-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="95815-108">Verwenden Sie zum Abrufen von Datenbankobjekten, mit denen der "-Database"-Parameter gefüllt werden soll, das Get-AzureRmSqlDatabase-Cmdlet (zum Beispiel).</span><span class="sxs-lookup"><span data-stu-id="95815-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="95815-109">Der primäre Server der failovergruppe muss verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="95815-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="95815-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95815-110">EXAMPLES</span></span>

### <span data-ttu-id="95815-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95815-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="95815-112">Mit diesem Befehl wird eine Datenbank aus einer failovergruppe entfernt, indem Sie in verrohrt wird.</span><span class="sxs-lookup"><span data-stu-id="95815-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="95815-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95815-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="95815-114">Mit diesem Befehl werden alle Datenbanken aus einer failovergruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="95815-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="95815-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="95815-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="95815-116">Mit diesem Befehl werden alle Datenbanken in einem elastischen Pool aus einer failovergruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="95815-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="95815-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="95815-117">PARAMETERS</span></span>

### <span data-ttu-id="95815-118">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="95815-118">-Database</span></span>
<span data-ttu-id="95815-119">Eine oder mehrere Azure SQL-Datenbanken auf dem primären Server der failovergruppe, die aus der Gruppe "Failover" entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="95815-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="95815-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="95815-120">-FailoverGroupName</span></span>
<span data-ttu-id="95815-121">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="95815-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="95815-122">-Force</span><span class="sxs-lookup"><span data-stu-id="95815-122">-Force</span></span>
<span data-ttu-id="95815-123">Bestätigungsmeldung zum Durchführen der Aktion überspringen.</span><span class="sxs-lookup"><span data-stu-id="95815-123">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="95815-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95815-124">-ResourceGroupName</span></span>
<span data-ttu-id="95815-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95815-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="95815-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="95815-126">-ServerName</span></span>
<span data-ttu-id="95815-127">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="95815-127">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="95815-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95815-128">-Confirm</span></span>
<span data-ttu-id="95815-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95815-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95815-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95815-130">-WhatIf</span></span>
<span data-ttu-id="95815-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95815-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95815-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95815-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95815-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95815-133">-DefaultProfile</span></span>
<span data-ttu-id="95815-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95815-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95815-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95815-135">CommonParameters</span></span>
<span data-ttu-id="95815-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95815-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95815-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95815-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95815-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95815-138">INPUTS</span></span>

### <span data-ttu-id="95815-139">System. String</span><span class="sxs-lookup"><span data-stu-id="95815-139">System.String</span></span>
<span data-ttu-id="95815-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="95815-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="95815-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95815-141">OUTPUTS</span></span>

### <span data-ttu-id="95815-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="95815-142">System.Object</span></span>

## <span data-ttu-id="95815-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="95815-143">NOTES</span></span>

## <span data-ttu-id="95815-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95815-144">RELATED LINKS</span></span>

[<span data-ttu-id="95815-145">Neu – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95815-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="95815-146">Satz-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95815-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="95815-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95815-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="95815-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95815-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="95815-149">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95815-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="95815-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95815-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="95815-151">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="95815-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
