---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: f92af476c7a9cf642512f3aa338069ab37b1c840
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360672"
---
# <span data-ttu-id="ef7ab-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ab-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="ef7ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7ab-103">Erstellt eine Datenbank oder eine Datenbank mit Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="ef7ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef7ab-104">SYNTAX</span></span>

### <span data-ttu-id="ef7ab-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef7ab-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef7ab-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ab-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7ab-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef7ab-107">DESCRIPTION</span></span>
<span data-ttu-id="ef7ab-108">Das **Cmdlet "New-AzSqlDatabase"** erstellt eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="ef7ab-109">Sie können auch eine Datenbank für Eine Datenbank erstellen, indem Sie den *Parameter "PoolName"* auf einen vorhandenen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="ef7ab-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef7ab-110">EXAMPLES</span></span>

### <span data-ttu-id="ef7ab-111">Beispiel 1: Erstellen einer Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ef7ab-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="ef7ab-112">Mit diesem Befehl wird eine Datenbank mit dem Namen "Database01" auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="ef7ab-113">Beispiel 2: Erstellen einer Datenbank mit Datenbanken auf einem bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="ef7ab-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="ef7ab-114">Mit diesem Befehl wird eine Datenbank mit dem Namen "Database02" im Pool mit dem Namen "PoolsPool01" auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="ef7ab-115">Beispiel 3: Erstellen einer Vcore-Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ef7ab-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="ef7ab-116">Mit diesem Befehl wird eine Vcore-Datenbank mit dem Namen "Database03" auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="ef7ab-117">Beispiel 4: Erstellen einer serverlosen Datenbank auf dem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ef7ab-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="ef7ab-118">Mit diesem Befehl wird eine serverlose Datenbank mit dem Namen "Database04" auf Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="ef7ab-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef7ab-119">PARAMETERS</span></span>

### <span data-ttu-id="ef7ab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef7ab-120">-AsJob</span></span>
<span data-ttu-id="ef7ab-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ef7ab-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef7ab-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef7ab-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="ef7ab-123">Automatische Verzögerung in Minuten für Datenbank (nur serverlos), -1 zum Abmelden</span><span class="sxs-lookup"><span data-stu-id="ef7ab-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="ef7ab-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ef7ab-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ef7ab-125">Die Sicherungsspeicherredundanz, die zum Speichern von Sicherungen für die datenbank SQL wird.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="ef7ab-126">Optionen sind: Lokal, Zone und Geo.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="ef7ab-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="ef7ab-127">-CatalogCollation</span></span>
<span data-ttu-id="ef7ab-128">Gibt den Namen der SQL Datenbankkatalogsortierung an.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="ef7ab-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="ef7ab-129">-CollationName</span></span>
<span data-ttu-id="ef7ab-130">Gibt den Namen der SQL Datenbanksortierung an.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="ef7ab-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ef7ab-131">-ComputeGeneration</span></span>
<span data-ttu-id="ef7ab-132">Die zuzuordnende Rechengenerierung.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="ef7ab-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="ef7ab-133">-ComputeModel</span></span>
<span data-ttu-id="ef7ab-134">Das Rechenmodell für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="ef7ab-135">Serverlos oder bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="ef7ab-135">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="ef7ab-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef7ab-136">-DatabaseName</span></span>
<span data-ttu-id="ef7ab-137">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ef7ab-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7ab-138">-DefaultProfile</span></span>
<span data-ttu-id="ef7ab-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ef7ab-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef7ab-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="ef7ab-140">-Edition</span></span>
<span data-ttu-id="ef7ab-141">Gibt die Edition an, die der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="ef7ab-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ef7ab-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef7ab-143">Keine</span><span class="sxs-lookup"><span data-stu-id="ef7ab-143">None</span></span>
- <span data-ttu-id="ef7ab-144">Standard</span><span class="sxs-lookup"><span data-stu-id="ef7ab-144">Basic</span></span>
- <span data-ttu-id="ef7ab-145">Standard</span><span class="sxs-lookup"><span data-stu-id="ef7ab-145">Standard</span></span>
- <span data-ttu-id="ef7ab-146">Premium</span><span class="sxs-lookup"><span data-stu-id="ef7ab-146">Premium</span></span>
- <span data-ttu-id="ef7ab-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="ef7ab-147">DataWarehouse</span></span>
- <span data-ttu-id="ef7ab-148">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="ef7ab-148">Free</span></span>
- <span data-ttu-id="ef7ab-149">Strecken</span><span class="sxs-lookup"><span data-stu-id="ef7ab-149">Stretch</span></span>
- <span data-ttu-id="ef7ab-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="ef7ab-150">GeneralPurpose</span></span>
- <span data-ttu-id="ef7ab-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="ef7ab-151">BusinessCritical</span></span>

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

### <span data-ttu-id="ef7ab-152">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ef7ab-152">-ElasticPoolName</span></span>
<span data-ttu-id="ef7ab-153">Gibt den Namen des Poolpools an, in dem die Datenbank gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="ef7ab-154">-Force</span><span class="sxs-lookup"><span data-stu-id="ef7ab-154">-Force</span></span>
<span data-ttu-id="ef7ab-155">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="ef7ab-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ef7ab-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="ef7ab-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="ef7ab-157">Die Anzahl der lesbaren sekundären Replikate, die der Datenbank zugeordnet sind, an die gelesene Anwendungsabsichtsverbindungen möglicherweise geroutet werden.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="ef7ab-158">Diese Eigenschaft kann nur für Hyperscale -Edition-Datenbanken festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-158">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="ef7ab-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ef7ab-159">-LicenseType</span></span>
<span data-ttu-id="ef7ab-160">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="ef7ab-161">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ef7ab-161">Possible values are:</span></span>
- <span data-ttu-id="ef7ab-162">BasePrice – Reduzierte Preise für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ef7ab-163">Der Datenbankpreis wird für vorhandene Lizenzbesitzer SQL Server vergünstigt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ef7ab-164">LicenseIncluded – Rabatte für Azure Hybrid Benefit (AHB) für vorhandene SQL Server Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ef7ab-165">Der Datenbankpreis enthält eine neue SQL Server Lizenzkosten.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="ef7ab-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ef7ab-166">-MaxSizeBytes</span></span>
<span data-ttu-id="ef7ab-167">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-167">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="ef7ab-168">-Minimum1</span><span class="sxs-lookup"><span data-stu-id="ef7ab-168">-MinimumCapacity</span></span>
<span data-ttu-id="ef7ab-169">Die minimale Kapazität, die die Datenbank immer zugeordnet hat, wenn sie nicht angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="ef7ab-170">Nur für serverlose Azure Sql-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-170">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="ef7ab-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="ef7ab-171">-ReadScale</span></span>
<span data-ttu-id="ef7ab-172">Wenn diese Option aktiviert ist, werden Verbindungen, für die der Anwendungsabsichtsabsichtssatz in der Verbindungszeichenfolge festgelegt ist, möglicherweise an eine lesbare sekundäre Replikatverbindung geroutet.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="ef7ab-173">Diese Eigenschaft kann nur für Premium- und unternehmenskritische Datenbanken festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-173">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="ef7ab-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ef7ab-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="ef7ab-175">Gibt den Namen des Dienstziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-175">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="ef7ab-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7ab-176">-ResourceGroupName</span></span>
<span data-ttu-id="ef7ab-177">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-177">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ef7ab-178">-SampleName</span><span class="sxs-lookup"><span data-stu-id="ef7ab-178">-SampleName</span></span>
<span data-ttu-id="ef7ab-179">Der Name des Beispielschemas, das beim Erstellen dieser Datenbank angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-179">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="ef7ab-180">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="ef7ab-180">-SecondaryType</span></span>
<span data-ttu-id="ef7ab-181">Der sekundäre Typ der Datenbank, wenn es sich um einen sekundären Datenbanktyp handelt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-181">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="ef7ab-182">Gültige Werte sind "Geo" und "Named".</span><span class="sxs-lookup"><span data-stu-id="ef7ab-182">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="ef7ab-183">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef7ab-183">-ServerName</span></span>
<span data-ttu-id="ef7ab-184">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-184">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ef7ab-185">-Tags</span><span class="sxs-lookup"><span data-stu-id="ef7ab-185">-Tags</span></span>
<span data-ttu-id="ef7ab-186">Gibt ein Wörterbuch von Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet der neuen Datenbank zugibt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-186">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="ef7ab-187">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ef7ab-187">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ef7ab-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="ef7ab-188">-VCore</span></span>
<span data-ttu-id="ef7ab-189">Die Vcore-Nummer für die Azure Sql-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ef7ab-189">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="ef7ab-190">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ef7ab-190">-ZoneRedundant</span></span>
<span data-ttu-id="ef7ab-191">Die Zonenredundanz, die der Azure -Sql-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="ef7ab-191">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="ef7ab-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef7ab-192">-Confirm</span></span>
<span data-ttu-id="ef7ab-193">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7ab-194">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ef7ab-194">-WhatIf</span></span>
<span data-ttu-id="ef7ab-195">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7ab-196">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7ab-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7ab-197">CommonParameters</span></span>
<span data-ttu-id="ef7ab-198">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7ab-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7ab-199">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef7ab-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7ab-200">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef7ab-200">INPUTS</span></span>

### <span data-ttu-id="ef7ab-201">System.String</span><span class="sxs-lookup"><span data-stu-id="ef7ab-201">System.String</span></span>

## <span data-ttu-id="ef7ab-202">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef7ab-202">OUTPUTS</span></span>

### <span data-ttu-id="ef7ab-203">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ef7ab-203">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ef7ab-204">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef7ab-204">NOTES</span></span>

## <span data-ttu-id="ef7ab-205">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef7ab-205">RELATED LINKS</span></span>

[<span data-ttu-id="ef7ab-206">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ab-206">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="ef7ab-207">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ef7ab-207">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ef7ab-208">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ef7ab-208">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="ef7ab-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ab-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="ef7ab-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ab-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="ef7ab-211">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ab-211">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="ef7ab-212">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ef7ab-212">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="ef7ab-213">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="ef7ab-213">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

