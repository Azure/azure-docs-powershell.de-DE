---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: a8f147b4e2c8a1f4525585f8622b7195ed759022
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499338"
---
# <span data-ttu-id="e9d23-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e9d23-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="e9d23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9d23-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d23-103">Entfernt mindestens eine Datenbank aus einer Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e9d23-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9d23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9d23-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9d23-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9d23-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d23-106">Entfernt mindestens eine Datenbank aus der angegebenen Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e9d23-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="e9d23-107">Die Datenbanken und Replikationsbeziehungen bleiben intakt, werden aber nicht mehr über die Failovercluster-Endpunkte zugänglich sein.</span><span class="sxs-lookup"><span data-stu-id="e9d23-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="e9d23-108">Verwenden Sie zum Abrufen von Datenbankobjekten, mit denen der "-Database"-Parameter gefüllt werden soll, das Get-AzureRmSqlDatabase-Cmdlet (zum Beispiel).</span><span class="sxs-lookup"><span data-stu-id="e9d23-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="e9d23-109">Der primäre Server der failovergruppe muss verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e9d23-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="e9d23-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9d23-110">EXAMPLES</span></span>

### <span data-ttu-id="e9d23-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9d23-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="e9d23-112">Mit diesem Befehl wird eine Datenbank aus einer failovergruppe entfernt, indem Sie in verrohrt wird.</span><span class="sxs-lookup"><span data-stu-id="e9d23-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="e9d23-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e9d23-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="e9d23-114">Mit diesem Befehl werden alle Datenbanken aus einer failovergruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9d23-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="e9d23-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e9d23-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="e9d23-116">Mit diesem Befehl werden alle Datenbanken in einem elastischen Pool aus einer failovergruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9d23-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="e9d23-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9d23-117">PARAMETERS</span></span>

### <span data-ttu-id="e9d23-118">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="e9d23-118">-Database</span></span>
<span data-ttu-id="e9d23-119">Eine oder mehrere Azure SQL-Datenbanken auf dem primären Server der failovergruppe, die aus der Gruppe "Failover" entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e9d23-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="e9d23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d23-120">-DefaultProfile</span></span>
<span data-ttu-id="e9d23-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e9d23-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9d23-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d23-122">-FailoverGroupName</span></span>
<span data-ttu-id="e9d23-123">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e9d23-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="e9d23-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e9d23-124">-Force</span></span>
<span data-ttu-id="e9d23-125">Bestätigungsmeldung zum Durchführen der Aktion überspringen.</span><span class="sxs-lookup"><span data-stu-id="e9d23-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="e9d23-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d23-126">-ResourceGroupName</span></span>
<span data-ttu-id="e9d23-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e9d23-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9d23-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="e9d23-128">-ServerName</span></span>
<span data-ttu-id="e9d23-129">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="e9d23-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="e9d23-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9d23-130">-Confirm</span></span>
<span data-ttu-id="e9d23-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9d23-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9d23-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d23-132">-WhatIf</span></span>
<span data-ttu-id="e9d23-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9d23-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9d23-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9d23-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9d23-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d23-135">CommonParameters</span></span>
<span data-ttu-id="e9d23-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d23-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d23-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d23-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d23-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9d23-138">INPUTS</span></span>

### <span data-ttu-id="e9d23-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e9d23-139">System.String</span></span>

### <span data-ttu-id="e9d23-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 4.11.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e9d23-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e9d23-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9d23-141">OUTPUTS</span></span>

### <span data-ttu-id="e9d23-142">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e9d23-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="e9d23-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9d23-143">NOTES</span></span>

## <span data-ttu-id="e9d23-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9d23-144">RELATED LINKS</span></span>

[<span data-ttu-id="e9d23-145">Neu – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e9d23-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e9d23-146">Satz-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e9d23-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e9d23-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e9d23-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e9d23-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e9d23-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="e9d23-149">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e9d23-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e9d23-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e9d23-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e9d23-151">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="e9d23-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
