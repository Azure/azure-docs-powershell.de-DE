---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: c4ccb57292fd4abc2c9b6fd14c5e4492047a2e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920912"
---
# <span data-ttu-id="ba262-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba262-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="ba262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba262-102">SYNOPSIS</span></span>
<span data-ttu-id="ba262-103">Erstellt eine Datenbank oder eine flexible Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba262-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="ba262-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba262-104">SYNTAX</span></span>

### <span data-ttu-id="ba262-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba262-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba262-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="ba262-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba262-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba262-107">DESCRIPTION</span></span>
<span data-ttu-id="ba262-108">Das **Cmdlet New-AzSqlDatabase** erstellt eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba262-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="ba262-109">Sie können auch eine flexible Datenbank erstellen, indem Sie den *Parameter "ElasticPoolName"* auf einen vorhandenen Pool für einen flexiblen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="ba262-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="ba262-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba262-110">EXAMPLES</span></span>

### <span data-ttu-id="ba262-111">Beispiel 1: Erstellen einer Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ba262-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="ba262-112">Mit diesem Befehl wird eine Datenbank mit dem Namen Database01 auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba262-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="ba262-113">Beispiel 2: Erstellen einer flexiblen Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ba262-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="ba262-114">Mit diesem Befehl wird eine Datenbank mit dem Namen Database02 im Pool mit dem Namen "ElasticPool01" auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba262-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="ba262-115">Beispiel 3: Erstellen einer Vcore-Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ba262-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="ba262-116">Mit diesem Befehl wird eine Vcore-Datenbank mit dem Namen Database03 auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba262-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="ba262-117">Beispiel 4: Erstellen einer serverlosen Datenbank auf dem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ba262-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="ba262-118">Mit diesem Befehl wird eine serverlose Datenbank mit dem Namen Database04 auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba262-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="ba262-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba262-119">PARAMETERS</span></span>

### <span data-ttu-id="ba262-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba262-120">-AsJob</span></span>
<span data-ttu-id="ba262-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ba262-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba262-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="ba262-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="ba262-123">Verzögerung der automatischen Pause in Minuten für Datenbank (nur serverlos), -1 zum Abmelden</span><span class="sxs-lookup"><span data-stu-id="ba262-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ba262-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ba262-125">Die Redundanz des Sicherungsspeichers zum Speichern von Sicherungen für die SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba262-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="ba262-126">Optionen sind: Lokal, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="ba262-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="ba262-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="ba262-127">-CatalogCollation</span></span>
<span data-ttu-id="ba262-128">Gibt den Namen der Datenbankkatalogsortierung SQL an.</span><span class="sxs-lookup"><span data-stu-id="ba262-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="ba262-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="ba262-129">-CollationName</span></span>
<span data-ttu-id="ba262-130">Gibt den Namen der Datenbanksortierung SQL an.</span><span class="sxs-lookup"><span data-stu-id="ba262-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="ba262-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ba262-131">-ComputeGeneration</span></span>
<span data-ttu-id="ba262-132">Die zuzuordnende Berechnungsgenerierung.</span><span class="sxs-lookup"><span data-stu-id="ba262-132">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="ba262-133">-ComputeModel</span></span>
<span data-ttu-id="ba262-134">Das Rechenmodell für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba262-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="ba262-135">Serverlos oder bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="ba262-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba262-136">-DatabaseName</span></span>
<span data-ttu-id="ba262-137">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ba262-137">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba262-138">-DefaultProfile</span></span>
<span data-ttu-id="ba262-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ba262-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba262-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="ba262-140">-Edition</span></span>
<span data-ttu-id="ba262-141">Gibt die Edition an, die der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba262-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="ba262-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ba262-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba262-143">Keine</span><span class="sxs-lookup"><span data-stu-id="ba262-143">None</span></span>
- <span data-ttu-id="ba262-144">Basic</span><span class="sxs-lookup"><span data-stu-id="ba262-144">Basic</span></span>
- <span data-ttu-id="ba262-145">Standard</span><span class="sxs-lookup"><span data-stu-id="ba262-145">Standard</span></span>
- <span data-ttu-id="ba262-146">Premium</span><span class="sxs-lookup"><span data-stu-id="ba262-146">Premium</span></span>
- <span data-ttu-id="ba262-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="ba262-147">DataWarehouse</span></span>
- <span data-ttu-id="ba262-148">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="ba262-148">Free</span></span>
- <span data-ttu-id="ba262-149">Stretch</span><span class="sxs-lookup"><span data-stu-id="ba262-149">Stretch</span></span>
- <span data-ttu-id="ba262-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="ba262-150">GeneralPurpose</span></span>
- <span data-ttu-id="ba262-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="ba262-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ba262-152">-ElasticPoolName</span></span>
<span data-ttu-id="ba262-153">Gibt den Namen des Poolpools an, in dem die Datenbank gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba262-153">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-154">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ba262-154">-Force</span></span>
<span data-ttu-id="ba262-155">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="ba262-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ba262-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="ba262-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="ba262-157">Die Anzahl der gelesenen sekundären Replikate, die der Datenbank zugeordnet sind, an die schreibgeschützte Anwendungsabsichtsverbindungen möglicherweise geroutet werden.</span><span class="sxs-lookup"><span data-stu-id="ba262-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="ba262-158">Diese Eigenschaft ist nur für Hyperscale-Edition-Datenbanken settable.</span><span class="sxs-lookup"><span data-stu-id="ba262-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ba262-159">-LicenseType</span></span>
<span data-ttu-id="ba262-160">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba262-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="ba262-161">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ba262-161">Possible values are:</span></span>
- <span data-ttu-id="ba262-162">BasePrice – AhB(Azure Hybrid Benefit)-rabattierte Preise für vorhandene SQL Server werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="ba262-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ba262-163">Der Datenbankpreis wird für vorhandene Lizenzbesitzer SQL Server vergünstigt.</span><span class="sxs-lookup"><span data-stu-id="ba262-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ba262-164">LicenseIncluded – Rabattpreise für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="ba262-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ba262-165">Der Datenbankpreis enthält eine neue SQL Server Lizenzkosten.</span><span class="sxs-lookup"><span data-stu-id="ba262-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="ba262-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ba262-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="ba262-167">Die Wartungskonfigurations-ID für die SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba262-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="ba262-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ba262-168">-MaxSizeBytes</span></span>
<span data-ttu-id="ba262-169">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="ba262-169">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-170">-MinimumKapazität</span><span class="sxs-lookup"><span data-stu-id="ba262-170">-MinimumCapacity</span></span>
<span data-ttu-id="ba262-171">Die minimale Kapazität, die die Datenbank immer zugewiesen hat, wenn nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="ba262-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="ba262-172">Nur für serverlose Azure Sql-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ba262-172">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="ba262-173">-ReadScale</span></span>
<span data-ttu-id="ba262-174">Wenn diese Option aktiviert ist, werden Verbindungen, deren Anwendungsabsicht auf "Lesen" in der Verbindungszeichenfolge festgelegt ist, möglicherweise an ein gelesenes sekundäres Replikat geroutet.</span><span class="sxs-lookup"><span data-stu-id="ba262-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="ba262-175">Diese Eigenschaft ist nur für Premium- und Geschäftskritische Datenbanken festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba262-175">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ba262-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="ba262-177">Gibt den Namen des Dienstziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba262-177">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba262-178">-ResourceGroupName</span></span>
<span data-ttu-id="ba262-179">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ba262-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ba262-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="ba262-180">-SampleName</span></span>
<span data-ttu-id="ba262-181">Der Name des Beispielschemas, das beim Erstellen dieser Datenbank angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba262-181">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="ba262-182">-SecondaryType</span></span>
<span data-ttu-id="ba262-183">Der sekundäre Typ der Datenbank, wenn es sich um eine sekundäre Datenbank handelt.</span><span class="sxs-lookup"><span data-stu-id="ba262-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="ba262-184">Gültige Werte sind "Geo" und "Named".</span><span class="sxs-lookup"><span data-stu-id="ba262-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="ba262-185">-Servername</span><span class="sxs-lookup"><span data-stu-id="ba262-185">-ServerName</span></span>
<span data-ttu-id="ba262-186">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ba262-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ba262-187">-Tags</span><span class="sxs-lookup"><span data-stu-id="ba262-187">-Tags</span></span>
<span data-ttu-id="ba262-188">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet der neuen Datenbank zurät.</span><span class="sxs-lookup"><span data-stu-id="ba262-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="ba262-189">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ba262-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="ba262-190">-VCore</span></span>
<span data-ttu-id="ba262-191">Die Vcore-Nummer für die Azure Sql-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ba262-191">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ba262-192">-ZoneRedundant</span></span>
<span data-ttu-id="ba262-193">Die Zonenredundanz, die der Azure Sql-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="ba262-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="ba262-194">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba262-194">-Confirm</span></span>
<span data-ttu-id="ba262-195">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba262-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba262-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba262-196">-WhatIf</span></span>
<span data-ttu-id="ba262-197">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba262-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba262-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba262-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba262-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba262-199">CommonParameters</span></span>
<span data-ttu-id="ba262-200">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba262-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba262-201">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba262-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba262-202">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba262-202">INPUTS</span></span>

### <span data-ttu-id="ba262-203">System.String</span><span class="sxs-lookup"><span data-stu-id="ba262-203">System.String</span></span>

## <span data-ttu-id="ba262-204">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba262-204">OUTPUTS</span></span>

### <span data-ttu-id="ba262-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ba262-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ba262-206">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba262-206">NOTES</span></span>

## <span data-ttu-id="ba262-207">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba262-207">RELATED LINKS</span></span>

[<span data-ttu-id="ba262-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba262-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="ba262-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ba262-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ba262-210">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ba262-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="ba262-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba262-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="ba262-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba262-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="ba262-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba262-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="ba262-214">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba262-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="ba262-215">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="ba262-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

