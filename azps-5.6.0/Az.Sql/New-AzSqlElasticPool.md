---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927720"
---
# <span data-ttu-id="5e875-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e875-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="5e875-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e875-102">SYNOPSIS</span></span>
<span data-ttu-id="5e875-103">Erstellt einen flexiblen Datenbankpool für eine SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5e875-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="5e875-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e875-104">SYNTAX</span></span>

### <span data-ttu-id="5e875-105">DtuBasedPool (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e875-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e875-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="5e875-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e875-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e875-107">DESCRIPTION</span></span>
<span data-ttu-id="5e875-108">Das **Cmdlet New-AzSqlElasticPool** erstellt einen flexiblen Datenbankpool für eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5e875-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="5e875-109">Mehrere Parameter (*-Dtu, -DatabaseDtuMin und -DatabaseDtuMax*) erfordern, dass der festgelegte Wert aus der Liste der gültigen Werte für diesen Parameter kommt.</span><span class="sxs-lookup"><span data-stu-id="5e875-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="5e875-110">Beispielsweise kann -DatabaseDtuMax für einen Standardmäßigen 100 eDTU-Pool nur auf 10, 20, 50 oder 100 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5e875-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="5e875-111">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren bestimmten Größenpool in [Den Pools für die größe](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="5e875-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="5e875-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e875-112">EXAMPLES</span></span>

### <span data-ttu-id="5e875-113">Beispiel 1: Erstellen eines DTU-Pool für einen Flexiblen Pool</span><span class="sxs-lookup"><span data-stu-id="5e875-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="5e875-114">Mit diesem Befehl wird ein Pool für einen flexiblen Pool in der Standarddienstebene namens "ElasticPool01" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e875-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="5e875-115">Der Server mit dem Namen Server01, der einer Azure-Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist, hostet den Pool für den Pool mit den Bändern.</span><span class="sxs-lookup"><span data-stu-id="5e875-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="5e875-116">Der Befehl gibt die Werte der DTU-Eigenschaft für den Pool und die Datenbanken im Pool an.</span><span class="sxs-lookup"><span data-stu-id="5e875-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="5e875-117">Beispiel 2: Erstellen eines vCore-Pool für einen flexiblen Pool</span><span class="sxs-lookup"><span data-stu-id="5e875-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="5e875-118">Mit diesem Befehl wird in der Dienstebene GengeralPurpose mit dem Namen "ElasticPool01" ein Pool für einen Flexiblen Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e875-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="5e875-119">Der Server mit dem Namen Server01, der einer Azure-Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist, hostet den Pool für den Pool mit den Bändern.</span><span class="sxs-lookup"><span data-stu-id="5e875-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="5e875-120">Der Befehl gibt die vCore-Eigenschaftswerte für den Pool und die Datenbanken im Pool an.</span><span class="sxs-lookup"><span data-stu-id="5e875-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="5e875-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5e875-121">Example 3</span></span>

<span data-ttu-id="5e875-122">Erstellt einen flexiblen Datenbankpool für eine SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5e875-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="5e875-123">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="5e875-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="5e875-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e875-124">PARAMETERS</span></span>

### <span data-ttu-id="5e875-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e875-125">-AsJob</span></span>
<span data-ttu-id="5e875-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5e875-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e875-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5e875-127">-ComputeGeneration</span></span>
<span data-ttu-id="5e875-128">Die zuzuordnende Berechnungsgenerierung.</span><span class="sxs-lookup"><span data-stu-id="5e875-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="5e875-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="5e875-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="5e875-130">Gibt die maximale Anzahl von DTUs (Database Throughput Units) an, die jede einzelne Datenbank im Pool nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="5e875-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="5e875-131">Die Standardwerte für die verschiedenen Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5e875-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="5e875-132">Basic.</span><span class="sxs-lookup"><span data-stu-id="5e875-132">Basic.</span></span> <span data-ttu-id="5e875-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="5e875-133">5 DTUs</span></span>
- <span data-ttu-id="5e875-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="5e875-134">Standard.</span></span> <span data-ttu-id="5e875-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="5e875-135">100 DTUs</span></span>
- <span data-ttu-id="5e875-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="5e875-136">Premium.</span></span> <span data-ttu-id="5e875-137">125 DTUs Details zu den gültigen Werten finden Sie in der Tabelle für Ihren speziellen Größenpool in [Pools für die größe von Pools.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="5e875-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="5e875-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="5e875-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="5e875-139">Gibt die Mindestanzahl von DTUs an, die der Pool für den Flexiblen Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="5e875-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="5e875-140">Der Standardwert ist Null (0).</span><span class="sxs-lookup"><span data-stu-id="5e875-140">The default value is zero (0).</span></span>
<span data-ttu-id="5e875-141">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren bestimmten Größenpool in [Den Pools für die größe](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="5e875-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="5e875-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="5e875-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="5e875-143">Die maximale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5e875-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5e875-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="5e875-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="5e875-145">Die mindeste VCore-Zahl, die jede SqlAzure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5e875-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5e875-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e875-146">-DefaultProfile</span></span>
<span data-ttu-id="5e875-147">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5e875-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e875-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="5e875-148">-Dtu</span></span>
<span data-ttu-id="5e875-149">Gibt die Gesamtanzahl der gemeinsam genutzten DTUs für den Pool für den Flexiblen Pool an.</span><span class="sxs-lookup"><span data-stu-id="5e875-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="5e875-150">Die Standardwerte für die verschiedenen Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5e875-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="5e875-151">Basic.</span><span class="sxs-lookup"><span data-stu-id="5e875-151">Basic.</span></span>
<span data-ttu-id="5e875-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="5e875-152">100 DTUs</span></span>
- <span data-ttu-id="5e875-153">Standard.</span><span class="sxs-lookup"><span data-stu-id="5e875-153">Standard.</span></span>
<span data-ttu-id="5e875-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="5e875-154">100 DTUs</span></span>
- <span data-ttu-id="5e875-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="5e875-155">Premium.</span></span>
<span data-ttu-id="5e875-156">125 DTUs Details zu den gültigen Werten finden Sie in der Tabelle für Ihren speziellen Größenpool in [den Pools für die flexible Größe.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="5e875-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="5e875-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="5e875-157">-Edition</span></span>
<span data-ttu-id="5e875-158">Gibt die Edition der Azure-SQL-Datenbank an, die für den Pool für den Flexiblen Pool verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e875-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="5e875-159">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5e875-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e875-160">Keine</span><span class="sxs-lookup"><span data-stu-id="5e875-160">None</span></span>
- <span data-ttu-id="5e875-161">Basic</span><span class="sxs-lookup"><span data-stu-id="5e875-161">Basic</span></span>
- <span data-ttu-id="5e875-162">Standard</span><span class="sxs-lookup"><span data-stu-id="5e875-162">Standard</span></span>
- <span data-ttu-id="5e875-163">Premium</span><span class="sxs-lookup"><span data-stu-id="5e875-163">Premium</span></span>
- <span data-ttu-id="5e875-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="5e875-164">DataWarehouse</span></span>
- <span data-ttu-id="5e875-165">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="5e875-165">Free</span></span>
- <span data-ttu-id="5e875-166">Stretch</span><span class="sxs-lookup"><span data-stu-id="5e875-166">Stretch</span></span>
- <span data-ttu-id="5e875-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="5e875-167">GeneralPurpose</span></span>
- <span data-ttu-id="5e875-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="5e875-168">BusinessCritical</span></span>

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

### <span data-ttu-id="5e875-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5e875-169">-ElasticPoolName</span></span>
<span data-ttu-id="5e875-170">Gibt den Namen des von diesem Cmdlet erstellten Pool für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="5e875-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5e875-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5e875-171">-LicenseType</span></span>
<span data-ttu-id="5e875-172">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5e875-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="5e875-173">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5e875-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="5e875-174">Die Wartungskonfigurations-ID für den SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="5e875-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="5e875-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e875-175">-ResourceGroupName</span></span>
<span data-ttu-id="5e875-176">Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet den Pool für den Flexiblen zuzuordnen hat.</span><span class="sxs-lookup"><span data-stu-id="5e875-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="5e875-177">-Servername</span><span class="sxs-lookup"><span data-stu-id="5e875-177">-ServerName</span></span>
<span data-ttu-id="5e875-178">Gibt den Namen des Servers an, auf dem sich der Pool für die flexiblen Bänder befindet.</span><span class="sxs-lookup"><span data-stu-id="5e875-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="5e875-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="5e875-179">-StorageMB</span></span>
<span data-ttu-id="5e875-180">Gibt den Speichergrenzwert (in Mb) für den Pool für den Flexiblen Pool an.</span><span class="sxs-lookup"><span data-stu-id="5e875-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="5e875-181">Wenn Sie diesen Parameter nicht angeben, berechnet dieses Cmdlet einen Wert, der vom Wert des *Parameters Dtu* abhängt.</span><span class="sxs-lookup"><span data-stu-id="5e875-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="5e875-182">Mögliche Werte finden Sie unter [eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) und Speichergrenzwerte.</span><span class="sxs-lookup"><span data-stu-id="5e875-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="5e875-183">-Tags</span><span class="sxs-lookup"><span data-stu-id="5e875-183">-Tags</span></span>
<span data-ttu-id="5e875-184">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet mit dem Pool für den Flexiblen Pool verknüpft.</span><span class="sxs-lookup"><span data-stu-id="5e875-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="5e875-185">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5e875-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5e875-186">-VCore</span><span class="sxs-lookup"><span data-stu-id="5e875-186">-VCore</span></span>
<span data-ttu-id="5e875-187">Die Gesamtanzahl der freigegebenen Vcores für den Sql Azure -Pool für flexible Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5e875-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="5e875-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5e875-188">-ZoneRedundant</span></span>
<span data-ttu-id="5e875-189">Die Zonenredundanz, die dem Azure Sql -Pool "Flexibler Pool" zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="5e875-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="5e875-190">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e875-190">-Confirm</span></span>
<span data-ttu-id="5e875-191">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e875-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e875-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e875-192">-WhatIf</span></span>
<span data-ttu-id="5e875-193">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e875-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e875-194">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e875-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e875-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e875-195">CommonParameters</span></span>
<span data-ttu-id="5e875-196">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e875-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e875-197">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e875-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e875-198">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e875-198">INPUTS</span></span>

### <span data-ttu-id="5e875-199">System.String</span><span class="sxs-lookup"><span data-stu-id="5e875-199">System.String</span></span>

## <span data-ttu-id="5e875-200">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e875-200">OUTPUTS</span></span>

### <span data-ttu-id="5e875-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="5e875-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5e875-202">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e875-202">NOTES</span></span>

## <span data-ttu-id="5e875-203">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e875-203">RELATED LINKS</span></span>

[<span data-ttu-id="5e875-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e875-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="5e875-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5e875-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="5e875-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5e875-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="5e875-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e875-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="5e875-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e875-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="5e875-209">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="5e875-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
