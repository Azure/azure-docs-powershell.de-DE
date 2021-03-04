---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 5ba899cba4c45c3d13858d8e274b333d613106dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922659"
---
# <span data-ttu-id="2ffa4-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2ffa4-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="2ffa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ffa4-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffa4-103">Ruft eine georedundant gesicherte Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="2ffa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ffa4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ffa4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ffa4-105">DESCRIPTION</span></span>
<span data-ttu-id="2ffa4-106">Das **Get-AzSqlDatabaseGeoBackup-Cmdlet** ruft eine angegebene georedundierte Sicherung einer SQL-Datenbank oder aller verfügbaren georedundierten Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="2ffa4-107">Eine georedundant gesicherte Ressource ist eine restorable Ressource, die Datendateien von einem separaten geografischen Speicherort verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="2ffa4-108">Sie können Geo-Restore verwenden, um eine georedundant gesicherte Sicherung im Fall eines regionalen Ausfalls wiederherzustellen, um Ihre Datenbank in einer neuen Region wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="2ffa4-109">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2ffa4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ffa4-110">EXAMPLES</span></span>

### <span data-ttu-id="2ffa4-111">Beispiel 1: Erhalten aller georedundanter Sicherungen auf einem Server</span><span class="sxs-lookup"><span data-stu-id="2ffa4-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="2ffa4-112">Dieser Befehl ruft alle verfügbaren georedundanziellen Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="2ffa4-113">Beispiel 2: Erhalten einer angegebenen georedundanzen Sicherung</span><span class="sxs-lookup"><span data-stu-id="2ffa4-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="2ffa4-114">Dieser Befehl ruft die georedundierte Datenbanksicherung namens ContosoDatabase ab.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="2ffa4-115">Beispiel 3: Erhalten aller georedundanter Sicherungen auf einem Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="2ffa4-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="2ffa4-116">Dieser Befehl ruft alle verfügbaren geo redundanten Sicherungen auf einem angegebenen Server ab, die mit "Contoso" beginnen.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="2ffa4-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2ffa4-117">PARAMETERS</span></span>

### <span data-ttu-id="2ffa4-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ffa4-118">-DatabaseName</span></span>
<span data-ttu-id="2ffa4-119">Gibt den Namen der zu erhaltenden Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-119">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="2ffa4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffa4-120">-DefaultProfile</span></span>
<span data-ttu-id="2ffa4-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2ffa4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ffa4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ffa4-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ffa4-123">Gibt den Namen der Ressourcengruppe an, der der SQL Datenbankserver zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="2ffa4-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="2ffa4-124">-ServerName</span></span>
<span data-ttu-id="2ffa4-125">Gibt den Namen des Servers an, der die wiederherzustellende Sicherung hostet.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="2ffa4-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ffa4-126">-Confirm</span></span>
<span data-ttu-id="2ffa4-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ffa4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ffa4-128">-WhatIf</span></span>
<span data-ttu-id="2ffa4-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ffa4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ffa4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffa4-131">CommonParameters</span></span>
<span data-ttu-id="2ffa4-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ffa4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffa4-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ffa4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffa4-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ffa4-134">INPUTS</span></span>

### <span data-ttu-id="2ffa4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2ffa4-135">System.String</span></span>

## <span data-ttu-id="2ffa4-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ffa4-136">OUTPUTS</span></span>

### <span data-ttu-id="2ffa4-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="2ffa4-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="2ffa4-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2ffa4-138">NOTES</span></span>

## <span data-ttu-id="2ffa4-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2ffa4-139">RELATED LINKS</span></span>

[<span data-ttu-id="2ffa4-140">Übersicht: Cloud business continuity and database disaster recovery with SQL Database</span><span class="sxs-lookup"><span data-stu-id="2ffa4-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="2ffa4-141">Wiederherstellen einer Azure SQL-Datenbank nach einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="2ffa4-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="2ffa4-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2ffa4-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="2ffa4-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="2ffa4-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
