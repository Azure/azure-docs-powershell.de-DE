---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500369"
---
# <span data-ttu-id="2b641-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b641-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="2b641-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b641-102">SYNOPSIS</span></span>
<span data-ttu-id="2b641-103">Erstellt eine Datenbank oder eine elastische Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2b641-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b641-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b641-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b641-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b641-105">DESCRIPTION</span></span>
<span data-ttu-id="2b641-106">Das Cmdlet **New-AzureRmSqlDatabase** erstellt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2b641-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="2b641-107">Sie können auch eine elastische Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.</span><span class="sxs-lookup"><span data-stu-id="2b641-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="2b641-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b641-108">EXAMPLES</span></span>

### <span data-ttu-id="2b641-109">Beispiel 1: Erstellen einer Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="2b641-109">Example 1: Create a database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="2b641-110">Mit diesem Befehl wird eine Datenbank mit dem Namen Database01 auf dem Server Server01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b641-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="2b641-111">Beispiel 2: Erstellen einer elastischen Datenbank auf einem angegebenen Server</span><span class="sxs-lookup"><span data-stu-id="2b641-111">Example 2: Create an elastic database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="2b641-112">Dieser Befehl erstellt eine Datenbank mit dem Namen database01 im elastischen Pool mit dem Namen ElasticPool01 auf Server Server01.</span><span class="sxs-lookup"><span data-stu-id="2b641-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="2b641-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b641-113">PARAMETERS</span></span>

### <span data-ttu-id="2b641-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b641-114">-AsJob</span></span>
<span data-ttu-id="2b641-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2b641-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-116">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="2b641-116">-CatalogCollation</span></span>
<span data-ttu-id="2b641-117">Gibt den Namen der SQL-Datenbankkatalog Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="2b641-117">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-118">-Collation</span><span class="sxs-lookup"><span data-stu-id="2b641-118">-CollationName</span></span>
<span data-ttu-id="2b641-119">Gibt den Namen der SQL-Datenbanksortierung an.</span><span class="sxs-lookup"><span data-stu-id="2b641-119">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b641-120">-DatabaseName</span></span>
<span data-ttu-id="2b641-121">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="2b641-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b641-122">-DefaultProfile</span></span>
<span data-ttu-id="2b641-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2b641-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-124">-Edition</span><span class="sxs-lookup"><span data-stu-id="2b641-124">-Edition</span></span>
<span data-ttu-id="2b641-125">Gibt die Edition an, die der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b641-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="2b641-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2b641-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b641-127">Standard</span><span class="sxs-lookup"><span data-stu-id="2b641-127">Default</span></span>
- <span data-ttu-id="2b641-128">Keine</span><span class="sxs-lookup"><span data-stu-id="2b641-128">None</span></span>
- <span data-ttu-id="2b641-129">Premium</span><span class="sxs-lookup"><span data-stu-id="2b641-129">Premium</span></span>
- <span data-ttu-id="2b641-130">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="2b641-130">Basic</span></span>
- <span data-ttu-id="2b641-131">Standard</span><span class="sxs-lookup"><span data-stu-id="2b641-131">Standard</span></span>
- <span data-ttu-id="2b641-132">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="2b641-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-133">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2b641-133">-ElasticPoolName</span></span>
<span data-ttu-id="2b641-134">Gibt den Namen des elastischen Pools an, in dem die Datenbank abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b641-134">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="2b641-135">-MaxSizeBytes</span></span>
<span data-ttu-id="2b641-136">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="2b641-136">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="2b641-137">-ReadScale</span></span>
<span data-ttu-id="2b641-138">Die Option zum Lesen der Skalierung, die der Azure SQL-Datenbank zugewiesen werden soll. (Aktiviert/deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="2b641-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2b641-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="2b641-140">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b641-140">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b641-141">-ResourceGroupName</span></span>
<span data-ttu-id="2b641-142">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2b641-142">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-143">-Samplename</span><span class="sxs-lookup"><span data-stu-id="2b641-143">-SampleName</span></span>
<span data-ttu-id="2b641-144">Der Name des Beispiel Schemas, das beim Erstellen dieser Datenbank angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b641-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-145">-Servername</span><span class="sxs-lookup"><span data-stu-id="2b641-145">-ServerName</span></span>
<span data-ttu-id="2b641-146">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="2b641-146">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-147">-Tags</span><span class="sxs-lookup"><span data-stu-id="2b641-147">-Tags</span></span>
<span data-ttu-id="2b641-148">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet der neuen Datenbank zuordnet.</span><span class="sxs-lookup"><span data-stu-id="2b641-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="2b641-149">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2b641-149">For example:</span></span>

<span data-ttu-id="2b641-150">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2b641-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2b641-151">-ZoneRedundant</span></span>
<span data-ttu-id="2b641-152">Die Zonen Redundanz, die der Azure SQL-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="2b641-152">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b641-153">-Confirm</span></span>
<span data-ttu-id="2b641-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b641-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b641-155">-WhatIf</span></span>
<span data-ttu-id="2b641-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b641-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b641-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b641-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b641-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b641-158">CommonParameters</span></span>
<span data-ttu-id="2b641-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b641-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b641-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b641-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b641-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b641-161">INPUTS</span></span>

### <span data-ttu-id="2b641-162">Keine</span><span class="sxs-lookup"><span data-stu-id="2b641-162">None</span></span>
<span data-ttu-id="2b641-163">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2b641-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b641-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b641-164">OUTPUTS</span></span>

### <span data-ttu-id="2b641-165">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2b641-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2b641-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b641-166">NOTES</span></span>

## <span data-ttu-id="2b641-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b641-167">RELATED LINKS</span></span>

[<span data-ttu-id="2b641-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b641-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="2b641-169">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2b641-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2b641-170">Neu – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2b641-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="2b641-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b641-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="2b641-172">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b641-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="2b641-173">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b641-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="2b641-174">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b641-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="2b641-175">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="2b641-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
