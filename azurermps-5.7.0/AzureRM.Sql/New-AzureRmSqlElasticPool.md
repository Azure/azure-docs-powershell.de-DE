---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498742"
---
# <span data-ttu-id="80243-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80243-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="80243-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80243-102">SYNOPSIS</span></span>
<span data-ttu-id="80243-103">Erstellt einen elastischen datenbankpool für eine SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="80243-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80243-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80243-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80243-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80243-105">DESCRIPTION</span></span>
<span data-ttu-id="80243-106">Das Cmdlet **New-AzureRmSqlElasticPool** erstellt einen elastischen datenbankpool für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="80243-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="80243-107">Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80243-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="80243-108">Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="80243-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="80243-109">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="80243-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="80243-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80243-110">EXAMPLES</span></span>

### <span data-ttu-id="80243-111">Beispiel 1: Erstellen eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="80243-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="80243-112">Dieser Befehl erstellt einen elastischen Pool in der Standard Dienstebene mit dem Namen ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="80243-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="80243-113">Der Server mit dem Namen Server01, der einer Azure-Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist, hostet den elastischen Pool in.</span><span class="sxs-lookup"><span data-stu-id="80243-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="80243-114">Mit dem Befehl werden die DTU-Eigenschaftswerte für den Pool und die Datenbanken im Pool angegeben.</span><span class="sxs-lookup"><span data-stu-id="80243-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="80243-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="80243-115">PARAMETERS</span></span>

### <span data-ttu-id="80243-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80243-116">-AsJob</span></span>
<span data-ttu-id="80243-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="80243-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="80243-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="80243-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="80243-119">Gibt die maximale Anzahl von Datenbankdurchsatz Einheiten (DTUs) an, die eine einzelne Datenbank im Pool nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="80243-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="80243-120">Die Standardwerte für die verschiedenen Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80243-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="80243-121">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="80243-121">Basic.</span></span> <span data-ttu-id="80243-122">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="80243-122">5 DTUs</span></span>
- <span data-ttu-id="80243-123">Standard.</span><span class="sxs-lookup"><span data-stu-id="80243-123">Standard.</span></span> <span data-ttu-id="80243-124">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="80243-124">100 DTUs</span></span>
- <span data-ttu-id="80243-125">Premium.</span><span class="sxs-lookup"><span data-stu-id="80243-125">Premium.</span></span> <span data-ttu-id="80243-126">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="80243-126">125 DTUs</span></span>

<span data-ttu-id="80243-127">Informationen dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) .</span><span class="sxs-lookup"><span data-stu-id="80243-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="80243-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="80243-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="80243-129">Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="80243-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="80243-130">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="80243-130">The default value is zero (0).</span></span>

<span data-ttu-id="80243-131">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="80243-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="80243-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80243-132">-DefaultProfile</span></span>
<span data-ttu-id="80243-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80243-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80243-134">-DTU</span><span class="sxs-lookup"><span data-stu-id="80243-134">-Dtu</span></span>
<span data-ttu-id="80243-135">Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="80243-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="80243-136">Die Standardwerte für die verschiedenen Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80243-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="80243-137">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="80243-137">Basic.</span></span>
<span data-ttu-id="80243-138">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="80243-138">100 DTUs</span></span>
- <span data-ttu-id="80243-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="80243-139">Standard.</span></span>
<span data-ttu-id="80243-140">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="80243-140">100 DTUs</span></span>
- <span data-ttu-id="80243-141">Premium.</span><span class="sxs-lookup"><span data-stu-id="80243-141">Premium.</span></span>
<span data-ttu-id="80243-142">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="80243-142">125 DTUs</span></span>

<span data-ttu-id="80243-143">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="80243-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="80243-144">-Edition</span><span class="sxs-lookup"><span data-stu-id="80243-144">-Edition</span></span>
<span data-ttu-id="80243-145">Gibt die Edition der Azure SQL-Datenbank an, die für den elastischen Pool verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80243-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="80243-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80243-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80243-147">Premium</span><span class="sxs-lookup"><span data-stu-id="80243-147">Premium</span></span>
- <span data-ttu-id="80243-148">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="80243-148">Basic</span></span>
- <span data-ttu-id="80243-149">Standard</span><span class="sxs-lookup"><span data-stu-id="80243-149">Standard</span></span>
- <span data-ttu-id="80243-150">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="80243-150">DataWarehouse</span></span>
- <span data-ttu-id="80243-151">Stretch</span><span class="sxs-lookup"><span data-stu-id="80243-151">Stretch</span></span>

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

### <span data-ttu-id="80243-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="80243-152">-ElasticPoolName</span></span>
<span data-ttu-id="80243-153">Gibt den Namen des von diesem Cmdlet erstellten elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="80243-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="80243-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80243-154">-ResourceGroupName</span></span>
<span data-ttu-id="80243-155">Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet den elastischen Pool zuweist.</span><span class="sxs-lookup"><span data-stu-id="80243-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="80243-156">-Servername</span><span class="sxs-lookup"><span data-stu-id="80243-156">-ServerName</span></span>
<span data-ttu-id="80243-157">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="80243-157">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="80243-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="80243-158">-StorageMB</span></span>
<span data-ttu-id="80243-159">Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="80243-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="80243-160">Wenn Sie diesen Parameter nicht angeben, berechnet dieses Cmdlet einen Wert, der vom Wert des *DTU* -Parameters abhängt.</span><span class="sxs-lookup"><span data-stu-id="80243-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="80243-161">Siehe [eDTU-und Speichergrenzwerte](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) für mögliche Werte.</span><span class="sxs-lookup"><span data-stu-id="80243-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="80243-162">-Tags</span><span class="sxs-lookup"><span data-stu-id="80243-162">-Tags</span></span>
<span data-ttu-id="80243-163">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet dem elastischen Pool zuordnet.</span><span class="sxs-lookup"><span data-stu-id="80243-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="80243-164">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="80243-164">For example:</span></span>

<span data-ttu-id="80243-165">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="80243-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="80243-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="80243-166">-ZoneRedundant</span></span>
<span data-ttu-id="80243-167">Die Zonen Redundanz, die dem Azure SQL-elastischen Pool zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="80243-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="80243-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80243-168">-Confirm</span></span>
<span data-ttu-id="80243-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80243-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80243-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80243-170">-WhatIf</span></span>
<span data-ttu-id="80243-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80243-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80243-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80243-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80243-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80243-173">CommonParameters</span></span>
<span data-ttu-id="80243-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80243-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80243-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80243-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80243-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80243-176">INPUTS</span></span>

### <span data-ttu-id="80243-177">Keine</span><span class="sxs-lookup"><span data-stu-id="80243-177">None</span></span>
<span data-ttu-id="80243-178">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="80243-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80243-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80243-179">OUTPUTS</span></span>

### <span data-ttu-id="80243-180">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="80243-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="80243-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="80243-181">NOTES</span></span>

## <span data-ttu-id="80243-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80243-182">RELATED LINKS</span></span>

[<span data-ttu-id="80243-183">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80243-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="80243-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="80243-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="80243-185">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="80243-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="80243-186">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80243-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="80243-187">Satz-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="80243-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="80243-188">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="80243-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
