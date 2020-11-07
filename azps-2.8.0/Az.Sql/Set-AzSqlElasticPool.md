---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: d78ca6ef2e342982dc6f5e53e8fff4de606dd5ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825736"
---
# <span data-ttu-id="9c98a-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9c98a-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="9c98a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c98a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c98a-103">Ändert die Eigenschaften eines elastischen Daten Bank Pools in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9c98a-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="9c98a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c98a-104">SYNTAX</span></span>

### <span data-ttu-id="9c98a-105">DtuBasedPool (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c98a-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c98a-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="9c98a-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c98a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c98a-107">DESCRIPTION</span></span>
<span data-ttu-id="9c98a-108">Das Cmdlet " **Set-AzSqlElasticPool** " legt Eigenschaften für einen elastischen Pool in Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="9c98a-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="9c98a-109">Mit diesem Cmdlet können die eDTUs pro Pool ( *DTU* ), die maximale Speichergröße pro Pool ( *StorageMB* ), maximale eDTUs pro Datenbank ( *DatabaseDtuMax* ) und minimale eDTUs pro Datenbank ( *DatabaseDtuMin* ) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9c98a-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="9c98a-110">Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c98a-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="9c98a-111">Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c98a-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="9c98a-112">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9c98a-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="9c98a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c98a-113">EXAMPLES</span></span>

### <span data-ttu-id="9c98a-114">Beispiel 1: Ändern der Eigenschaften eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="9c98a-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="9c98a-115">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="9c98a-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="9c98a-116">Mit dem Befehl wird die Anzahl der DTUs für den elastischen Pool auf 1000 und die Mindest-und höchst DTUs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c98a-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="9c98a-117">Beispiel 2: Ändern der maximalen Speichergröße eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="9c98a-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="9c98a-118">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="9c98a-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="9c98a-119">Der Befehl legt den Max-Speicher für einen elastischen Pool auf 2 TB fest.</span><span class="sxs-lookup"><span data-stu-id="9c98a-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="9c98a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c98a-120">PARAMETERS</span></span>

### <span data-ttu-id="9c98a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c98a-121">-AsJob</span></span>
<span data-ttu-id="9c98a-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9c98a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c98a-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9c98a-123">-ComputeGeneration</span></span>
<span data-ttu-id="9c98a-124">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c98a-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c98a-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="9c98a-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="9c98a-126">Gibt die maximale Anzahl von DTUs an, die eine einzelne Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="9c98a-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="9c98a-127">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9c98a-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="9c98a-128">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c98a-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="9c98a-129">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="9c98a-129">Basic.</span></span>  <span data-ttu-id="9c98a-130">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="9c98a-130">5 DTUs</span></span>
- <span data-ttu-id="9c98a-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="9c98a-131">Standard.</span></span> <span data-ttu-id="9c98a-132">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="9c98a-132">100 DTUs</span></span>
- <span data-ttu-id="9c98a-133">Premium.</span><span class="sxs-lookup"><span data-stu-id="9c98a-133">Premium.</span></span> <span data-ttu-id="9c98a-134">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="9c98a-134">125 DTUs</span></span>

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

### <span data-ttu-id="9c98a-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="9c98a-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="9c98a-136">Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="9c98a-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="9c98a-137">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9c98a-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="9c98a-138">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9c98a-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="9c98a-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="9c98a-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="9c98a-140">Die maximale Vcore-Nummer, die eine sqlazure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="9c98a-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="9c98a-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="9c98a-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="9c98a-142">Die minimale Vcore-Nummer, die eine beliebige sqlazure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="9c98a-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="9c98a-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c98a-143">-DefaultProfile</span></span>
<span data-ttu-id="9c98a-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9c98a-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c98a-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="9c98a-145">-Dtu</span></span>
<span data-ttu-id="9c98a-146">Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="9c98a-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="9c98a-147">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="9c98a-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="9c98a-148">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c98a-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="9c98a-149">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="9c98a-149">Basic.</span></span> <span data-ttu-id="9c98a-150">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="9c98a-150">100 DTUs</span></span>
- <span data-ttu-id="9c98a-151">Standard.</span><span class="sxs-lookup"><span data-stu-id="9c98a-151">Standard.</span></span> <span data-ttu-id="9c98a-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="9c98a-152">100 DTUs</span></span>
- <span data-ttu-id="9c98a-153">Premium.</span><span class="sxs-lookup"><span data-stu-id="9c98a-153">Premium.</span></span> <span data-ttu-id="9c98a-154">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="9c98a-154">125 DTUs</span></span>

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

### <span data-ttu-id="9c98a-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="9c98a-155">-Edition</span></span>
<span data-ttu-id="9c98a-156">Gibt die Edition der Azure SQL-Datenbank für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="9c98a-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="9c98a-157">Sie können die Edition nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="9c98a-157">You cannot change the edition.</span></span> <span data-ttu-id="9c98a-158">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c98a-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c98a-159">Keine</span><span class="sxs-lookup"><span data-stu-id="9c98a-159">None</span></span>
- <span data-ttu-id="9c98a-160">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="9c98a-160">Basic</span></span>
- <span data-ttu-id="9c98a-161">Standard</span><span class="sxs-lookup"><span data-stu-id="9c98a-161">Standard</span></span>
- <span data-ttu-id="9c98a-162">Premium</span><span class="sxs-lookup"><span data-stu-id="9c98a-162">Premium</span></span>
- <span data-ttu-id="9c98a-163">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="9c98a-163">DataWarehouse</span></span>
- <span data-ttu-id="9c98a-164">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="9c98a-164">Free</span></span>
- <span data-ttu-id="9c98a-165">Stretch</span><span class="sxs-lookup"><span data-stu-id="9c98a-165">Stretch</span></span>
- <span data-ttu-id="9c98a-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="9c98a-166">GeneralPurpose</span></span>
- <span data-ttu-id="9c98a-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="9c98a-167">BusinessCritical</span></span>

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

### <span data-ttu-id="9c98a-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9c98a-168">-ElasticPoolName</span></span>
<span data-ttu-id="9c98a-169">Gibt den Namen des elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="9c98a-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="9c98a-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9c98a-170">-LicenseType</span></span>
<span data-ttu-id="9c98a-171">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9c98a-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="9c98a-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c98a-172">-ResourceGroupName</span></span>
<span data-ttu-id="9c98a-173">Gibt den Namen der Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9c98a-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="9c98a-174">-Servername</span><span class="sxs-lookup"><span data-stu-id="9c98a-174">-ServerName</span></span>
<span data-ttu-id="9c98a-175">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="9c98a-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="9c98a-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="9c98a-176">-StorageMB</span></span>
<span data-ttu-id="9c98a-177">Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="9c98a-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="9c98a-178">Weitere Informationen finden Sie im New-AzSqlElasticPool-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c98a-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="9c98a-179">-Tags</span><span class="sxs-lookup"><span data-stu-id="9c98a-179">-Tags</span></span>
<span data-ttu-id="9c98a-180">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an, die dieses Cmdlet dem elastischen Pool in Form einer Hashtabelle zuordnet.</span><span class="sxs-lookup"><span data-stu-id="9c98a-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="9c98a-181">Zum Beispiel: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="9c98a-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="9c98a-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="9c98a-182">-VCore</span></span>
<span data-ttu-id="9c98a-183">Die Gesamtanzahl der freigegebenen Vcore für den SQL Azure Elastic-Pool.</span><span class="sxs-lookup"><span data-stu-id="9c98a-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c98a-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="9c98a-184">-ZoneRedundant</span></span>
<span data-ttu-id="9c98a-185">Die Zonen Redundanz, die dem Azure SQL-elastischen Pool zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="9c98a-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="9c98a-186">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c98a-186">-Confirm</span></span>
<span data-ttu-id="9c98a-187">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c98a-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c98a-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c98a-188">-WhatIf</span></span>
<span data-ttu-id="9c98a-189">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c98a-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c98a-190">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c98a-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c98a-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c98a-191">CommonParameters</span></span>
<span data-ttu-id="9c98a-192">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c98a-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c98a-193">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c98a-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c98a-194">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c98a-194">INPUTS</span></span>

### <span data-ttu-id="9c98a-195">System. String</span><span class="sxs-lookup"><span data-stu-id="9c98a-195">System.String</span></span>

## <span data-ttu-id="9c98a-196">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c98a-196">OUTPUTS</span></span>

### <span data-ttu-id="9c98a-197">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="9c98a-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="9c98a-198">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c98a-198">NOTES</span></span>

## <span data-ttu-id="9c98a-199">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c98a-199">RELATED LINKS</span></span>

[<span data-ttu-id="9c98a-200">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9c98a-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="9c98a-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="9c98a-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="9c98a-202">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="9c98a-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="9c98a-203">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9c98a-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="9c98a-204">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9c98a-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
