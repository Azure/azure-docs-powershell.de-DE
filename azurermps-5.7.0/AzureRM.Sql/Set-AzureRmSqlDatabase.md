---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: b0493433f7419039acacd696748b3c5f9518aef5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480798"
---
# <span data-ttu-id="dad8a-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dad8a-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="dad8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dad8a-102">SYNOPSIS</span></span>
<span data-ttu-id="dad8a-103">Legt Eigenschaften für eine Datenbank fest oder verschiebt eine vorhandene Datenbank in einen elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="dad8a-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dad8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dad8a-104">SYNTAX</span></span>

### <span data-ttu-id="dad8a-105">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="dad8a-105">Update</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad8a-106">Umbenennen</span><span class="sxs-lookup"><span data-stu-id="dad8a-106">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dad8a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dad8a-107">DESCRIPTION</span></span>
<span data-ttu-id="dad8a-108">Das Cmdlet " **Set-AzureRmSqlDatabase** " legt Eigenschaften für eine Datenbank in Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="dad8a-108">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="dad8a-109">Mit diesem Cmdlet können die Dienstebene ( *Edition* ), die Leistungsstufe ( *RequestedServiceObjectiveName* ) und die Speicher-Max-Größe ( *MaxSizeBytes* ) für die Datenbank geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dad8a-109">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="dad8a-110">Darüber hinaus können Sie den *ElasticPoolName* -Parameter angeben, um eine Datenbank in einen elastischen Pool zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="dad8a-110">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="dad8a-111">Wenn sich eine Datenbank bereits in einem elastischen Pool befindet, können Sie den *RequestedServiceObjectiveName* -Parameter verwenden, um die Datenbank aus einem elastischen Pool in eine Leistungsstufe für einzelne Datenbanken zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="dad8a-111">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="dad8a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dad8a-112">EXAMPLES</span></span>

### <span data-ttu-id="dad8a-113">Beispiel 1: Aktualisieren einer Datenbank auf eine Standard-S2-Datenbank</span><span class="sxs-lookup"><span data-stu-id="dad8a-113">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="dad8a-114">Mit diesem Befehl wird eine Datenbank mit dem Namen database01 in eine Standard-S2-Datenbank auf einem Server mit dem Namen Server01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dad8a-114">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="dad8a-115">Beispiel 2: Hinzufügen einer Datenbank zu einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="dad8a-115">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="dad8a-116">Dieser Befehl fügt dem elastischen Pool mit dem Namen ElasticPool01, der auf dem Server mit dem Namen Server01 gehostet wird, eine Datenbank mit dem Namen database01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="dad8a-116">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="dad8a-117">Beispiel 3: Ändern der maximalen Speichergröße einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="dad8a-117">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
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

<span data-ttu-id="dad8a-118">Mit diesem Befehl wird eine Datenbank mit dem Namen database01 aktualisiert, um die maximale Größe auf 1 TB zu setzen.</span><span class="sxs-lookup"><span data-stu-id="dad8a-118">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="dad8a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="dad8a-119">PARAMETERS</span></span>

### <span data-ttu-id="dad8a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad8a-120">-AsJob</span></span>
<span data-ttu-id="dad8a-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dad8a-121">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="dad8a-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dad8a-122">-DatabaseName</span></span>
<span data-ttu-id="dad8a-123">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="dad8a-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad8a-124">-DefaultProfile</span></span>
<span data-ttu-id="dad8a-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dad8a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dad8a-126">-Edition</span><span class="sxs-lookup"><span data-stu-id="dad8a-126">-Edition</span></span>
<span data-ttu-id="dad8a-127">Gibt die Edition für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="dad8a-127">Specifies the edition for the database.</span></span>
<span data-ttu-id="dad8a-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="dad8a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dad8a-129">Keine</span><span class="sxs-lookup"><span data-stu-id="dad8a-129">None</span></span>
- <span data-ttu-id="dad8a-130">Premium</span><span class="sxs-lookup"><span data-stu-id="dad8a-130">Premium</span></span>
- <span data-ttu-id="dad8a-131">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="dad8a-131">Basic</span></span>
- <span data-ttu-id="dad8a-132">Standard</span><span class="sxs-lookup"><span data-stu-id="dad8a-132">Standard</span></span>
- <span data-ttu-id="dad8a-133">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="dad8a-133">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: Update
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-134">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="dad8a-134">-ElasticPoolName</span></span>
<span data-ttu-id="dad8a-135">Gibt den Namen des elastischen Pools an, in dem die Datenbank verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="dad8a-135">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-136">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="dad8a-136">-MaxSizeBytes</span></span>
<span data-ttu-id="dad8a-137">Die maximale Größe der Azure SQL-Datenbank in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dad8a-137">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="dad8a-138">-NewName</span></span>
<span data-ttu-id="dad8a-139">Der neue Name, in den die Datenbank umbenannt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dad8a-139">The new name to rename the database to.</span></span>

```yaml
Type: String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-140">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="dad8a-140">-ReadScale</span></span>
<span data-ttu-id="dad8a-141">Die Option zum Lesen der Skalierung, die der Azure SQL-Datenbank zugewiesen werden soll. (Aktiviert/deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="dad8a-141">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: Update
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-142">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="dad8a-142">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="dad8a-143">Gibt den Namen des Dienst Ziels an, das der Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dad8a-143">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="dad8a-144">Informationen zu den Dienst Zielen finden Sie unter [Azure SQL-Datenbankdienst Ebenen und Leistungsstufen](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in der Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="dad8a-144">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad8a-145">-ResourceGroupName</span></span>
<span data-ttu-id="dad8a-146">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dad8a-146">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dad8a-147">-Servername</span><span class="sxs-lookup"><span data-stu-id="dad8a-147">-ServerName</span></span>
<span data-ttu-id="dad8a-148">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="dad8a-148">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="dad8a-149">-Tags</span><span class="sxs-lookup"><span data-stu-id="dad8a-149">-Tags</span></span>
<span data-ttu-id="dad8a-150">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="dad8a-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dad8a-151">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dad8a-151">For example:</span></span>

<span data-ttu-id="dad8a-152">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="dad8a-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Update
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-153">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="dad8a-153">-ZoneRedundant</span></span>
<span data-ttu-id="dad8a-154">Die Zonen Redundanz, die der Azure SQL-Datenbank zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="dad8a-154">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad8a-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dad8a-155">-Confirm</span></span>
<span data-ttu-id="dad8a-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dad8a-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad8a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad8a-157">-WhatIf</span></span>
<span data-ttu-id="dad8a-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dad8a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad8a-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dad8a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad8a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad8a-160">CommonParameters</span></span>
<span data-ttu-id="dad8a-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad8a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad8a-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad8a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad8a-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dad8a-163">INPUTS</span></span>

### <span data-ttu-id="dad8a-164">Keine</span><span class="sxs-lookup"><span data-stu-id="dad8a-164">None</span></span>
<span data-ttu-id="dad8a-165">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="dad8a-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dad8a-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dad8a-166">OUTPUTS</span></span>

### <span data-ttu-id="dad8a-167">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="dad8a-167">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="dad8a-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="dad8a-168">NOTES</span></span>

## <span data-ttu-id="dad8a-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dad8a-169">RELATED LINKS</span></span>

[<span data-ttu-id="dad8a-170">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dad8a-170">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="dad8a-171">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dad8a-171">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="dad8a-172">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dad8a-172">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="dad8a-173">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dad8a-173">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="dad8a-174">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="dad8a-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="dad8a-175">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="dad8a-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
