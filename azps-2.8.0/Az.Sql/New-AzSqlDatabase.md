---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 3655204204dc35ea62473a1002a84d53ce0c327d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826028"
---
# <span data-ttu-id="ead9f-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ead9f-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="ead9f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ead9f-102">SYNOPSIS</span></span>
<span data-ttu-id="ead9f-103">Erstellt eine Datenbank oder eine elastische Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ead9f-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="ead9f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead9f-104">SYNTAX</span></span>

### <span data-ttu-id="ead9f-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="ead9f-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead9f-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="ead9f-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead9f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ead9f-107">DESCRIPTION</span></span>
<span data-ttu-id="ead9f-108">Das Cmdlet **New-AzSqlDatabase** erstellt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ead9f-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="ead9f-109">Sie können auch eine elastische Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="ead9f-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="ead9f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ead9f-110">EXAMPLES</span></span>

### <span data-ttu-id="ead9f-111">Beispiel 1: Erstellen einer Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ead9f-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="ead9f-112">Mit diesem Befehl wird eine Datenbank mit dem Namen Database01 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ead9f-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="ead9f-113">Beispiel 2: Erstellen einer elastischen Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ead9f-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="ead9f-114">Dieser Befehl erstellt eine Datenbank mit dem Namen Database02 im elastischen Pool mit dem Namen ElasticPool01 auf Server Server01.</span><span class="sxs-lookup"><span data-stu-id="ead9f-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="ead9f-115">Beispiel 3: Erstellen einer Vcore-Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ead9f-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="ead9f-116">Mit diesem Befehl wird eine Vcore-Datenbank mit dem Namen Database03 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ead9f-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="ead9f-117">Beispiel 4: Erstellen einer Server Übersichtsdatenbank auf dem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="ead9f-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="ead9f-118">Dieser Befehl erstellt eine Server-Datenbank mit dem Namen Database04 auf dem Server Server01.</span><span class="sxs-lookup"><span data-stu-id="ead9f-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="ead9f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead9f-119">PARAMETERS</span></span>

### <span data-ttu-id="ead9f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ead9f-120">-AsJob</span></span>
<span data-ttu-id="ead9f-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ead9f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ead9f-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="ead9f-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="ead9f-123">Die automatische Pausen Verzögerung in Minuten für Datenbank (nur serverlos),-1 zum Abmelden</span><span class="sxs-lookup"><span data-stu-id="ead9f-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="ead9f-124">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="ead9f-124">-CatalogCollation</span></span>
<span data-ttu-id="ead9f-125">Gibt den Namen der SQL-Datenbankkatalog Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="ead9f-125">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="ead9f-126">-Collation</span><span class="sxs-lookup"><span data-stu-id="ead9f-126">-CollationName</span></span>
<span data-ttu-id="ead9f-127">Gibt den Namen der SQL-Datenbanksortierung an.</span><span class="sxs-lookup"><span data-stu-id="ead9f-127">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="ead9f-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ead9f-128">-ComputeGeneration</span></span>
<span data-ttu-id="ead9f-129">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ead9f-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="ead9f-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="ead9f-130">-ComputeModel</span></span>
<span data-ttu-id="ead9f-131">Das Compute-Modell für Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ead9f-131">The compute model for Azure Sql database.</span></span> <span data-ttu-id="ead9f-132">Serverlos oder bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="ead9f-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="ead9f-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ead9f-133">-DatabaseName</span></span>
<span data-ttu-id="ead9f-134">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ead9f-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ead9f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead9f-135">-DefaultProfile</span></span>
<span data-ttu-id="ead9f-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ead9f-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ead9f-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="ead9f-137">-Edition</span></span>
<span data-ttu-id="ead9f-138">Gibt die Edition an, die der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ead9f-138">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="ead9f-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ead9f-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ead9f-140">Keine</span><span class="sxs-lookup"><span data-stu-id="ead9f-140">None</span></span>
- <span data-ttu-id="ead9f-141">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="ead9f-141">Basic</span></span>
- <span data-ttu-id="ead9f-142">Standard</span><span class="sxs-lookup"><span data-stu-id="ead9f-142">Standard</span></span>
- <span data-ttu-id="ead9f-143">Premium</span><span class="sxs-lookup"><span data-stu-id="ead9f-143">Premium</span></span>
- <span data-ttu-id="ead9f-144">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="ead9f-144">DataWarehouse</span></span>
- <span data-ttu-id="ead9f-145">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="ead9f-145">Free</span></span>
- <span data-ttu-id="ead9f-146">Stretch</span><span class="sxs-lookup"><span data-stu-id="ead9f-146">Stretch</span></span>
- <span data-ttu-id="ead9f-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="ead9f-147">GeneralPurpose</span></span>
- <span data-ttu-id="ead9f-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="ead9f-148">BusinessCritical</span></span>

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

### <span data-ttu-id="ead9f-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ead9f-149">-ElasticPoolName</span></span>
<span data-ttu-id="ead9f-150">Gibt den Namen des elastischen Pools an, in dem die Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ead9f-150">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="ead9f-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ead9f-151">-LicenseType</span></span>
<span data-ttu-id="ead9f-152">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ead9f-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="ead9f-153">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="ead9f-153">Possible values are:</span></span>
- <span data-ttu-id="ead9f-154">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="ead9f-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ead9f-155">Der Daten Bank Preis wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="ead9f-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ead9f-156">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="ead9f-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ead9f-157">Der Daten Bank Preis enthält eine neue SQL Server-Lizenzgebühr.</span><span class="sxs-lookup"><span data-stu-id="ead9f-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="ead9f-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ead9f-158">-MaxSizeBytes</span></span>
<span data-ttu-id="ead9f-159">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="ead9f-159">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="ead9f-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="ead9f-160">-MinimumCapacity</span></span>
<span data-ttu-id="ead9f-161">Die minimale Kapazität, die die Datenbank immer zugewiesen hat, wenn Sie nicht angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="ead9f-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="ead9f-162">Nur für Server-Azure SQL-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ead9f-162">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="ead9f-163">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="ead9f-163">-ReadScale</span></span>
<span data-ttu-id="ead9f-164">Die Option zum Lesen der Skalierung, die der Azure SQL-Datenbank zugewiesen werden soll. (Aktiviert/deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="ead9f-164">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="ead9f-165">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ead9f-165">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="ead9f-166">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ead9f-166">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="ead9f-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead9f-167">-ResourceGroupName</span></span>
<span data-ttu-id="ead9f-168">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ead9f-168">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ead9f-169">-Samplename</span><span class="sxs-lookup"><span data-stu-id="ead9f-169">-SampleName</span></span>
<span data-ttu-id="ead9f-170">Der Name des Beispiel Schemas, das beim Erstellen dieser Datenbank angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ead9f-170">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="ead9f-171">-Servername</span><span class="sxs-lookup"><span data-stu-id="ead9f-171">-ServerName</span></span>
<span data-ttu-id="ead9f-172">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ead9f-172">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ead9f-173">-Tags</span><span class="sxs-lookup"><span data-stu-id="ead9f-173">-Tags</span></span>
<span data-ttu-id="ead9f-174">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet der neuen Datenbank zuordnet.</span><span class="sxs-lookup"><span data-stu-id="ead9f-174">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="ead9f-175">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="ead9f-175">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ead9f-176">-VCore</span><span class="sxs-lookup"><span data-stu-id="ead9f-176">-VCore</span></span>
<span data-ttu-id="ead9f-177">Die Vcore-Nummer für die Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ead9f-177">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="ead9f-178">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ead9f-178">-ZoneRedundant</span></span>
<span data-ttu-id="ead9f-179">Die Zonen Redundanz, die der Azure SQL-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="ead9f-179">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="ead9f-180">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ead9f-180">-Confirm</span></span>
<span data-ttu-id="ead9f-181">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ead9f-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead9f-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead9f-182">-WhatIf</span></span>
<span data-ttu-id="ead9f-183">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ead9f-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead9f-184">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ead9f-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead9f-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead9f-185">CommonParameters</span></span>
<span data-ttu-id="ead9f-186">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead9f-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead9f-187">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ead9f-187">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead9f-188">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ead9f-188">INPUTS</span></span>

### <span data-ttu-id="ead9f-189">System. String</span><span class="sxs-lookup"><span data-stu-id="ead9f-189">System.String</span></span>

## <span data-ttu-id="ead9f-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ead9f-190">OUTPUTS</span></span>

### <span data-ttu-id="ead9f-191">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ead9f-191">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ead9f-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="ead9f-192">NOTES</span></span>

## <span data-ttu-id="ead9f-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ead9f-193">RELATED LINKS</span></span>

[<span data-ttu-id="ead9f-194">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ead9f-194">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="ead9f-195">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ead9f-195">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ead9f-196">Neu – AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ead9f-196">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="ead9f-197">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ead9f-197">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="ead9f-198">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ead9f-198">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="ead9f-199">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ead9f-199">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="ead9f-200">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ead9f-200">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="ead9f-201">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ead9f-201">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

