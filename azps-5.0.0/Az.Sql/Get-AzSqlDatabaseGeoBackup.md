---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179808"
---
# <span data-ttu-id="4325e-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="4325e-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="4325e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4325e-102">SYNOPSIS</span></span>
<span data-ttu-id="4325e-103">Ruft eine Geo-redundante Sicherung einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4325e-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="4325e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4325e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4325e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4325e-105">DESCRIPTION</span></span>
<span data-ttu-id="4325e-106">Das Cmdlet " **Get-AzSqlDatabaseGeoBackup** " Ruft eine angegebene Geo-redundante Sicherung einer SQL-Datenbank oder aller verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="4325e-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="4325e-107">Bei einer Geo-redundanten Sicherung handelt es sich um eine wiederherstellbare Ressource, die Datendateien von einem separaten geografischen Standort verwendet.</span><span class="sxs-lookup"><span data-stu-id="4325e-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="4325e-108">Sie können Geo-Restore verwenden, um eine Geo-redundante Sicherung bei einem regionalen Ausfall wiederherzustellen, um Ihre Datenbank in einer neuen Region wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="4325e-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="4325e-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4325e-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4325e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4325e-110">EXAMPLES</span></span>

### <span data-ttu-id="4325e-111">Beispiel 1: Abrufen aller Geo-redundanten Sicherungen auf einem Server</span><span class="sxs-lookup"><span data-stu-id="4325e-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="4325e-112">Dieser Befehl ruft alle verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="4325e-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="4325e-113">Beispiel 2: Abrufen einer angegebenen Geo-redundanten Sicherung</span><span class="sxs-lookup"><span data-stu-id="4325e-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="4325e-114">Mit diesem Befehl wird die Daten Bank Geo-redundante Sicherung mit dem Namen ContosoDatabase abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4325e-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="4325e-115">Beispiel 3: Abrufen aller Geo-redundanten Sicherungen auf einem Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="4325e-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="4325e-116">Dieser Befehl ruft alle verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab, die mit "Contoso" beginnen.</span><span class="sxs-lookup"><span data-stu-id="4325e-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="4325e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4325e-117">PARAMETERS</span></span>

### <span data-ttu-id="4325e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4325e-118">-DatabaseName</span></span>
<span data-ttu-id="4325e-119">Gibt den Namen der Datenbank an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4325e-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4325e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4325e-120">-DefaultProfile</span></span>
<span data-ttu-id="4325e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4325e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4325e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4325e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4325e-123">Gibt den Namen der Ressourcengruppe an, der der SQL-Datenbankserver zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4325e-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="4325e-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="4325e-124">-ServerName</span></span>
<span data-ttu-id="4325e-125">Gibt den Namen des Servers an, der die wiederherzustellende Sicherung hostet.</span><span class="sxs-lookup"><span data-stu-id="4325e-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="4325e-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4325e-126">-Confirm</span></span>
<span data-ttu-id="4325e-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4325e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4325e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4325e-128">-WhatIf</span></span>
<span data-ttu-id="4325e-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4325e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4325e-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4325e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4325e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4325e-131">CommonParameters</span></span>
<span data-ttu-id="4325e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4325e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4325e-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4325e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4325e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4325e-134">INPUTS</span></span>

### <span data-ttu-id="4325e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4325e-135">System.String</span></span>

## <span data-ttu-id="4325e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4325e-136">OUTPUTS</span></span>

### <span data-ttu-id="4325e-137">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="4325e-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="4325e-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4325e-138">NOTES</span></span>

## <span data-ttu-id="4325e-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4325e-139">RELATED LINKS</span></span>

[<span data-ttu-id="4325e-140">Übersicht: Cloud Business Continuity und Datenbank-Disaster Recovery mit SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="4325e-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="4325e-141">Wiederherstellen einer Azure SQL-Datenbank aus einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="4325e-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="4325e-142">Wiederherstellen – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4325e-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="4325e-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="4325e-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
