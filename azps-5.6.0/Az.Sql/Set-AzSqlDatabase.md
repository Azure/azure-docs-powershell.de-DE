---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 17e6c492828f877ebf53c634a7670e8d60c9ccba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940891"
---
# <span data-ttu-id="46413-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46413-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="46413-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46413-102">SYNOPSIS</span></span>
<span data-ttu-id="46413-103">Legt Eigenschaften für eine Datenbank fest, oder verschiebt eine vorhandene Datenbank in einen Pool für flexible Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="46413-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="46413-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46413-104">SYNTAX</span></span>

### <span data-ttu-id="46413-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="46413-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46413-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="46413-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46413-107">Umbenennen</span><span class="sxs-lookup"><span data-stu-id="46413-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46413-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46413-108">DESCRIPTION</span></span>
<span data-ttu-id="46413-109">Das **Cmdlet Set-AzSqlDatabase** legt Eigenschaften für eine Datenbank in Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="46413-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="46413-110">Dieses Cmdlet kann die Dienstebene (*Edition),* die Leistungsstufe (*RequestedServiceObjectiveName*) und die maximale Speichergröße (*MaxSizeBytes*) für die Datenbank ändern.</span><span class="sxs-lookup"><span data-stu-id="46413-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="46413-111">Darüber hinaus können Sie den *Parameter "ElasticPoolName"* angeben, um eine Datenbank in einen Pool mit einem Flexiblen Pool zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="46413-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="46413-112">Wenn sich eine Datenbank bereits in einem Pool mit einem flexiblen Pool befindet, können Sie den *Parameter RequestedServiceObjectiveName* verwenden, um die Datenbank aus einem Pool mit einem Flexiblen Pool in eine Leistungsstufe für einzelne Datenbanken zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="46413-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="46413-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46413-113">EXAMPLES</span></span>

### <span data-ttu-id="46413-114">Beispiel 1: Aktualisieren einer Datenbank auf eine Standard-S0-Datenbank</span><span class="sxs-lookup"><span data-stu-id="46413-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="46413-115">Mit diesem Befehl wird eine Datenbank mit dem Namen Datenbank01 auf eine Standard-S0-Datenbank auf einem Server namens Server01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="46413-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="46413-116">Beispiel 2: Hinzufügen einer Datenbank zu einem Pool mit einem Flexiblen Pool</span><span class="sxs-lookup"><span data-stu-id="46413-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="46413-117">Mit diesem Befehl wird eine Datenbank mit dem Namen Datenbank01 zum Pool mit dem Namen "ElasticPool01" hinzugefügt, der auf dem Server mit dem Namen Server01 gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="46413-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="46413-118">Beispiel 3: Ändern der maximalen Speichergröße einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="46413-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="46413-119">Mit diesem Befehl wird eine Datenbank mit dem Namen Datenbank01 aktualisiert, um die maximale Größe auf 1 TB zu legen.</span><span class="sxs-lookup"><span data-stu-id="46413-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="46413-120">Beispiel 4: Aktualisieren einer vorhandenen Allgemeinen Datenbank auf Hyperscale-Dienstebene</span><span class="sxs-lookup"><span data-stu-id="46413-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="46413-121">Mit diesem Befehl wird eine Datenbank mit dem Namen "Database01" von "Allgemeinzweck" auf "Hyperscale"-Dienstebene aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="46413-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="46413-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46413-122">PARAMETERS</span></span>

### <span data-ttu-id="46413-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46413-123">-AsJob</span></span>
<span data-ttu-id="46413-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="46413-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46413-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="46413-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="46413-126">Die Verzögerung der automatischen Pause in Minuten für die Datenbank (nur serverlos), -1 zum Abmelden</span><span class="sxs-lookup"><span data-stu-id="46413-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="46413-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="46413-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="46413-128">Die Redundanz des Sicherungsspeichers zum Speichern von Sicherungen für die SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="46413-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="46413-129">Optionen sind: Lokal, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="46413-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="46413-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="46413-130">-ComputeGeneration</span></span>
<span data-ttu-id="46413-131">Die zuzuordnende Berechnungsgenerierung.</span><span class="sxs-lookup"><span data-stu-id="46413-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="46413-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="46413-132">-ComputeModel</span></span>
<span data-ttu-id="46413-133">Berechnetes Modell der Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="46413-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="46413-134">Serverlos oder bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="46413-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="46413-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46413-135">-DatabaseName</span></span>
<span data-ttu-id="46413-136">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="46413-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="46413-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46413-137">-DefaultProfile</span></span>
<span data-ttu-id="46413-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="46413-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46413-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="46413-139">-Edition</span></span>
<span data-ttu-id="46413-140">Gibt die Edition für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="46413-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="46413-141">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="46413-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46413-142">Keine</span><span class="sxs-lookup"><span data-stu-id="46413-142">None</span></span>
- <span data-ttu-id="46413-143">Basic</span><span class="sxs-lookup"><span data-stu-id="46413-143">Basic</span></span>
- <span data-ttu-id="46413-144">Standard</span><span class="sxs-lookup"><span data-stu-id="46413-144">Standard</span></span>
- <span data-ttu-id="46413-145">Premium</span><span class="sxs-lookup"><span data-stu-id="46413-145">Premium</span></span>
- <span data-ttu-id="46413-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="46413-146">DataWarehouse</span></span>
- <span data-ttu-id="46413-147">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="46413-147">Free</span></span>
- <span data-ttu-id="46413-148">Stretch</span><span class="sxs-lookup"><span data-stu-id="46413-148">Stretch</span></span>
- <span data-ttu-id="46413-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="46413-149">GeneralPurpose</span></span>
- <span data-ttu-id="46413-150">Hyperscale</span><span class="sxs-lookup"><span data-stu-id="46413-150">Hyperscale</span></span>
- <span data-ttu-id="46413-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="46413-151">BusinessCritical</span></span>

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

### <span data-ttu-id="46413-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="46413-152">-ElasticPoolName</span></span>
<span data-ttu-id="46413-153">Gibt den Namen des Poolpools an, in dem die Datenbank bewegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46413-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="46413-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="46413-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="46413-155">Die Anzahl der gelesenen sekundären Replikate, die der Datenbank zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="46413-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="46413-156">Nur für Hyperscale Edition.</span><span class="sxs-lookup"><span data-stu-id="46413-156">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46413-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="46413-157">-LicenseType</span></span>
<span data-ttu-id="46413-158">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="46413-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="46413-159">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="46413-159">Possible values are:</span></span>
- <span data-ttu-id="46413-160">BasePrice – AhB(Azure Hybrid Benefit)-rabattierte Preise für vorhandene SQL Server werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="46413-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="46413-161">Der Datenbankpreis wird für vorhandene Lizenzbesitzer SQL Server vergünstigt.</span><span class="sxs-lookup"><span data-stu-id="46413-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="46413-162">LicenseIncluded – Rabattpreise für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="46413-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="46413-163">Der Datenbankpreis enthält eine neue SQL Server Lizenzkosten.</span><span class="sxs-lookup"><span data-stu-id="46413-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="46413-164">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="46413-164">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="46413-165">Die Wartungskonfigurations-ID für die SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="46413-165">The Maintenance configuration id for the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46413-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="46413-166">-MaxSizeBytes</span></span>
<span data-ttu-id="46413-167">Die maximale Größe der Azure SQL Datenbank in Bytes.</span><span class="sxs-lookup"><span data-stu-id="46413-167">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="46413-168">-MinimumKapazität</span><span class="sxs-lookup"><span data-stu-id="46413-168">-MinimumCapacity</span></span>
<span data-ttu-id="46413-169">Die minimale Kapazität, die die Datenbank immer zugewiesen hat, wenn nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="46413-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="46413-170">Nur für serverlose Azure Sql-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="46413-170">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="46413-171">-NewName</span><span class="sxs-lookup"><span data-stu-id="46413-171">-NewName</span></span>
<span data-ttu-id="46413-172">Der neue Name, in den die Datenbank umbenannt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46413-172">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="46413-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="46413-173">-ReadScale</span></span>
<span data-ttu-id="46413-174">Wenn diese Option aktiviert ist, werden Verbindungen, deren Anwendungsabsicht auf "Lesen" in der Verbindungszeichenfolge festgelegt ist, möglicherweise an ein gelesenes sekundäres Replikat geroutet.</span><span class="sxs-lookup"><span data-stu-id="46413-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="46413-175">Diese Eigenschaft ist nur für Premium- und Geschäftskritische Datenbanken festgelegt.</span><span class="sxs-lookup"><span data-stu-id="46413-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="46413-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="46413-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="46413-177">Gibt den Namen des Dienstziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="46413-177">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="46413-178">Informationen zu Dienstzielen finden Sie unter [Azure SQL Datenbankdienstebenen](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) und Leistungsstufen in der Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="46413-178">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="46413-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46413-179">-ResourceGroupName</span></span>
<span data-ttu-id="46413-180">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="46413-180">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="46413-181">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="46413-181">-SecondaryType</span></span>
<span data-ttu-id="46413-182">Der sekundäre Typ der Datenbank, wenn es sich um eine sekundäre Datenbank handelt.</span><span class="sxs-lookup"><span data-stu-id="46413-182">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="46413-183">Gültige Werte sind "Geo" und "Named".</span><span class="sxs-lookup"><span data-stu-id="46413-183">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46413-184">-Servername</span><span class="sxs-lookup"><span data-stu-id="46413-184">-ServerName</span></span>
<span data-ttu-id="46413-185">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="46413-185">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="46413-186">-Tags</span><span class="sxs-lookup"><span data-stu-id="46413-186">-Tags</span></span>
<span data-ttu-id="46413-187">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="46413-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="46413-188">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="46413-188">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="46413-189">-VCore</span><span class="sxs-lookup"><span data-stu-id="46413-189">-VCore</span></span>
<span data-ttu-id="46413-190">Die Vcore-Nummer für die Azure Sql-Datenbank</span><span class="sxs-lookup"><span data-stu-id="46413-190">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="46413-191">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="46413-191">-ZoneRedundant</span></span>
<span data-ttu-id="46413-192">Die Zonenredundanz, die der Azure Sql-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="46413-192">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="46413-193">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46413-193">-Confirm</span></span>
<span data-ttu-id="46413-194">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46413-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46413-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46413-195">-WhatIf</span></span>
<span data-ttu-id="46413-196">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46413-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46413-197">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46413-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46413-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46413-198">CommonParameters</span></span>
<span data-ttu-id="46413-199">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46413-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46413-200">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46413-200">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46413-201">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46413-201">INPUTS</span></span>

### <span data-ttu-id="46413-202">System.String</span><span class="sxs-lookup"><span data-stu-id="46413-202">System.String</span></span>

## <span data-ttu-id="46413-203">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46413-203">OUTPUTS</span></span>

### <span data-ttu-id="46413-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="46413-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="46413-205">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46413-205">NOTES</span></span>

## <span data-ttu-id="46413-206">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46413-206">RELATED LINKS</span></span>

[<span data-ttu-id="46413-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46413-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="46413-208">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46413-208">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="46413-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46413-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="46413-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46413-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="46413-211">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46413-211">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="46413-212">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="46413-212">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
