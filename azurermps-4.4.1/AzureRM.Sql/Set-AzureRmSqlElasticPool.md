---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481421"
---
# <span data-ttu-id="280c2-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="280c2-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="280c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="280c2-102">SYNOPSIS</span></span>
<span data-ttu-id="280c2-103">Ändert die Eigenschaften eines elastischen Daten Bank Pools in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="280c2-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="280c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="280c2-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="280c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="280c2-105">DESCRIPTION</span></span>
<span data-ttu-id="280c2-106">Das Cmdlet " **Satz-AzureRmSqlElasticPool** " ändert Eigenschaften für einen elastischen datenbankpool in einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="280c2-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="280c2-107">Mit diesem Cmdlet können die Mindest-Datenbankdurchsatz Einheiten (DTUs) pro Datenbank sowie die maximale DTUs pro Datenbank, die Anzahl der DTUs für den Pool und die Speichergrenze für den Pool geändert werden.</span><span class="sxs-lookup"><span data-stu-id="280c2-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="280c2-108">Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="280c2-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="280c2-109">Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="280c2-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="280c2-110">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="280c2-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="280c2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="280c2-111">EXAMPLES</span></span>

### <span data-ttu-id="280c2-112">Beispiel 1: Ändern der Eigenschaften eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="280c2-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="280c2-113">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="280c2-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="280c2-114">Mit dem Befehl wird die Anzahl der DTUs für den elastischen Pool auf 1000 und die Mindest-und höchst DTUs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="280c2-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="280c2-115">Beispiel 2: Ändern des Max-Speichers eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="280c2-115">Example 2: Modify the max storage of an elastic pool</span></span>
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

<span data-ttu-id="280c2-116">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="280c2-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="280c2-117">Der Befehl legt den Max-Speicher für einen elastischen Pool auf 2 TB fest.</span><span class="sxs-lookup"><span data-stu-id="280c2-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="280c2-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="280c2-118">PARAMETERS</span></span>

### <span data-ttu-id="280c2-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="280c2-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="280c2-120">Gibt die maximale Anzahl von DTUs an, die eine einzelne Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="280c2-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="280c2-121">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="280c2-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="280c2-122">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="280c2-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="280c2-123">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="280c2-123">Basic.</span></span>  <span data-ttu-id="280c2-124">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="280c2-124">5 DTUs</span></span>
- <span data-ttu-id="280c2-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="280c2-125">Standard.</span></span> <span data-ttu-id="280c2-126">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="280c2-126">100 DTUs</span></span>
- <span data-ttu-id="280c2-127">Premium.</span><span class="sxs-lookup"><span data-stu-id="280c2-127">Premium.</span></span> <span data-ttu-id="280c2-128">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="280c2-128">125 DTUs</span></span>


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

### <span data-ttu-id="280c2-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="280c2-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="280c2-130">Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="280c2-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="280c2-131">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="280c2-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="280c2-132">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="280c2-132">The default value is zero (0).</span></span>

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

### <span data-ttu-id="280c2-133">-DTU</span><span class="sxs-lookup"><span data-stu-id="280c2-133">-Dtu</span></span>
<span data-ttu-id="280c2-134">Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="280c2-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="280c2-135">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="280c2-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="280c2-136">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="280c2-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="280c2-137">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="280c2-137">Basic.</span></span> <span data-ttu-id="280c2-138">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="280c2-138">100 DTUs</span></span>
- <span data-ttu-id="280c2-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="280c2-139">Standard.</span></span> <span data-ttu-id="280c2-140">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="280c2-140">100 DTUs</span></span>
- <span data-ttu-id="280c2-141">Premium.</span><span class="sxs-lookup"><span data-stu-id="280c2-141">Premium.</span></span> <span data-ttu-id="280c2-142">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="280c2-142">125 DTUs</span></span>

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

### <span data-ttu-id="280c2-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="280c2-143">-Edition</span></span>
<span data-ttu-id="280c2-144">Gibt die Edition der Azure SQL-Datenbank für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="280c2-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="280c2-145">Sie können die Edition nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="280c2-145">You cannot change the edition.</span></span> <span data-ttu-id="280c2-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="280c2-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="280c2-147">Keine</span><span class="sxs-lookup"><span data-stu-id="280c2-147">None</span></span>
- <span data-ttu-id="280c2-148">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="280c2-148">Basic</span></span>
- <span data-ttu-id="280c2-149">Standard</span><span class="sxs-lookup"><span data-stu-id="280c2-149">Standard</span></span>
- <span data-ttu-id="280c2-150">Premium</span><span class="sxs-lookup"><span data-stu-id="280c2-150">Premium</span></span>
- <span data-ttu-id="280c2-151">Premiums</span><span class="sxs-lookup"><span data-stu-id="280c2-151">PremiumRS</span></span>
- <span data-ttu-id="280c2-152">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="280c2-152">DataWarehouse</span></span>
- <span data-ttu-id="280c2-153">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="280c2-153">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280c2-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="280c2-154">-ElasticPoolName</span></span>
<span data-ttu-id="280c2-155">Gibt den Namen des elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="280c2-155">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="280c2-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="280c2-156">-ResourceGroupName</span></span>
<span data-ttu-id="280c2-157">Gibt den Namen der Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="280c2-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="280c2-158">-Servername</span><span class="sxs-lookup"><span data-stu-id="280c2-158">-ServerName</span></span>
<span data-ttu-id="280c2-159">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="280c2-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="280c2-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="280c2-160">-StorageMB</span></span>
<span data-ttu-id="280c2-161">Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="280c2-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="280c2-162">Weitere Informationen finden Sie im New-AzureRmSqlElasticPool-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="280c2-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="280c2-163">-Tags</span><span class="sxs-lookup"><span data-stu-id="280c2-163">-Tags</span></span>
<span data-ttu-id="280c2-164">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an, die dieses Cmdlet dem elastischen Pool in Form einer Hashtabelle zuordnet.</span><span class="sxs-lookup"><span data-stu-id="280c2-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="280c2-165">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="280c2-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="280c2-166">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="280c2-166">-Confirm</span></span>
<span data-ttu-id="280c2-167">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="280c2-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="280c2-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="280c2-168">-WhatIf</span></span>
<span data-ttu-id="280c2-169">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="280c2-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="280c2-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="280c2-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="280c2-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280c2-171">-DefaultProfile</span></span>
<span data-ttu-id="280c2-172">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="280c2-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="280c2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280c2-173">CommonParameters</span></span>
<span data-ttu-id="280c2-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="280c2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280c2-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="280c2-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280c2-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="280c2-176">INPUTS</span></span>

## <span data-ttu-id="280c2-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="280c2-177">OUTPUTS</span></span>

### <span data-ttu-id="280c2-178">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="280c2-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="280c2-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="280c2-179">NOTES</span></span>

## <span data-ttu-id="280c2-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="280c2-180">RELATED LINKS</span></span>

[<span data-ttu-id="280c2-181">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="280c2-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="280c2-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="280c2-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="280c2-183">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="280c2-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="280c2-184">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="280c2-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="280c2-185">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="280c2-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
