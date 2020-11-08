---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 180cd3c8d9301ab287bc4a37c13f7b07276f7794
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995573"
---
# <span data-ttu-id="7e064-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e064-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="7e064-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e064-102">SYNOPSIS</span></span>
<span data-ttu-id="7e064-103">Legt Eigenschaften für eine Datenbank fest oder verschiebt eine vorhandene Datenbank in einen elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="7e064-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="7e064-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e064-104">SYNTAX</span></span>

### <span data-ttu-id="7e064-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e064-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e064-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="7e064-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e064-107">Umbenennen</span><span class="sxs-lookup"><span data-stu-id="7e064-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e064-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e064-108">DESCRIPTION</span></span>
<span data-ttu-id="7e064-109">Das Cmdlet " **Set-AzSqlDatabase** " legt Eigenschaften für eine Datenbank in Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="7e064-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="7e064-110">Mit diesem Cmdlet können die Dienstebene ( *Edition* ), die Leistungsstufe ( *RequestedServiceObjectiveName* ) und die Speicher-Max-Größe ( *MaxSizeBytes* ) für die Datenbank geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7e064-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="7e064-111">Darüber hinaus können Sie den *ElasticPoolName* -Parameter angeben, um eine Datenbank in einen elastischen Pool zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7e064-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="7e064-112">Wenn sich eine Datenbank bereits in einem elastischen Pool befindet, können Sie den *RequestedServiceObjectiveName* -Parameter verwenden, um die Datenbank aus einem elastischen Pool in eine Leistungsstufe für einzelne Datenbanken zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7e064-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="7e064-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e064-113">EXAMPLES</span></span>

### <span data-ttu-id="7e064-114">Beispiel 1: Aktualisieren einer Datenbank auf eine Standard-S0-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7e064-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="7e064-115">Mit diesem Befehl wird eine Datenbank mit dem Namen database01 in eine Standard-S0-Datenbank auf einem Server mit dem Namen Server01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7e064-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="7e064-116">Beispiel 2: Hinzufügen einer Datenbank zu einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="7e064-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="7e064-117">Dieser Befehl fügt dem elastischen Pool mit dem Namen ElasticPool01, der auf dem Server mit dem Namen Server01 gehostet wird, eine Datenbank mit dem Namen database01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e064-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="7e064-118">Beispiel 3: Ändern der maximalen Speichergröße einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="7e064-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="7e064-119">Mit diesem Befehl wird eine Datenbank mit dem Namen database01 aktualisiert, um die maximale Größe auf 1 TB zu setzen.</span><span class="sxs-lookup"><span data-stu-id="7e064-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="7e064-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e064-120">PARAMETERS</span></span>

### <span data-ttu-id="7e064-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e064-121">-AsJob</span></span>
<span data-ttu-id="7e064-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7e064-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e064-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="7e064-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="7e064-124">Die automatische Pausen Verzögerung in Minuten für Datenbank (nur serverlos),-1 zum Abmelden</span><span class="sxs-lookup"><span data-stu-id="7e064-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="7e064-125">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="7e064-125">-ComputeGeneration</span></span>
<span data-ttu-id="7e064-126">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e064-126">The compute generation to assign.</span></span>

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

### <span data-ttu-id="7e064-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="7e064-127">-ComputeModel</span></span>
<span data-ttu-id="7e064-128">Berechnetes Modell der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7e064-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="7e064-129">Serverlos oder bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="7e064-129">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="7e064-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e064-130">-DatabaseName</span></span>
<span data-ttu-id="7e064-131">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="7e064-131">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="7e064-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e064-132">-DefaultProfile</span></span>
<span data-ttu-id="7e064-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7e064-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e064-134">-Edition</span><span class="sxs-lookup"><span data-stu-id="7e064-134">-Edition</span></span>
<span data-ttu-id="7e064-135">Gibt die Edition für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="7e064-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="7e064-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7e064-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e064-137">Keine</span><span class="sxs-lookup"><span data-stu-id="7e064-137">None</span></span>
- <span data-ttu-id="7e064-138">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="7e064-138">Basic</span></span>
- <span data-ttu-id="7e064-139">Standard</span><span class="sxs-lookup"><span data-stu-id="7e064-139">Standard</span></span>
- <span data-ttu-id="7e064-140">Premium</span><span class="sxs-lookup"><span data-stu-id="7e064-140">Premium</span></span>
- <span data-ttu-id="7e064-141">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="7e064-141">DataWarehouse</span></span>
- <span data-ttu-id="7e064-142">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="7e064-142">Free</span></span>
- <span data-ttu-id="7e064-143">Stretch</span><span class="sxs-lookup"><span data-stu-id="7e064-143">Stretch</span></span>
- <span data-ttu-id="7e064-144">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="7e064-144">GeneralPurpose</span></span>
- <span data-ttu-id="7e064-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="7e064-145">BusinessCritical</span></span>

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

### <span data-ttu-id="7e064-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7e064-146">-ElasticPoolName</span></span>
<span data-ttu-id="7e064-147">Gibt den Namen des elastischen Pools an, in dem die Datenbank verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e064-147">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="7e064-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7e064-148">-LicenseType</span></span>
<span data-ttu-id="7e064-149">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7e064-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="7e064-150">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="7e064-150">Possible values are:</span></span>
- <span data-ttu-id="7e064-151">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="7e064-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="7e064-152">Der Daten Bank Preis wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="7e064-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="7e064-153">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="7e064-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="7e064-154">Der Daten Bank Preis enthält eine neue SQL Server-Lizenzgebühr.</span><span class="sxs-lookup"><span data-stu-id="7e064-154">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="7e064-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="7e064-155">-MaxSizeBytes</span></span>
<span data-ttu-id="7e064-156">Die maximale Größe der Azure SQL-Datenbank in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7e064-156">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="7e064-157">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="7e064-157">-MinimumCapacity</span></span>
<span data-ttu-id="7e064-158">Die minimale Kapazität, die die Datenbank immer zugewiesen hat, wenn Sie nicht angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="7e064-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="7e064-159">Nur für Server-Azure SQL-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="7e064-159">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="7e064-160">-Name</span><span class="sxs-lookup"><span data-stu-id="7e064-160">-NewName</span></span>
<span data-ttu-id="7e064-161">Der neue Name, in den die Datenbank umbenannt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e064-161">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="7e064-162">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7e064-162">-ReadReplicaCount</span></span>
<span data-ttu-id="7e064-163">Die Anzahl der ReadOnly-sekundären Replikate, die der Datenbank zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7e064-163">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="7e064-164">Nur für die hoch skalierte Edition.</span><span class="sxs-lookup"><span data-stu-id="7e064-164">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="7e064-165">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="7e064-165">-ReadScale</span></span>
<span data-ttu-id="7e064-166">Wenn diese Option aktiviert ist, können Verbindungen, deren Verbindungszeichenfolge auf ReadOnly festgesetzt ist, möglicherweise an ein ReadOnly-sekundäres Replikat weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="7e064-166">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="7e064-167">Diese Eigenschaft kann nur für unternehmenskritische Premium-und geschäftskritische Datenbanken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e064-167">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="7e064-168">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="7e064-168">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="7e064-169">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e064-169">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="7e064-170">Informationen zu den Dienst Zielen finden Sie unter [Azure SQL-Datenbankdienst Ebenen und Leistungsstufen](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in der Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="7e064-170">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="7e064-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e064-171">-ResourceGroupName</span></span>
<span data-ttu-id="7e064-172">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7e064-172">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7e064-173">-Servername</span><span class="sxs-lookup"><span data-stu-id="7e064-173">-ServerName</span></span>
<span data-ttu-id="7e064-174">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="7e064-174">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7e064-175">-Tags</span><span class="sxs-lookup"><span data-stu-id="7e064-175">-Tags</span></span>
<span data-ttu-id="7e064-176">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="7e064-176">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7e064-177">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="7e064-177">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7e064-178">-VCore</span><span class="sxs-lookup"><span data-stu-id="7e064-178">-VCore</span></span>
<span data-ttu-id="7e064-179">Die Vcore-Nummer für die Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7e064-179">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="7e064-180">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7e064-180">-ZoneRedundant</span></span>
<span data-ttu-id="7e064-181">Die Zonen Redundanz, die der Azure SQL-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="7e064-181">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="7e064-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e064-182">-Confirm</span></span>
<span data-ttu-id="7e064-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e064-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e064-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e064-184">-WhatIf</span></span>
<span data-ttu-id="7e064-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e064-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e064-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e064-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e064-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e064-187">CommonParameters</span></span>
<span data-ttu-id="7e064-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e064-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e064-189">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e064-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e064-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e064-190">INPUTS</span></span>

### <span data-ttu-id="7e064-191">System. String</span><span class="sxs-lookup"><span data-stu-id="7e064-191">System.String</span></span>

## <span data-ttu-id="7e064-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e064-192">OUTPUTS</span></span>

### <span data-ttu-id="7e064-193">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7e064-193">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7e064-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e064-194">NOTES</span></span>

## <span data-ttu-id="7e064-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e064-195">RELATED LINKS</span></span>

[<span data-ttu-id="7e064-196">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e064-196">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="7e064-197">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e064-197">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="7e064-198">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e064-198">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="7e064-199">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e064-199">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="7e064-200">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e064-200">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="7e064-201">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7e064-201">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
