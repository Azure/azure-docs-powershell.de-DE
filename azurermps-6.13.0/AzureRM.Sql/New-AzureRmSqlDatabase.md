---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664311"
---
# <span data-ttu-id="47894-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47894-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="47894-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47894-102">SYNOPSIS</span></span>
<span data-ttu-id="47894-103">Erstellt eine Datenbank oder eine elastische Datenbank.</span><span class="sxs-lookup"><span data-stu-id="47894-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47894-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47894-104">SYNTAX</span></span>

### <span data-ttu-id="47894-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="47894-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47894-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="47894-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47894-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47894-107">DESCRIPTION</span></span>
<span data-ttu-id="47894-108">Das Cmdlet **New-AzureRmSqlDatabase** erstellt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="47894-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="47894-109">Sie können auch eine elastische Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="47894-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="47894-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47894-110">EXAMPLES</span></span>

### <span data-ttu-id="47894-111">Beispiel 1: Erstellen einer Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="47894-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="47894-112">Mit diesem Befehl wird eine Datenbank mit dem Namen Database01 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="47894-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="47894-113">Beispiel 2: Erstellen einer elastischen Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="47894-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="47894-114">Dieser Befehl erstellt eine Datenbank mit dem Namen Database02 im elastischen Pool mit dem Namen ElasticPool01 auf Server Server01.</span><span class="sxs-lookup"><span data-stu-id="47894-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="47894-115">Beispiel 3: Erstellen einer Vcore-Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="47894-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="47894-116">Mit diesem Befehl wird eine Vcore-Datenbank mit dem Namen Database03 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="47894-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="47894-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="47894-117">PARAMETERS</span></span>

### <span data-ttu-id="47894-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47894-118">-AsJob</span></span>
<span data-ttu-id="47894-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="47894-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47894-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="47894-120">-CatalogCollation</span></span>
<span data-ttu-id="47894-121">Gibt den Namen der SQL-Datenbankkatalog Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="47894-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="47894-122">-Collation</span><span class="sxs-lookup"><span data-stu-id="47894-122">-CollationName</span></span>
<span data-ttu-id="47894-123">Gibt den Namen der SQL-Datenbanksortierung an.</span><span class="sxs-lookup"><span data-stu-id="47894-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="47894-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="47894-124">-ComputeGeneration</span></span>
<span data-ttu-id="47894-125">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="47894-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="47894-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47894-126">-DatabaseName</span></span>
<span data-ttu-id="47894-127">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="47894-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="47894-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47894-128">-DefaultProfile</span></span>
<span data-ttu-id="47894-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="47894-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47894-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="47894-130">-Edition</span></span>
<span data-ttu-id="47894-131">Gibt die Edition an, die der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="47894-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="47894-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="47894-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47894-133">Keine</span><span class="sxs-lookup"><span data-stu-id="47894-133">None</span></span>
- <span data-ttu-id="47894-134">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="47894-134">Basic</span></span>
- <span data-ttu-id="47894-135">Standard</span><span class="sxs-lookup"><span data-stu-id="47894-135">Standard</span></span>
- <span data-ttu-id="47894-136">Premium</span><span class="sxs-lookup"><span data-stu-id="47894-136">Premium</span></span>
- <span data-ttu-id="47894-137">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="47894-137">DataWarehouse</span></span>
- <span data-ttu-id="47894-138">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="47894-138">Free</span></span>
- <span data-ttu-id="47894-139">Stretch</span><span class="sxs-lookup"><span data-stu-id="47894-139">Stretch</span></span>
- <span data-ttu-id="47894-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="47894-140">GeneralPurpose</span></span>
- <span data-ttu-id="47894-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="47894-141">BusinessCritical</span></span>

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

### <span data-ttu-id="47894-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="47894-142">-ElasticPoolName</span></span>
<span data-ttu-id="47894-143">Gibt den Namen des elastischen Pools an, in dem die Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="47894-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="47894-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="47894-144">-LicenseType</span></span>
<span data-ttu-id="47894-145">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="47894-145">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="47894-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="47894-146">-MaxSizeBytes</span></span>
<span data-ttu-id="47894-147">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="47894-147">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="47894-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="47894-148">-ReadScale</span></span>
<span data-ttu-id="47894-149">Die Option zum Lesen der Skalierung, die der Azure SQL-Datenbank zugewiesen werden soll. (Aktiviert/deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="47894-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="47894-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="47894-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="47894-151">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="47894-151">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="47894-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47894-152">-ResourceGroupName</span></span>
<span data-ttu-id="47894-153">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="47894-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="47894-154">-Samplename</span><span class="sxs-lookup"><span data-stu-id="47894-154">-SampleName</span></span>
<span data-ttu-id="47894-155">Der Name des Beispiel Schemas, das beim Erstellen dieser Datenbank angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47894-155">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="47894-156">-Servername</span><span class="sxs-lookup"><span data-stu-id="47894-156">-ServerName</span></span>
<span data-ttu-id="47894-157">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="47894-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="47894-158">-Tags</span><span class="sxs-lookup"><span data-stu-id="47894-158">-Tags</span></span>
<span data-ttu-id="47894-159">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet der neuen Datenbank zuordnet.</span><span class="sxs-lookup"><span data-stu-id="47894-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="47894-160">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="47894-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="47894-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="47894-161">-VCore</span></span>
<span data-ttu-id="47894-162">Die Vcore-Nummer für die Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="47894-162">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="47894-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="47894-163">-ZoneRedundant</span></span>
<span data-ttu-id="47894-164">Die Zonen Redundanz, die der Azure SQL-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="47894-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="47894-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47894-165">-Confirm</span></span>
<span data-ttu-id="47894-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47894-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47894-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47894-167">-WhatIf</span></span>
<span data-ttu-id="47894-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47894-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47894-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47894-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47894-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47894-170">CommonParameters</span></span>
<span data-ttu-id="47894-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47894-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47894-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47894-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47894-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47894-173">INPUTS</span></span>

### <span data-ttu-id="47894-174">System. String</span><span class="sxs-lookup"><span data-stu-id="47894-174">System.String</span></span>

## <span data-ttu-id="47894-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47894-175">OUTPUTS</span></span>

### <span data-ttu-id="47894-176">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="47894-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="47894-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="47894-177">NOTES</span></span>

## <span data-ttu-id="47894-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47894-178">RELATED LINKS</span></span>

[<span data-ttu-id="47894-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47894-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="47894-180">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47894-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="47894-181">Neu – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="47894-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="47894-182">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47894-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="47894-183">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47894-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="47894-184">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47894-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="47894-185">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47894-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="47894-186">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="47894-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

