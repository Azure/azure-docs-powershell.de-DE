---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: f22730e39a1b53cfea8181163dd770c67dc598a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481998"
---
# <span data-ttu-id="5ab1b-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="5ab1b-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="5ab1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ab1b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab1b-103">Ruft eine Geo-redundante Sicherung einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ab1b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab1b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ab1b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab1b-106">Das Cmdlet " **Get-AzureRMSqlDatabaseGeoBackup** " Ruft eine angegebene Geo-redundante Sicherung einer SQL-Datenbank oder aller verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="5ab1b-107">Bei einer Geo-redundanten Sicherung handelt es sich um eine wiederherstellbare Ressource, die Datendateien von einem separaten geografischen Standort verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="5ab1b-108">Sie können Geo-Restore verwenden, um eine Geo-redundante Sicherung bei einem regionalen Ausfall wiederherzustellen, um Ihre Datenbank in einer neuen Region wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="5ab1b-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5ab1b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ab1b-110">EXAMPLES</span></span>

### <span data-ttu-id="5ab1b-111">Beispiel 1: Abrufen aller Geo-redundanten Sicherungen auf einem Server</span><span class="sxs-lookup"><span data-stu-id="5ab1b-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="5ab1b-112">Dieser Befehl ruft alle verfügbaren Geo-redundanten Sicherungen auf einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="5ab1b-113">Beispiel 2: Abrufen einer angegebenen Geo-redundanten Sicherung</span><span class="sxs-lookup"><span data-stu-id="5ab1b-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="5ab1b-114">Mit diesem Befehl wird die Daten Bank Geo-redundante Sicherung mit dem Namen ContosoDatabase abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="5ab1b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ab1b-115">PARAMETERS</span></span>

### <span data-ttu-id="5ab1b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ab1b-116">-DatabaseName</span></span>
<span data-ttu-id="5ab1b-117">Gibt den Namen der Datenbank an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-117">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="5ab1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab1b-118">-DefaultProfile</span></span>
<span data-ttu-id="5ab1b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5ab1b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ab1b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab1b-120">-ResourceGroupName</span></span>
<span data-ttu-id="5ab1b-121">Gibt den Namen der Ressourcengruppe an, der der SQL-Datenbankserver zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-121">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="5ab1b-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="5ab1b-122">-ServerName</span></span>
<span data-ttu-id="5ab1b-123">Gibt den Namen des Servers an, der die wiederherzustellende Sicherung hostet.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-123">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="5ab1b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5ab1b-124">-Confirm</span></span>
<span data-ttu-id="5ab1b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab1b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab1b-126">-WhatIf</span></span>
<span data-ttu-id="5ab1b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab1b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab1b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab1b-129">CommonParameters</span></span>
<span data-ttu-id="5ab1b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab1b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab1b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab1b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab1b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ab1b-132">INPUTS</span></span>

### <span data-ttu-id="5ab1b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab1b-133">System.String</span></span>

## <span data-ttu-id="5ab1b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ab1b-134">OUTPUTS</span></span>

### <span data-ttu-id="5ab1b-135">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="5ab1b-135">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="5ab1b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ab1b-136">NOTES</span></span>

## <span data-ttu-id="5ab1b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ab1b-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ab1b-138">Übersicht: Cloud Business Continuity und Datenbank-Disaster Recovery mit SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5ab1b-138">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="5ab1b-139">Wiederherstellen einer Azure SQL-Datenbank aus einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="5ab1b-139">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="5ab1b-140">Wiederherstellen – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ab1b-140">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="5ab1b-141">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5ab1b-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
