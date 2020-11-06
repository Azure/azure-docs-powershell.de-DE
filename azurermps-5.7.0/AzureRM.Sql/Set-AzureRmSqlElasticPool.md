---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498702"
---
# <span data-ttu-id="ca9bf-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ca9bf-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="ca9bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9bf-103">Ändert die Eigenschaften eines elastischen Daten Bank Pools in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca9bf-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca9bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9bf-106">Das Cmdlet " **Set-AzureRmSqlElasticPool** " legt Eigenschaften für einen elastischen Pool in Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="ca9bf-107">Mit diesem Cmdlet können die eDTUs pro Pool ( *DTU* ), die maximale Speichergröße pro Pool ( *StorageMB* ), maximale eDTUs pro Datenbank ( *DatabaseDtuMax* ) und minimale eDTUs pro Datenbank ( *DatqabaseDtuMin* ) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="ca9bf-108">Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="ca9bf-109">Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="ca9bf-110">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca9bf-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="ca9bf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca9bf-111">EXAMPLES</span></span>

### <span data-ttu-id="ca9bf-112">Beispiel 1: Ändern der Eigenschaften eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="ca9bf-112">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="ca9bf-113">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="ca9bf-114">Mit dem Befehl wird die Anzahl der DTUs für den elastischen Pool auf 1000 und die Mindest-und höchst DTUs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="ca9bf-115">Beispiel 2: Ändern der maximalen Speichergröße eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="ca9bf-115">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="ca9bf-116">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="ca9bf-117">Der Befehl legt den Max-Speicher für einen elastischen Pool auf 2 TB fest.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="ca9bf-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca9bf-118">PARAMETERS</span></span>

### <span data-ttu-id="ca9bf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca9bf-119">-AsJob</span></span>
<span data-ttu-id="ca9bf-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ca9bf-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="ca9bf-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="ca9bf-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="ca9bf-122">Gibt die maximale Anzahl von DTUs an, die eine einzelne Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="ca9bf-123">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca9bf-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="ca9bf-124">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca9bf-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="ca9bf-125">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-125">Basic.</span></span>  <span data-ttu-id="ca9bf-126">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca9bf-126">5 DTUs</span></span>
- <span data-ttu-id="ca9bf-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-127">Standard.</span></span> <span data-ttu-id="ca9bf-128">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca9bf-128">100 DTUs</span></span>
- <span data-ttu-id="ca9bf-129">Premium.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-129">Premium.</span></span> <span data-ttu-id="ca9bf-130">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca9bf-130">125 DTUs</span></span>


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9bf-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="ca9bf-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="ca9bf-132">Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="ca9bf-133">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca9bf-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="ca9bf-134">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ca9bf-134">The default value is zero (0).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9bf-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9bf-135">-DefaultProfile</span></span>
<span data-ttu-id="ca9bf-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ca9bf-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca9bf-137">-DTU</span><span class="sxs-lookup"><span data-stu-id="ca9bf-137">-Dtu</span></span>
<span data-ttu-id="ca9bf-138">Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="ca9bf-139">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca9bf-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="ca9bf-140">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca9bf-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="ca9bf-141">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-141">Basic.</span></span> <span data-ttu-id="ca9bf-142">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca9bf-142">100 DTUs</span></span>
- <span data-ttu-id="ca9bf-143">Standard.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-143">Standard.</span></span> <span data-ttu-id="ca9bf-144">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca9bf-144">100 DTUs</span></span>
- <span data-ttu-id="ca9bf-145">Premium.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-145">Premium.</span></span> <span data-ttu-id="ca9bf-146">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca9bf-146">125 DTUs</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9bf-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="ca9bf-147">-Edition</span></span>
<span data-ttu-id="ca9bf-148">Gibt die Edition der Azure SQL-Datenbank für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="ca9bf-149">Sie können die Edition nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-149">You cannot change the edition.</span></span> <span data-ttu-id="ca9bf-150">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca9bf-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ca9bf-151">Keine</span><span class="sxs-lookup"><span data-stu-id="ca9bf-151">None</span></span>
- <span data-ttu-id="ca9bf-152">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="ca9bf-152">Basic</span></span>
- <span data-ttu-id="ca9bf-153">Standard</span><span class="sxs-lookup"><span data-stu-id="ca9bf-153">Standard</span></span>
- <span data-ttu-id="ca9bf-154">Premium</span><span class="sxs-lookup"><span data-stu-id="ca9bf-154">Premium</span></span>
- <span data-ttu-id="ca9bf-155">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="ca9bf-155">DataWarehouse</span></span>

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

### <span data-ttu-id="ca9bf-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ca9bf-156">-ElasticPoolName</span></span>
<span data-ttu-id="ca9bf-157">Gibt den Namen des elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-157">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="ca9bf-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9bf-158">-ResourceGroupName</span></span>
<span data-ttu-id="ca9bf-159">Gibt den Namen der Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="ca9bf-160">-Servername</span><span class="sxs-lookup"><span data-stu-id="ca9bf-160">-ServerName</span></span>
<span data-ttu-id="ca9bf-161">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-161">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="ca9bf-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="ca9bf-162">-StorageMB</span></span>
<span data-ttu-id="ca9bf-163">Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="ca9bf-164">Weitere Informationen finden Sie im New-AzureRmSqlElasticPool-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9bf-165">-Tags</span><span class="sxs-lookup"><span data-stu-id="ca9bf-165">-Tags</span></span>
<span data-ttu-id="ca9bf-166">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an, die dieses Cmdlet dem elastischen Pool in Form einer Hashtabelle zuordnet.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="ca9bf-167">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ca9bf-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="ca9bf-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ca9bf-168">-ZoneRedundant</span></span>
<span data-ttu-id="ca9bf-169">Die Zonen Redundanz, die dem Azure SQL-elastischen Pool zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="ca9bf-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="ca9bf-170">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ca9bf-170">-Confirm</span></span>
<span data-ttu-id="ca9bf-171">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9bf-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9bf-172">-WhatIf</span></span>
<span data-ttu-id="ca9bf-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca9bf-174">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9bf-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9bf-175">CommonParameters</span></span>
<span data-ttu-id="ca9bf-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9bf-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9bf-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9bf-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca9bf-178">INPUTS</span></span>

### <span data-ttu-id="ca9bf-179">Keine</span><span class="sxs-lookup"><span data-stu-id="ca9bf-179">None</span></span>
<span data-ttu-id="ca9bf-180">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ca9bf-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca9bf-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca9bf-181">OUTPUTS</span></span>

### <span data-ttu-id="ca9bf-182">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="ca9bf-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="ca9bf-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca9bf-183">NOTES</span></span>

## <span data-ttu-id="ca9bf-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca9bf-184">RELATED LINKS</span></span>

[<span data-ttu-id="ca9bf-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ca9bf-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ca9bf-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ca9bf-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="ca9bf-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ca9bf-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="ca9bf-188">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ca9bf-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ca9bf-189">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ca9bf-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
