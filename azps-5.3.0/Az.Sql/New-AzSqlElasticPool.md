---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460707"
---
# <span data-ttu-id="49dcd-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49dcd-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="49dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="49dcd-103">Erstellt einen Datenbankpool für eine Datenbank SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="49dcd-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="49dcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49dcd-104">SYNTAX</span></span>

### <span data-ttu-id="49dcd-105">DtuBasedPool (Standard)</span><span class="sxs-lookup"><span data-stu-id="49dcd-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49dcd-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="49dcd-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49dcd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49dcd-107">DESCRIPTION</span></span>
<span data-ttu-id="49dcd-108">Das **Cmdlet "New-AzSqlElasticPool"** erstellt einen Datenbankpool im Datenbankpool für eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="49dcd-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="49dcd-109">Für mehrere Parameter *("-Dtu", "-DatabaseDtuMin" und "-DatabaseDtuMax")* muss der Festgelegte Wert aus der Liste der gültigen Werte für diesen Parameter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="49dcd-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="49dcd-110">Beispielsweise kann "-DatabaseDtuMax" für einen Standardmäßigen 100 eDTU-Pool nur auf 10, 20, 50 oder 100 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="49dcd-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="49dcd-111">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für ihren speziellen Größenpool in [Pool in Schwimmpools.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="49dcd-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="49dcd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49dcd-112">EXAMPLES</span></span>

### <span data-ttu-id="49dcd-113">Beispiel 1: Erstellen eines Pool für TTU-Pool</span><span class="sxs-lookup"><span data-stu-id="49dcd-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
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

<span data-ttu-id="49dcd-114">Mit diesem Befehl wird ein Pool mit dem Namen "Poolpool01" der Standarddienststufe erstellt.</span><span class="sxs-lookup"><span data-stu-id="49dcd-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="49dcd-115">Der Server mit dem Namen "server01", der einer Azure-Ressourcengruppe namens "ResourceGroup01" zugewiesen ist, hostet den Pool "Pool".</span><span class="sxs-lookup"><span data-stu-id="49dcd-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="49dcd-116">Der Befehl gibt die Werte der "DTU"-Eigenschaft für den Pool und die Datenbanken im Pool an.</span><span class="sxs-lookup"><span data-stu-id="49dcd-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="49dcd-117">Beispiel 2: Erstellen eines vCore-Pool-</span><span class="sxs-lookup"><span data-stu-id="49dcd-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="49dcd-118">Mit diesem Befehl wird ein Pool mit dem Namen "Poolpool01" auf der Dienstebene "GengeralPurpose" erstellt.</span><span class="sxs-lookup"><span data-stu-id="49dcd-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="49dcd-119">Der Server mit dem Namen "server01", der einer Azure-Ressourcengruppe namens "ResourceGroup01" zugewiesen ist, hostet den Pool "Pool".</span><span class="sxs-lookup"><span data-stu-id="49dcd-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="49dcd-120">Der Befehl gibt die vCore-Eigenschaftswerte für den Pool und die Datenbanken im Pool an.</span><span class="sxs-lookup"><span data-stu-id="49dcd-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="49dcd-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="49dcd-121">Example 3</span></span>

<span data-ttu-id="49dcd-122">Erstellt einen Datenbankpool für eine Datenbank SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="49dcd-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="49dcd-123">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="49dcd-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="49dcd-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49dcd-124">PARAMETERS</span></span>

### <span data-ttu-id="49dcd-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49dcd-125">-AsJob</span></span>
<span data-ttu-id="49dcd-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="49dcd-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49dcd-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="49dcd-127">-ComputeGeneration</span></span>
<span data-ttu-id="49dcd-128">Die zuzuordnende Rechengenerierung.</span><span class="sxs-lookup"><span data-stu-id="49dcd-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="49dcd-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="49dcd-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="49dcd-130">Gibt die maximale Anzahl von DTUs (Database Throughput Units) an, die jede einzelne Datenbank im Pool nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="49dcd-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="49dcd-131">Die Standardwerte für die verschiedenen Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="49dcd-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="49dcd-132">Standard.</span><span class="sxs-lookup"><span data-stu-id="49dcd-132">Basic.</span></span> <span data-ttu-id="49dcd-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="49dcd-133">5 DTUs</span></span>
- <span data-ttu-id="49dcd-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="49dcd-134">Standard.</span></span> <span data-ttu-id="49dcd-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="49dcd-135">100 DTUs</span></span>
- <span data-ttu-id="49dcd-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="49dcd-136">Premium.</span></span> <span data-ttu-id="49dcd-137">125 DTUs Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Den speziellen Größenpool in [In-Pool-Pools.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="49dcd-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="49dcd-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="49dcd-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="49dcd-139">Gibt die Mindestanzahl von DTUs an, die der Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="49dcd-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="49dcd-140">Der Standardwert ist null (0).</span><span class="sxs-lookup"><span data-stu-id="49dcd-140">The default value is zero (0).</span></span>
<span data-ttu-id="49dcd-141">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="49dcd-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="49dcd-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="49dcd-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="49dcd-143">Die maximale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verbrauchen kann.</span><span class="sxs-lookup"><span data-stu-id="49dcd-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="49dcd-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="49dcd-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="49dcd-145">Die minimale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verbrauchen kann.</span><span class="sxs-lookup"><span data-stu-id="49dcd-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="49dcd-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49dcd-146">-DefaultProfile</span></span>
<span data-ttu-id="49dcd-147">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="49dcd-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49dcd-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="49dcd-148">-Dtu</span></span>
<span data-ttu-id="49dcd-149">Gibt die Gesamtzahl der freigegebenen DTUs für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="49dcd-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="49dcd-150">Die Standardwerte für die verschiedenen Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="49dcd-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="49dcd-151">Standard.</span><span class="sxs-lookup"><span data-stu-id="49dcd-151">Basic.</span></span>
<span data-ttu-id="49dcd-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="49dcd-152">100 DTUs</span></span>
- <span data-ttu-id="49dcd-153">Standard.</span><span class="sxs-lookup"><span data-stu-id="49dcd-153">Standard.</span></span>
<span data-ttu-id="49dcd-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="49dcd-154">100 DTUs</span></span>
- <span data-ttu-id="49dcd-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="49dcd-155">Premium.</span></span>
<span data-ttu-id="49dcd-156">125 DTUs Details zu gültigen Werten finden Sie in der Tabelle für den jeweiligen Größenpool in [Pool-Pools.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="49dcd-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="49dcd-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="49dcd-157">-Edition</span></span>
<span data-ttu-id="49dcd-158">Gibt die Edition der Azure SQL-Datenbank an, die für den Pool des Poolpools verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49dcd-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="49dcd-159">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="49dcd-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49dcd-160">Keine</span><span class="sxs-lookup"><span data-stu-id="49dcd-160">None</span></span>
- <span data-ttu-id="49dcd-161">Standard</span><span class="sxs-lookup"><span data-stu-id="49dcd-161">Basic</span></span>
- <span data-ttu-id="49dcd-162">Standard</span><span class="sxs-lookup"><span data-stu-id="49dcd-162">Standard</span></span>
- <span data-ttu-id="49dcd-163">Premium</span><span class="sxs-lookup"><span data-stu-id="49dcd-163">Premium</span></span>
- <span data-ttu-id="49dcd-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="49dcd-164">DataWarehouse</span></span>
- <span data-ttu-id="49dcd-165">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="49dcd-165">Free</span></span>
- <span data-ttu-id="49dcd-166">Strecken</span><span class="sxs-lookup"><span data-stu-id="49dcd-166">Stretch</span></span>
- <span data-ttu-id="49dcd-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="49dcd-167">GeneralPurpose</span></span>
- <span data-ttu-id="49dcd-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="49dcd-168">BusinessCritical</span></span>

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

### <span data-ttu-id="49dcd-169">-PoolName</span><span class="sxs-lookup"><span data-stu-id="49dcd-169">-ElasticPoolName</span></span>
<span data-ttu-id="49dcd-170">Gibt den Namen des Poolpools an, der von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="49dcd-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="49dcd-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="49dcd-171">-LicenseType</span></span>
<span data-ttu-id="49dcd-172">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="49dcd-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="49dcd-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49dcd-173">-ResourceGroupName</span></span>
<span data-ttu-id="49dcd-174">Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet den Pool "Pool" zugibt.</span><span class="sxs-lookup"><span data-stu-id="49dcd-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="49dcd-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49dcd-175">-ServerName</span></span>
<span data-ttu-id="49dcd-176">Gibt den Namen des Servers an, auf dem sich der Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="49dcd-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="49dcd-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="49dcd-177">-StorageMB</span></span>
<span data-ttu-id="49dcd-178">Gibt die Speichergrenze in Megabyte für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="49dcd-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="49dcd-179">Wenn Sie diesen Parameter nicht angeben, berechnet dieses Cmdlet einen Wert, der vom Wert des Parameters *"Dtu"* abhängt.</span><span class="sxs-lookup"><span data-stu-id="49dcd-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="49dcd-180">Mögliche [Werte finden Sie unter eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) und Speichergrenzwerte.</span><span class="sxs-lookup"><span data-stu-id="49dcd-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="49dcd-181">-Tags</span><span class="sxs-lookup"><span data-stu-id="49dcd-181">-Tags</span></span>
<span data-ttu-id="49dcd-182">Gibt ein Wörterbuch von Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet dem Pool "Pool" zugibt.</span><span class="sxs-lookup"><span data-stu-id="49dcd-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="49dcd-183">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="49dcd-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="49dcd-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="49dcd-184">-VCore</span></span>
<span data-ttu-id="49dcd-185">Die Gesamtzahl der gemeinsam genutzten Vcores für den Sql Azure-Pool".</span><span class="sxs-lookup"><span data-stu-id="49dcd-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="49dcd-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="49dcd-186">-ZoneRedundant</span></span>
<span data-ttu-id="49dcd-187">Die Zonenredundanz, die dem Azure Sql-Pool (Pool für Sql-Pool) zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="49dcd-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="49dcd-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49dcd-188">-Confirm</span></span>
<span data-ttu-id="49dcd-189">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49dcd-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49dcd-190">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="49dcd-190">-WhatIf</span></span>
<span data-ttu-id="49dcd-191">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49dcd-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49dcd-192">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49dcd-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49dcd-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49dcd-193">CommonParameters</span></span>
<span data-ttu-id="49dcd-194">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49dcd-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49dcd-195">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49dcd-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49dcd-196">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49dcd-196">INPUTS</span></span>

### <span data-ttu-id="49dcd-197">System.String</span><span class="sxs-lookup"><span data-stu-id="49dcd-197">System.String</span></span>

## <span data-ttu-id="49dcd-198">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49dcd-198">OUTPUTS</span></span>

### <span data-ttu-id="49dcd-199">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="49dcd-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="49dcd-200">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49dcd-200">NOTES</span></span>

## <span data-ttu-id="49dcd-201">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49dcd-201">RELATED LINKS</span></span>

[<span data-ttu-id="49dcd-202">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49dcd-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="49dcd-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="49dcd-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="49dcd-204">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="49dcd-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="49dcd-205">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49dcd-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="49dcd-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49dcd-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="49dcd-207">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="49dcd-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
