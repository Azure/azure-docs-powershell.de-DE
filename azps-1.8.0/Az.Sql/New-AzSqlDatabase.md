---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659114"
---
# <span data-ttu-id="b056c-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b056c-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="b056c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b056c-102">SYNOPSIS</span></span>
<span data-ttu-id="b056c-103">Erstellt eine Datenbank oder eine elastische Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b056c-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="b056c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b056c-104">SYNTAX</span></span>

### <span data-ttu-id="b056c-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="b056c-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b056c-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="b056c-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b056c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b056c-107">DESCRIPTION</span></span>
<span data-ttu-id="b056c-108">Das Cmdlet **New-AzSqlDatabase** erstellt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b056c-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="b056c-109">Sie können auch eine elastische Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="b056c-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="b056c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b056c-110">EXAMPLES</span></span>

### <span data-ttu-id="b056c-111">Beispiel 1: Erstellen einer Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="b056c-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="b056c-112">Mit diesem Befehl wird eine Datenbank mit dem Namen Database01 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="b056c-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="b056c-113">Beispiel 2: Erstellen einer elastischen Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="b056c-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="b056c-114">Dieser Befehl erstellt eine Datenbank mit dem Namen Database02 im elastischen Pool mit dem Namen ElasticPool01 auf Server Server01.</span><span class="sxs-lookup"><span data-stu-id="b056c-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="b056c-115">Beispiel 3: Erstellen einer Vcore-Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="b056c-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="b056c-116">Mit diesem Befehl wird eine Vcore-Datenbank mit dem Namen Database03 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="b056c-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="b056c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b056c-117">PARAMETERS</span></span>

### <span data-ttu-id="b056c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b056c-118">-AsJob</span></span>
<span data-ttu-id="b056c-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b056c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b056c-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="b056c-120">-CatalogCollation</span></span>
<span data-ttu-id="b056c-121">Gibt den Namen der SQL-Datenbankkatalog Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="b056c-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="b056c-122">-Collation</span><span class="sxs-lookup"><span data-stu-id="b056c-122">-CollationName</span></span>
<span data-ttu-id="b056c-123">Gibt den Namen der SQL-Datenbanksortierung an.</span><span class="sxs-lookup"><span data-stu-id="b056c-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="b056c-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b056c-124">-ComputeGeneration</span></span>
<span data-ttu-id="b056c-125">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b056c-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="b056c-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b056c-126">-DatabaseName</span></span>
<span data-ttu-id="b056c-127">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="b056c-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="b056c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b056c-128">-DefaultProfile</span></span>
<span data-ttu-id="b056c-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b056c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b056c-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="b056c-130">-Edition</span></span>
<span data-ttu-id="b056c-131">Gibt die Edition an, die der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b056c-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="b056c-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b056c-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b056c-133">Keine</span><span class="sxs-lookup"><span data-stu-id="b056c-133">None</span></span>
- <span data-ttu-id="b056c-134">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="b056c-134">Basic</span></span>
- <span data-ttu-id="b056c-135">Standard</span><span class="sxs-lookup"><span data-stu-id="b056c-135">Standard</span></span>
- <span data-ttu-id="b056c-136">Premium</span><span class="sxs-lookup"><span data-stu-id="b056c-136">Premium</span></span>
- <span data-ttu-id="b056c-137">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="b056c-137">DataWarehouse</span></span>
- <span data-ttu-id="b056c-138">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="b056c-138">Free</span></span>
- <span data-ttu-id="b056c-139">Stretch</span><span class="sxs-lookup"><span data-stu-id="b056c-139">Stretch</span></span>
- <span data-ttu-id="b056c-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b056c-140">GeneralPurpose</span></span>
- <span data-ttu-id="b056c-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b056c-141">BusinessCritical</span></span>

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

### <span data-ttu-id="b056c-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b056c-142">-ElasticPoolName</span></span>
<span data-ttu-id="b056c-143">Gibt den Namen des elastischen Pools an, in dem die Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b056c-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="b056c-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b056c-144">-LicenseType</span></span>
<span data-ttu-id="b056c-145">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b056c-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="b056c-146">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="b056c-146">Possible values are:</span></span>
- <span data-ttu-id="b056c-147">Grundpr.-Azure Hybrid Benefit (AHB) Discounted Pricing für vorhandene SQL Server-Lizenzbesitzer wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="b056c-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="b056c-148">Der Daten Bank Preis wird für vorhandene SQL Server-Lizenzbesitzer abgezinst.</span><span class="sxs-lookup"><span data-stu-id="b056c-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="b056c-149">LicenseIncluded-Azure Hybrid Benefit (AHB) Preisnachlässe für vorhandene SQL Server-Lizenzbesitzer werden nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="b056c-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="b056c-150">Der Daten Bank Preis enthält eine neue SQL Server-Lizenzgebühr.</span><span class="sxs-lookup"><span data-stu-id="b056c-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="b056c-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="b056c-151">-MaxSizeBytes</span></span>
<span data-ttu-id="b056c-152">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="b056c-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="b056c-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="b056c-153">-ReadScale</span></span>
<span data-ttu-id="b056c-154">Die Option zum Lesen der Skalierung, die der Azure SQL-Datenbank zugewiesen werden soll. (Aktiviert/deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="b056c-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="b056c-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b056c-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="b056c-156">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b056c-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="b056c-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b056c-157">-ResourceGroupName</span></span>
<span data-ttu-id="b056c-158">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b056c-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b056c-159">-Samplename</span><span class="sxs-lookup"><span data-stu-id="b056c-159">-SampleName</span></span>
<span data-ttu-id="b056c-160">Der Name des Beispiel Schemas, das beim Erstellen dieser Datenbank angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b056c-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="b056c-161">-Servername</span><span class="sxs-lookup"><span data-stu-id="b056c-161">-ServerName</span></span>
<span data-ttu-id="b056c-162">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="b056c-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b056c-163">-Tags</span><span class="sxs-lookup"><span data-stu-id="b056c-163">-Tags</span></span>
<span data-ttu-id="b056c-164">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet der neuen Datenbank zuordnet.</span><span class="sxs-lookup"><span data-stu-id="b056c-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="b056c-165">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="b056c-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b056c-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="b056c-166">-VCore</span></span>
<span data-ttu-id="b056c-167">Die Vcore-Nummer für die Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="b056c-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b056c-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b056c-168">-ZoneRedundant</span></span>
<span data-ttu-id="b056c-169">Die Zonen Redundanz, die der Azure SQL-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="b056c-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="b056c-170">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b056c-170">-Confirm</span></span>
<span data-ttu-id="b056c-171">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b056c-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b056c-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b056c-172">-WhatIf</span></span>
<span data-ttu-id="b056c-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b056c-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b056c-174">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b056c-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b056c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b056c-175">CommonParameters</span></span>
<span data-ttu-id="b056c-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b056c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b056c-177">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b056c-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b056c-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b056c-178">INPUTS</span></span>

### <span data-ttu-id="b056c-179">System. String</span><span class="sxs-lookup"><span data-stu-id="b056c-179">System.String</span></span>

## <span data-ttu-id="b056c-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b056c-180">OUTPUTS</span></span>

### <span data-ttu-id="b056c-181">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b056c-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b056c-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="b056c-182">NOTES</span></span>

## <span data-ttu-id="b056c-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b056c-183">RELATED LINKS</span></span>

[<span data-ttu-id="b056c-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b056c-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b056c-185">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b056c-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="b056c-186">Neu – AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b056c-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="b056c-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b056c-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="b056c-188">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b056c-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="b056c-189">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b056c-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="b056c-190">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b056c-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="b056c-191">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b056c-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

