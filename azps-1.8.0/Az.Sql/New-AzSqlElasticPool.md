---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fbc0d1e1ac32906c081c5a9714c8420e0f1292e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659098"
---
# <span data-ttu-id="0b639-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b639-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="0b639-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b639-102">SYNOPSIS</span></span>
<span data-ttu-id="0b639-103">Erstellt einen elastischen datenbankpool für eine SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0b639-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="0b639-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b639-104">SYNTAX</span></span>

### <span data-ttu-id="0b639-105">DtuBasedPool (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b639-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b639-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="0b639-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b639-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b639-107">DESCRIPTION</span></span>
<span data-ttu-id="0b639-108">Das Cmdlet **New-AzSqlElasticPool** erstellt einen elastischen datenbankpool für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0b639-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="0b639-109">Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b639-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="0b639-110">Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0b639-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="0b639-111">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0b639-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="0b639-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b639-112">EXAMPLES</span></span>

### <span data-ttu-id="0b639-113">Beispiel 1: Erstellen eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="0b639-113">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="0b639-114">Dieser Befehl erstellt einen elastischen Pool in der Standard Dienstebene mit dem Namen ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="0b639-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="0b639-115">Der Server mit dem Namen Server01, der einer Azure-Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist, hostet den elastischen Pool in.</span><span class="sxs-lookup"><span data-stu-id="0b639-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="0b639-116">Mit dem Befehl werden die DTU-Eigenschaftswerte für den Pool und die Datenbanken im Pool angegeben.</span><span class="sxs-lookup"><span data-stu-id="0b639-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="0b639-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b639-117">PARAMETERS</span></span>

### <span data-ttu-id="0b639-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b639-118">-AsJob</span></span>
<span data-ttu-id="0b639-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0b639-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b639-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0b639-120">-ComputeGeneration</span></span>
<span data-ttu-id="0b639-121">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b639-121">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="0b639-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="0b639-123">Gibt die maximale Anzahl von Datenbankdurchsatz Einheiten (DTUs) an, die eine einzelne Datenbank im Pool nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="0b639-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="0b639-124">Die Standardwerte für die verschiedenen Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b639-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="0b639-125">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="0b639-125">Basic.</span></span> <span data-ttu-id="0b639-126">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="0b639-126">5 DTUs</span></span>
- <span data-ttu-id="0b639-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="0b639-127">Standard.</span></span> <span data-ttu-id="0b639-128">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="0b639-128">100 DTUs</span></span>
- <span data-ttu-id="0b639-129">Premium.</span><span class="sxs-lookup"><span data-stu-id="0b639-129">Premium.</span></span> <span data-ttu-id="0b639-130">125 DTUs für Details, welche Werte gültig sind, finden Sie in der Tabelle Ihres speziellen Größen Pools in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) .</span><span class="sxs-lookup"><span data-stu-id="0b639-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="0b639-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="0b639-132">Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="0b639-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="0b639-133">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0b639-133">The default value is zero (0).</span></span>
<span data-ttu-id="0b639-134">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0b639-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="0b639-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="0b639-136">Die maxmium-Vcore-Nummer, die eine beliebige sqlazure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="0b639-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="0b639-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="0b639-138">Die minimale Vcore-Nummer, die eine beliebige sqlazure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="0b639-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b639-139">-DefaultProfile</span></span>
<span data-ttu-id="0b639-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b639-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b639-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="0b639-141">-Dtu</span></span>
<span data-ttu-id="0b639-142">Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="0b639-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="0b639-143">Die Standardwerte für die verschiedenen Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b639-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="0b639-144">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="0b639-144">Basic.</span></span>
<span data-ttu-id="0b639-145">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="0b639-145">100 DTUs</span></span>
- <span data-ttu-id="0b639-146">Standard.</span><span class="sxs-lookup"><span data-stu-id="0b639-146">Standard.</span></span>
<span data-ttu-id="0b639-147">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="0b639-147">100 DTUs</span></span>
- <span data-ttu-id="0b639-148">Premium.</span><span class="sxs-lookup"><span data-stu-id="0b639-148">Premium.</span></span>
<span data-ttu-id="0b639-149">125 DTUs für Details, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="0b639-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-150">-Edition</span><span class="sxs-lookup"><span data-stu-id="0b639-150">-Edition</span></span>
<span data-ttu-id="0b639-151">Gibt die Edition der Azure SQL-Datenbank an, die für den elastischen Pool verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b639-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="0b639-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b639-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b639-153">Keine</span><span class="sxs-lookup"><span data-stu-id="0b639-153">None</span></span>
- <span data-ttu-id="0b639-154">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="0b639-154">Basic</span></span>
- <span data-ttu-id="0b639-155">Standard</span><span class="sxs-lookup"><span data-stu-id="0b639-155">Standard</span></span>
- <span data-ttu-id="0b639-156">Premium</span><span class="sxs-lookup"><span data-stu-id="0b639-156">Premium</span></span>
- <span data-ttu-id="0b639-157">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="0b639-157">DataWarehouse</span></span>
- <span data-ttu-id="0b639-158">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="0b639-158">Free</span></span>
- <span data-ttu-id="0b639-159">Stretch</span><span class="sxs-lookup"><span data-stu-id="0b639-159">Stretch</span></span>
- <span data-ttu-id="0b639-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0b639-160">GeneralPurpose</span></span>
- <span data-ttu-id="0b639-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0b639-161">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0b639-162">-ElasticPoolName</span></span>
<span data-ttu-id="0b639-163">Gibt den Namen des von diesem Cmdlet erstellten elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="0b639-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0b639-164">-LicenseType</span></span>
<span data-ttu-id="0b639-165">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0b639-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0b639-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b639-166">-ResourceGroupName</span></span>
<span data-ttu-id="0b639-167">Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet den elastischen Pool zuweist.</span><span class="sxs-lookup"><span data-stu-id="0b639-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="0b639-168">-Servername</span><span class="sxs-lookup"><span data-stu-id="0b639-168">-ServerName</span></span>
<span data-ttu-id="0b639-169">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="0b639-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0b639-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="0b639-170">-StorageMB</span></span>
<span data-ttu-id="0b639-171">Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="0b639-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="0b639-172">Wenn Sie diesen Parameter nicht angeben, berechnet dieses Cmdlet einen Wert, der vom Wert des *DTU* -Parameters abhängt.</span><span class="sxs-lookup"><span data-stu-id="0b639-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="0b639-173">Siehe [eDTU-und Speichergrenzwerte](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) für mögliche Werte.</span><span class="sxs-lookup"><span data-stu-id="0b639-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="0b639-174">-Tags</span><span class="sxs-lookup"><span data-stu-id="0b639-174">-Tags</span></span>
<span data-ttu-id="0b639-175">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet dem elastischen Pool zuordnet.</span><span class="sxs-lookup"><span data-stu-id="0b639-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="0b639-176">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0b639-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0b639-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="0b639-177">-VCore</span></span>
<span data-ttu-id="0b639-178">Die Gesamtanzahl der freigegebenen Vcores für den SQL Azure Elastic-Pool.</span><span class="sxs-lookup"><span data-stu-id="0b639-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b639-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0b639-179">-ZoneRedundant</span></span>
<span data-ttu-id="0b639-180">Die Zonen Redundanz, die dem Azure SQL-elastischen Pool zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="0b639-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="0b639-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b639-181">-Confirm</span></span>
<span data-ttu-id="0b639-182">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b639-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b639-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b639-183">-WhatIf</span></span>
<span data-ttu-id="0b639-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b639-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b639-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b639-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b639-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b639-186">CommonParameters</span></span>
<span data-ttu-id="0b639-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b639-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b639-188">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b639-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b639-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b639-189">INPUTS</span></span>

### <span data-ttu-id="0b639-190">System. String</span><span class="sxs-lookup"><span data-stu-id="0b639-190">System.String</span></span>

## <span data-ttu-id="0b639-191">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b639-191">OUTPUTS</span></span>

### <span data-ttu-id="0b639-192">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="0b639-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0b639-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b639-193">NOTES</span></span>

## <span data-ttu-id="0b639-194">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b639-194">RELATED LINKS</span></span>

[<span data-ttu-id="0b639-195">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b639-195">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0b639-196">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0b639-196">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0b639-197">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0b639-197">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0b639-198">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b639-198">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="0b639-199">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b639-199">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="0b639-200">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="0b639-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
