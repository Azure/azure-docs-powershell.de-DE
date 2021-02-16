---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144212"
---
# <span data-ttu-id="bd1f2-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="bd1f2-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="bd1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd1f2-103">Ruft eine geo redundante Sicherung einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="bd1f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd1f2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd1f2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd1f2-105">DESCRIPTION</span></span>
<span data-ttu-id="bd1f2-106">Das **Cmdlet "Get-AzSqlDatabaseGeoBackup"** ruft eine angegebene georedundierte Sicherung einer SQL-Datenbank oder alle verfügbaren georedundierten Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="bd1f2-107">Eine georedundable Sicherung ist eine wiederversetzbare Ressource, die Datendateien von einem separaten geografischen Standort verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="bd1f2-108">Sie können eine Geo-Restore für den Fall eines regionalen Ausfalls zum Wiederherstellen einer georedundanzen Sicherung verwenden, um die Datenbank in eine neue Region wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="bd1f2-109">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bd1f2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd1f2-110">EXAMPLES</span></span>

### <span data-ttu-id="bd1f2-111">Beispiel 1: Alle georedundanzen Sicherungen auf einem Server erhalten</span><span class="sxs-lookup"><span data-stu-id="bd1f2-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="bd1f2-112">Dieser Befehl ruft alle verfügbaren georedundanzen Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="bd1f2-113">Beispiel 2: Erhalten einer angegebenen georedundanzen Sicherung</span><span class="sxs-lookup"><span data-stu-id="bd1f2-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="bd1f2-114">Dieser Befehl ruft die georedundierte Datenbanksicherung namens "ContosoDatabase" ab.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="bd1f2-115">Beispiel 3: Erhalten aller georedundanzen Sicherungen auf einem Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="bd1f2-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="bd1f2-116">Dieser Befehl ruft alle verfügbaren georedundanzen Sicherungen auf einem angegebenen Server ab, die mit "Contoso" beginnen.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="bd1f2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd1f2-117">PARAMETERS</span></span>

### <span data-ttu-id="bd1f2-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd1f2-118">-DatabaseName</span></span>
<span data-ttu-id="bd1f2-119">Gibt den Namen der datenbank an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-119">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="bd1f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd1f2-120">-DefaultProfile</span></span>
<span data-ttu-id="bd1f2-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bd1f2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd1f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd1f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd1f2-123">Gibt den Namen der Ressourcengruppe an, der der SQL Datenbankserver zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="bd1f2-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd1f2-124">-ServerName</span></span>
<span data-ttu-id="bd1f2-125">Gibt den Namen des Servers an, der die wiederherzustellende Sicherung hostet.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="bd1f2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd1f2-126">-Confirm</span></span>
<span data-ttu-id="bd1f2-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd1f2-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bd1f2-128">-WhatIf</span></span>
<span data-ttu-id="bd1f2-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd1f2-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd1f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd1f2-131">CommonParameters</span></span>
<span data-ttu-id="bd1f2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd1f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd1f2-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd1f2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd1f2-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd1f2-134">INPUTS</span></span>

### <span data-ttu-id="bd1f2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bd1f2-135">System.String</span></span>

## <span data-ttu-id="bd1f2-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd1f2-136">OUTPUTS</span></span>

### <span data-ttu-id="bd1f2-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="bd1f2-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="bd1f2-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bd1f2-138">NOTES</span></span>

## <span data-ttu-id="bd1f2-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bd1f2-139">RELATED LINKS</span></span>

[<span data-ttu-id="bd1f2-140">Übersicht: Cloud-Geschäftskontinuität und Datenbank-Notfallwiederherstellung mit SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="bd1f2-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="bd1f2-141">Wiederherstellen einer Azure SQL-Datenbank nach einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="bd1f2-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="bd1f2-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd1f2-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="bd1f2-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="bd1f2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
