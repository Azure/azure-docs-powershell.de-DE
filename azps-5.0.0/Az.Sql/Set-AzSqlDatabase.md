---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: f236c00f50d9ec74a98def114d08ab851e5a89f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177171"
---
# <span data-ttu-id="dd31a-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd31a-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="dd31a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd31a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd31a-103">Legt Eigenschaften für eine Datenbank fest oder verschiebt eine vorhandene Datenbank in einen elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="dd31a-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="dd31a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd31a-104">SYNTAX</span></span>

### <span data-ttu-id="dd31a-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd31a-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd31a-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="dd31a-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd31a-107">Umbenennen</span><span class="sxs-lookup"><span data-stu-id="dd31a-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd31a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd31a-108">DESCRIPTION</span></span>
<span data-ttu-id="dd31a-109">Das Cmdlet " **Set-AzSqlDatabase** " legt Eigenschaften für eine Datenbank in Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="dd31a-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="dd31a-110">Mit diesem Cmdlet können die Dienstebene ( *Edition* ), die Leistungsstufe ( *RequestedServiceObjectiveName* ) und die Speicher-Max-Größe ( *MaxSizeBytes* ) für die Datenbank geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dd31a-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="dd31a-111">Darüber hinaus können Sie den *ElasticPoolName* -Parameter angeben, um eine Datenbank in einen elastischen Pool zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="dd31a-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="dd31a-112">Wenn sich eine Datenbank bereits in einem elastischen Pool befindet, können Sie den *RequestedServiceObjectiveName* -Parameter verwenden, um die Datenbank aus einem elastischen Pool in eine Leistungsstufe für einzelne Datenbanken zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="dd31a-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="dd31a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd31a-113">EXAMPLES</span></span>

### <span data-ttu-id="dd31a-114">Beispiel 1: Aktualisieren einer Datenbank auf eine Standard-S0-Datenbank</span><span class="sxs-lookup"><span data-stu-id="dd31a-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="dd31a-115">Mit diesem Befehl wird eine Datenbank mit dem Namen database01 in eine Standard-S0-Datenbank auf einem Server mit dem Namen Server01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dd31a-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="dd31a-116">Beispiel 2: Hinzufügen einer Datenbank zu einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="dd31a-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="dd31a-117">Dieser Befehl fügt dem elastischen Pool mit dem Namen ElasticPool01, der auf dem Server mit dem Namen Server01 gehostet wird, eine Datenbank mit dem Namen database01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="dd31a-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="dd31a-118">Beispiel 3: Ändern der maximalen Speichergröße einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="dd31a-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="dd31a-119">Mit diesem Befehl wird eine Datenbank mit dem Namen database01 aktualisiert, um die maximale Größe auf 1 TB zu setzen.</span><span class="sxs-lookup"><span data-stu-id="dd31a-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="dd31a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd31a-120">PARAMETERS</span></span>

### <span data-ttu-id="dd31a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd31a-121">-AsJob</span></span>
<span data-ttu-id="dd31a-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dd31a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd31a-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd31a-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="dd31a-124">Die automatische Pausen Verzögerung in Minuten für Datenbank (nur serverlos),-1 zum Abmelden</span><span class="sxs-lookup"><span data-stu-id="dd31a-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="dd31a-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="dd31a-126">Die Backup-Speicherredundanz, die zum Speichern von Sicherungen für die SQL-Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd31a-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="dd31a-127">Die Optionen sind: local, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="dd31a-127">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="dd31a-128">-ComputeGeneration</span></span>
<span data-ttu-id="dd31a-129">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd31a-129">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="dd31a-130">-ComputeModel</span></span>
<span data-ttu-id="dd31a-131">Berechnetes Modell der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dd31a-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="dd31a-132">Serverlos oder bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="dd31a-132">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd31a-133">-DatabaseName</span></span>
<span data-ttu-id="dd31a-134">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="dd31a-134">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd31a-135">-DefaultProfile</span></span>
<span data-ttu-id="dd31a-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dd31a-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd31a-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="dd31a-137">-Edition</span></span>
<span data-ttu-id="dd31a-138">Gibt die Edition für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="dd31a-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="dd31a-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="dd31a-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd31a-140">Keine</span><span class="sxs-lookup"><span data-stu-id="dd31a-140">None</span></span>
- <span data-ttu-id="dd31a-141">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="dd31a-141">Basic</span></span>
- <span data-ttu-id="dd31a-142">Standard</span><span class="sxs-lookup"><span data-stu-id="dd31a-142">Standard</span></span>
- <span data-ttu-id="dd31a-143">Premium</span><span class="sxs-lookup"><span data-stu-id="dd31a-143">Premium</span></span>
- <span data-ttu-id="dd31a-144">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="dd31a-144">DataWarehouse</span></span>
- <span data-ttu-id="dd31a-145">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="dd31a-145">Free</span></span>
- <span data-ttu-id="dd31a-146">Stretch</span><span class="sxs-lookup"><span data-stu-id="dd31a-146">Stretch</span></span>
- <span data-ttu-id="dd31a-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="dd31a-147">GeneralPurpose</span></span>
- <span data-ttu-id="dd31a-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="dd31a-148">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="dd31a-149">-ElasticPoolName</span></span>
<span data-ttu-id="dd31a-150">Gibt den Namen des elastischen Pools an, in dem die Datenbank verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd31a-150">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="dd31a-151">-LicenseType</span></span>
<span data-ttu-id="dd31a-152">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dd31a-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="dd31a-153">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="dd31a-153">Possible values are:</span></span>
- <span data-ttu-id="dd31a-154">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="dd31a-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="dd31a-155">Der Daten Bank Preis wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="dd31a-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="dd31a-156">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="dd31a-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="dd31a-157">Der Daten Bank Preis enthält eine neue SQL Server-Lizenzgebühr.</span><span class="sxs-lookup"><span data-stu-id="dd31a-157">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="dd31a-158">-MaxSizeBytes</span></span>
<span data-ttu-id="dd31a-159">Die maximale Größe der Azure SQL-Datenbank in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dd31a-159">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="dd31a-160">-MinimumCapacity</span></span>
<span data-ttu-id="dd31a-161">Die minimale Kapazität, die die Datenbank immer zugewiesen hat, wenn Sie nicht angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="dd31a-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="dd31a-162">Nur für Server-Azure SQL-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="dd31a-162">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-163">-Name</span><span class="sxs-lookup"><span data-stu-id="dd31a-163">-NewName</span></span>
<span data-ttu-id="dd31a-164">Der neue Name, in den die Datenbank umbenannt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd31a-164">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-165">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="dd31a-165">-ReadReplicaCount</span></span>
<span data-ttu-id="dd31a-166">Die Anzahl der ReadOnly-sekundären Replikate, die der Datenbank zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dd31a-166">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="dd31a-167">Nur für die hoch skalierte Edition.</span><span class="sxs-lookup"><span data-stu-id="dd31a-167">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="dd31a-168">-ReadScale</span></span>
<span data-ttu-id="dd31a-169">Wenn diese Option aktiviert ist, können Verbindungen, deren Verbindungszeichenfolge auf ReadOnly festgesetzt ist, möglicherweise an ein ReadOnly-sekundäres Replikat weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="dd31a-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="dd31a-170">Diese Eigenschaft kann nur für unternehmenskritische Premium-und geschäftskritische Datenbanken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd31a-170">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="dd31a-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="dd31a-172">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd31a-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="dd31a-173">Informationen zu den Dienst Zielen finden Sie unter [Azure SQL-Datenbankdienst Ebenen und Leistungsstufen](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in der Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="dd31a-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd31a-174">-ResourceGroupName</span></span>
<span data-ttu-id="dd31a-175">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dd31a-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dd31a-176">-Servername</span><span class="sxs-lookup"><span data-stu-id="dd31a-176">-ServerName</span></span>
<span data-ttu-id="dd31a-177">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="dd31a-177">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="dd31a-178">-Tags</span><span class="sxs-lookup"><span data-stu-id="dd31a-178">-Tags</span></span>
<span data-ttu-id="dd31a-179">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="dd31a-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dd31a-180">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="dd31a-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="dd31a-181">-VCore</span></span>
<span data-ttu-id="dd31a-182">Die Vcore-Nummer für die Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="dd31a-182">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="dd31a-183">-ZoneRedundant</span></span>
<span data-ttu-id="dd31a-184">Die Zonen Redundanz, die der Azure SQL-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="dd31a-184">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd31a-185">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd31a-185">-Confirm</span></span>
<span data-ttu-id="dd31a-186">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd31a-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd31a-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd31a-187">-WhatIf</span></span>
<span data-ttu-id="dd31a-188">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd31a-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd31a-189">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd31a-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd31a-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd31a-190">CommonParameters</span></span>
<span data-ttu-id="dd31a-191">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd31a-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd31a-192">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd31a-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd31a-193">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd31a-193">INPUTS</span></span>

### <span data-ttu-id="dd31a-194">System. String</span><span class="sxs-lookup"><span data-stu-id="dd31a-194">System.String</span></span>

## <span data-ttu-id="dd31a-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd31a-195">OUTPUTS</span></span>

### <span data-ttu-id="dd31a-196">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="dd31a-196">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="dd31a-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd31a-197">NOTES</span></span>

## <span data-ttu-id="dd31a-198">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd31a-198">RELATED LINKS</span></span>

[<span data-ttu-id="dd31a-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd31a-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="dd31a-200">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd31a-200">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="dd31a-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd31a-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="dd31a-202">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd31a-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="dd31a-203">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dd31a-203">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="dd31a-204">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="dd31a-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
