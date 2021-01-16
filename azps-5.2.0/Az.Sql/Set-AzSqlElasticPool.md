---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296356"
---
# <span data-ttu-id="6e66c-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6e66c-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="6e66c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e66c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e66c-103">Ändert die Eigenschaften eines Datenbankpools in Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6e66c-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="6e66c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e66c-104">SYNTAX</span></span>

### <span data-ttu-id="6e66c-105">DtuBasedPool (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e66c-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e66c-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="6e66c-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e66c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e66c-107">DESCRIPTION</span></span>
<span data-ttu-id="6e66c-108">Das **Cmdlet "Set-AzSqlElasticPool"** legt Eigenschaften für einen Pool in Azure SQL fest.</span><span class="sxs-lookup"><span data-stu-id="6e66c-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="6e66c-109">Mit diesem Cmdlet können die eDTUs pro Pool *(Dtu),* die maximale Speichergröße pro Pool *(StorageMB),* die maximalen eDTUs pro Datenbank *(DatabaseDtuMax)* und die minimalen eDTUs pro Datenbank *(DatabaseDtuMin)* geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6e66c-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="6e66c-110">Für mehrere Parameter *("-Dtu", "-DatabaseDtuMin" und "-DatabaseDtuMax")* muss der Festgelegte Wert aus der Liste der gültigen Werte für diesen Parameter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e66c-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="6e66c-111">Beispielsweise kann "-DatabaseDtuMax" für einen Standardmäßigen 100 eDTU-Pool nur auf 10, 20, 50 oder 100 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6e66c-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="6e66c-112">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6e66c-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="6e66c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e66c-113">EXAMPLES</span></span>

### <span data-ttu-id="6e66c-114">Beispiel 1: Ändern der Eigenschaften für einen Pool mit Pool</span><span class="sxs-lookup"><span data-stu-id="6e66c-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
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

<span data-ttu-id="6e66c-115">Mit diesem Befehl werden die Eigenschaften für einen Pool mit dem Namen "poolpool01" geändert.</span><span class="sxs-lookup"><span data-stu-id="6e66c-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="6e66c-116">Mit dem Befehl wird die Anzahl der DTUs für den Pool für den Pool auf 1000 und die kleinsten und maximalen DTUs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6e66c-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="6e66c-117">Beispiel 2: Ändern der maximalen Speichergröße eines Pool im Pool</span><span class="sxs-lookup"><span data-stu-id="6e66c-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
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

<span data-ttu-id="6e66c-118">Mit diesem Befehl werden die Eigenschaften für einen Pool mit dem Namen "poolpool01" geändert.</span><span class="sxs-lookup"><span data-stu-id="6e66c-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="6e66c-119">Mit dem Befehl wird der maximale Speicher für einen Pool mit Pool und Pool auf 2 TB begrenzt.</span><span class="sxs-lookup"><span data-stu-id="6e66c-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="6e66c-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6e66c-120">Example 3</span></span>

<span data-ttu-id="6e66c-121">Ändert die Eigenschaften eines Datenbankpools in Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6e66c-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="6e66c-122">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="6e66c-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="6e66c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e66c-123">PARAMETERS</span></span>

### <span data-ttu-id="6e66c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e66c-124">-AsJob</span></span>
<span data-ttu-id="6e66c-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6e66c-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e66c-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6e66c-126">-ComputeGeneration</span></span>
<span data-ttu-id="6e66c-127">Die zuzuordnende Rechengenerierung.</span><span class="sxs-lookup"><span data-stu-id="6e66c-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="6e66c-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="6e66c-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="6e66c-129">Gibt die maximale Anzahl von DTUs an, die jede einzelne Datenbank im Pool nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="6e66c-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="6e66c-130">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6e66c-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="6e66c-131">Die Standardwerte für verschiedene Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6e66c-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="6e66c-132">Standard.</span><span class="sxs-lookup"><span data-stu-id="6e66c-132">Basic.</span></span>  <span data-ttu-id="6e66c-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="6e66c-133">5 DTUs</span></span>
- <span data-ttu-id="6e66c-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="6e66c-134">Standard.</span></span> <span data-ttu-id="6e66c-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6e66c-135">100 DTUs</span></span>
- <span data-ttu-id="6e66c-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="6e66c-136">Premium.</span></span> <span data-ttu-id="6e66c-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="6e66c-137">125 DTUs</span></span>

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

### <span data-ttu-id="6e66c-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="6e66c-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="6e66c-139">Gibt die Mindestanzahl von DTUs an, die der Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="6e66c-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="6e66c-140">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6e66c-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="6e66c-141">Der Standardwert ist null (0).</span><span class="sxs-lookup"><span data-stu-id="6e66c-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="6e66c-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="6e66c-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="6e66c-143">Die maximale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verbrauchen kann.</span><span class="sxs-lookup"><span data-stu-id="6e66c-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="6e66c-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="6e66c-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="6e66c-145">Die minimale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verbrauchen kann.</span><span class="sxs-lookup"><span data-stu-id="6e66c-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="6e66c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e66c-146">-DefaultProfile</span></span>
<span data-ttu-id="6e66c-147">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6e66c-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e66c-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="6e66c-148">-Dtu</span></span>
<span data-ttu-id="6e66c-149">Gibt die Gesamtzahl der freigegebenen DTUs für den Pool des Pools an.</span><span class="sxs-lookup"><span data-stu-id="6e66c-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="6e66c-150">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6e66c-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="6e66c-151">Die Standardwerte für verschiedene Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6e66c-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="6e66c-152">Standard.</span><span class="sxs-lookup"><span data-stu-id="6e66c-152">Basic.</span></span> <span data-ttu-id="6e66c-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6e66c-153">100 DTUs</span></span>
- <span data-ttu-id="6e66c-154">Standard.</span><span class="sxs-lookup"><span data-stu-id="6e66c-154">Standard.</span></span> <span data-ttu-id="6e66c-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6e66c-155">100 DTUs</span></span>
- <span data-ttu-id="6e66c-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="6e66c-156">Premium.</span></span> <span data-ttu-id="6e66c-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="6e66c-157">125 DTUs</span></span>

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

### <span data-ttu-id="6e66c-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="6e66c-158">-Edition</span></span>
<span data-ttu-id="6e66c-159">Gibt die Edition der Azure SQL Datenbank für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="6e66c-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="6e66c-160">Sie können die Edition nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="6e66c-160">You cannot change the edition.</span></span> <span data-ttu-id="6e66c-161">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6e66c-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e66c-162">Keine</span><span class="sxs-lookup"><span data-stu-id="6e66c-162">None</span></span>
- <span data-ttu-id="6e66c-163">Standard</span><span class="sxs-lookup"><span data-stu-id="6e66c-163">Basic</span></span>
- <span data-ttu-id="6e66c-164">Standard</span><span class="sxs-lookup"><span data-stu-id="6e66c-164">Standard</span></span>
- <span data-ttu-id="6e66c-165">Premium</span><span class="sxs-lookup"><span data-stu-id="6e66c-165">Premium</span></span>
- <span data-ttu-id="6e66c-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="6e66c-166">DataWarehouse</span></span>
- <span data-ttu-id="6e66c-167">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="6e66c-167">Free</span></span>
- <span data-ttu-id="6e66c-168">Strecken</span><span class="sxs-lookup"><span data-stu-id="6e66c-168">Stretch</span></span>
- <span data-ttu-id="6e66c-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="6e66c-169">GeneralPurpose</span></span>
- <span data-ttu-id="6e66c-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="6e66c-170">BusinessCritical</span></span>

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

### <span data-ttu-id="6e66c-171">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6e66c-171">-ElasticPoolName</span></span>
<span data-ttu-id="6e66c-172">Gibt den Namen des Poolpools an.</span><span class="sxs-lookup"><span data-stu-id="6e66c-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="6e66c-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6e66c-173">-LicenseType</span></span>
<span data-ttu-id="6e66c-174">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6e66c-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="6e66c-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e66c-175">-ResourceGroupName</span></span>
<span data-ttu-id="6e66c-176">Gibt den Namen der Ressourcengruppe an, der der Pool "Pool" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6e66c-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="6e66c-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e66c-177">-ServerName</span></span>
<span data-ttu-id="6e66c-178">Gibt den Namen des Servers an, auf dem sich der Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="6e66c-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="6e66c-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="6e66c-179">-StorageMB</span></span>
<span data-ttu-id="6e66c-180">Gibt die Speichergrenze in Megabyte für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="6e66c-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="6e66c-181">Weitere Informationen finden Sie im New-AzSqlElasticPool Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e66c-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="6e66c-182">-Tags</span><span class="sxs-lookup"><span data-stu-id="6e66c-182">-Tags</span></span>
<span data-ttu-id="6e66c-183">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an, das dieses Cmdlet dem Pool des Pool in Form einer Hashtabelle zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="6e66c-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="6e66c-184">Zum Beispiel: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="6e66c-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="6e66c-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="6e66c-185">-VCore</span></span>
<span data-ttu-id="6e66c-186">Die Gesamtzahl der freigegebenen Vcore für den Sql Azure-Pool".</span><span class="sxs-lookup"><span data-stu-id="6e66c-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="6e66c-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="6e66c-187">-ZoneRedundant</span></span>
<span data-ttu-id="6e66c-188">Die Zonenredundanz, die dem Azure Sql-Pool (Pool für Sql-Pool) zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="6e66c-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="6e66c-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e66c-189">-Confirm</span></span>
<span data-ttu-id="6e66c-190">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e66c-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e66c-191">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6e66c-191">-WhatIf</span></span>
<span data-ttu-id="6e66c-192">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e66c-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e66c-193">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e66c-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e66c-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e66c-194">CommonParameters</span></span>
<span data-ttu-id="6e66c-195">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e66c-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e66c-196">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e66c-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e66c-197">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e66c-197">INPUTS</span></span>

### <span data-ttu-id="6e66c-198">System.String</span><span class="sxs-lookup"><span data-stu-id="6e66c-198">System.String</span></span>

## <span data-ttu-id="6e66c-199">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e66c-199">OUTPUTS</span></span>

### <span data-ttu-id="6e66c-200">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="6e66c-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6e66c-201">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6e66c-201">NOTES</span></span>

## <span data-ttu-id="6e66c-202">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6e66c-202">RELATED LINKS</span></span>

[<span data-ttu-id="6e66c-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6e66c-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="6e66c-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6e66c-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="6e66c-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="6e66c-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="6e66c-206">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6e66c-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="6e66c-207">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="6e66c-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
