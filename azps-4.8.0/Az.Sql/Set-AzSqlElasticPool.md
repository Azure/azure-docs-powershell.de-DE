---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174082"
---
# <span data-ttu-id="5a46e-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5a46e-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="5a46e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a46e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a46e-103">Ändert die Eigenschaften eines elastischen Daten Bank Pools in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5a46e-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="5a46e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a46e-104">SYNTAX</span></span>

### <span data-ttu-id="5a46e-105">DtuBasedPool (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a46e-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a46e-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="5a46e-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a46e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a46e-107">DESCRIPTION</span></span>
<span data-ttu-id="5a46e-108">Das Cmdlet " **Set-AzSqlElasticPool** " legt Eigenschaften für einen elastischen Pool in Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="5a46e-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="5a46e-109">Mit diesem Cmdlet können die eDTUs pro Pool ( *DTU* ), die maximale Speichergröße pro Pool ( *StorageMB* ), maximale eDTUs pro Datenbank ( *DatabaseDtuMax* ) und minimale eDTUs pro Datenbank ( *DatabaseDtuMin* ) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a46e-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="5a46e-110">Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5a46e-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="5a46e-111">Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5a46e-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="5a46e-112">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="5a46e-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="5a46e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a46e-113">EXAMPLES</span></span>

### <span data-ttu-id="5a46e-114">Beispiel 1: Ändern der Eigenschaften eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="5a46e-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="5a46e-115">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="5a46e-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="5a46e-116">Mit dem Befehl wird die Anzahl der DTUs für den elastischen Pool auf 1000 und die Mindest-und höchst DTUs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a46e-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="5a46e-117">Beispiel 2: Ändern der maximalen Speichergröße eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="5a46e-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="5a46e-118">Dieser Befehl ändert Eigenschaften für einen elastischen Pool mit dem Namen elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="5a46e-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="5a46e-119">Der Befehl legt den Max-Speicher für einen elastischen Pool auf 2 TB fest.</span><span class="sxs-lookup"><span data-stu-id="5a46e-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="5a46e-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5a46e-120">Example 3</span></span>

<span data-ttu-id="5a46e-121">Ändert die Eigenschaften eines elastischen Daten Bank Pools in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5a46e-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="5a46e-122">automatisch</span><span class="sxs-lookup"><span data-stu-id="5a46e-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="5a46e-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a46e-123">PARAMETERS</span></span>

### <span data-ttu-id="5a46e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a46e-124">-AsJob</span></span>
<span data-ttu-id="5a46e-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5a46e-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a46e-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5a46e-126">-ComputeGeneration</span></span>
<span data-ttu-id="5a46e-127">Die COMPUTE-Generierung, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a46e-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="5a46e-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="5a46e-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="5a46e-129">Gibt die maximale Anzahl von DTUs an, die eine einzelne Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5a46e-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="5a46e-130">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="5a46e-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="5a46e-131">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5a46e-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="5a46e-132">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="5a46e-132">Basic.</span></span>  <span data-ttu-id="5a46e-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="5a46e-133">5 DTUs</span></span>
- <span data-ttu-id="5a46e-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="5a46e-134">Standard.</span></span> <span data-ttu-id="5a46e-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="5a46e-135">100 DTUs</span></span>
- <span data-ttu-id="5a46e-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="5a46e-136">Premium.</span></span> <span data-ttu-id="5a46e-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="5a46e-137">125 DTUs</span></span>

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

### <span data-ttu-id="5a46e-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="5a46e-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="5a46e-139">Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="5a46e-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="5a46e-140">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="5a46e-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="5a46e-141">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5a46e-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="5a46e-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="5a46e-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="5a46e-143">Die maximale Vcore-Nummer, die eine sqlazure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5a46e-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5a46e-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="5a46e-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="5a46e-145">Die minimale Vcore-Nummer, die eine beliebige sqlazure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5a46e-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5a46e-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a46e-146">-DefaultProfile</span></span>
<span data-ttu-id="5a46e-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5a46e-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a46e-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="5a46e-148">-Dtu</span></span>
<span data-ttu-id="5a46e-149">Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="5a46e-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="5a46e-150">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="5a46e-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="5a46e-151">Die Standardwerte für verschiedene Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5a46e-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="5a46e-152">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="5a46e-152">Basic.</span></span> <span data-ttu-id="5a46e-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="5a46e-153">100 DTUs</span></span>
- <span data-ttu-id="5a46e-154">Standard.</span><span class="sxs-lookup"><span data-stu-id="5a46e-154">Standard.</span></span> <span data-ttu-id="5a46e-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="5a46e-155">100 DTUs</span></span>
- <span data-ttu-id="5a46e-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="5a46e-156">Premium.</span></span> <span data-ttu-id="5a46e-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="5a46e-157">125 DTUs</span></span>

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

### <span data-ttu-id="5a46e-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="5a46e-158">-Edition</span></span>
<span data-ttu-id="5a46e-159">Gibt die Edition der Azure SQL-Datenbank für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="5a46e-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="5a46e-160">Sie können die Edition nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="5a46e-160">You cannot change the edition.</span></span> <span data-ttu-id="5a46e-161">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5a46e-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a46e-162">Keine</span><span class="sxs-lookup"><span data-stu-id="5a46e-162">None</span></span>
- <span data-ttu-id="5a46e-163">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="5a46e-163">Basic</span></span>
- <span data-ttu-id="5a46e-164">Standard</span><span class="sxs-lookup"><span data-stu-id="5a46e-164">Standard</span></span>
- <span data-ttu-id="5a46e-165">Premium</span><span class="sxs-lookup"><span data-stu-id="5a46e-165">Premium</span></span>
- <span data-ttu-id="5a46e-166">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="5a46e-166">DataWarehouse</span></span>
- <span data-ttu-id="5a46e-167">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="5a46e-167">Free</span></span>
- <span data-ttu-id="5a46e-168">Stretch</span><span class="sxs-lookup"><span data-stu-id="5a46e-168">Stretch</span></span>
- <span data-ttu-id="5a46e-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="5a46e-169">GeneralPurpose</span></span>
- <span data-ttu-id="5a46e-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="5a46e-170">BusinessCritical</span></span>

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

### <span data-ttu-id="5a46e-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5a46e-171">-ElasticPoolName</span></span>
<span data-ttu-id="5a46e-172">Gibt den Namen des elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="5a46e-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="5a46e-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5a46e-173">-LicenseType</span></span>
<span data-ttu-id="5a46e-174">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5a46e-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="5a46e-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a46e-175">-ResourceGroupName</span></span>
<span data-ttu-id="5a46e-176">Gibt den Namen der Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5a46e-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="5a46e-177">-Servername</span><span class="sxs-lookup"><span data-stu-id="5a46e-177">-ServerName</span></span>
<span data-ttu-id="5a46e-178">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="5a46e-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="5a46e-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="5a46e-179">-StorageMB</span></span>
<span data-ttu-id="5a46e-180">Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="5a46e-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="5a46e-181">Weitere Informationen finden Sie im New-AzSqlElasticPool-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a46e-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="5a46e-182">-Tags</span><span class="sxs-lookup"><span data-stu-id="5a46e-182">-Tags</span></span>
<span data-ttu-id="5a46e-183">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an, die dieses Cmdlet dem elastischen Pool in Form einer Hashtabelle zuordnet.</span><span class="sxs-lookup"><span data-stu-id="5a46e-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="5a46e-184">Zum Beispiel: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="5a46e-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="5a46e-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="5a46e-185">-VCore</span></span>
<span data-ttu-id="5a46e-186">Die Gesamtanzahl der freigegebenen Vcore für den SQL Azure Elastic-Pool.</span><span class="sxs-lookup"><span data-stu-id="5a46e-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="5a46e-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5a46e-187">-ZoneRedundant</span></span>
<span data-ttu-id="5a46e-188">Die Zonen Redundanz, die dem Azure SQL-elastischen Pool zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="5a46e-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="5a46e-189">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a46e-189">-Confirm</span></span>
<span data-ttu-id="5a46e-190">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a46e-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a46e-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a46e-191">-WhatIf</span></span>
<span data-ttu-id="5a46e-192">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a46e-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a46e-193">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a46e-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a46e-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a46e-194">CommonParameters</span></span>
<span data-ttu-id="5a46e-195">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a46e-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a46e-196">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a46e-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a46e-197">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a46e-197">INPUTS</span></span>

### <span data-ttu-id="5a46e-198">System. String</span><span class="sxs-lookup"><span data-stu-id="5a46e-198">System.String</span></span>

## <span data-ttu-id="5a46e-199">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a46e-199">OUTPUTS</span></span>

### <span data-ttu-id="5a46e-200">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="5a46e-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5a46e-201">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a46e-201">NOTES</span></span>

## <span data-ttu-id="5a46e-202">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a46e-202">RELATED LINKS</span></span>

[<span data-ttu-id="5a46e-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5a46e-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="5a46e-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5a46e-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="5a46e-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5a46e-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="5a46e-206">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5a46e-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="5a46e-207">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5a46e-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
