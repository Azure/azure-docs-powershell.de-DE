---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 564bd475b8574f30f8d00cc1a374bc11b4a93ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924416"
---
# <span data-ttu-id="512d5-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="512d5-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="512d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="512d5-102">SYNOPSIS</span></span>
<span data-ttu-id="512d5-103">Ändert die Eigenschaften eines flexiblen Datenbankpools in Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="512d5-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="512d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="512d5-104">SYNTAX</span></span>

### <span data-ttu-id="512d5-105">DtuBasedPool (Standard)</span><span class="sxs-lookup"><span data-stu-id="512d5-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="512d5-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="512d5-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="512d5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="512d5-107">DESCRIPTION</span></span>
<span data-ttu-id="512d5-108">Das **Set-AzSqlElasticPool-Cmdlet** legt Eigenschaften für einen Pool für einen flexiblen Pool in Azure SQL Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="512d5-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="512d5-109">Dieses Cmdlet kann die eDTUs pro Pool (*Dtu*), maximale Speichergröße pro Pool (*StorageMB*), maximale eDTUs pro Datenbank (*DatabaseDtuMax*) und minimale eDTUs pro Datenbank (*DatabaseDtuMin*) ändern.</span><span class="sxs-lookup"><span data-stu-id="512d5-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="512d5-110">Mehrere Parameter (*-Dtu, -DatabaseDtuMin und -DatabaseDtuMax*) erfordern, dass der festgelegte Wert aus der Liste der gültigen Werte für diesen Parameter kommt.</span><span class="sxs-lookup"><span data-stu-id="512d5-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="512d5-111">Beispielsweise kann -DatabaseDtuMax für einen Standardmäßigen 100 eDTU-Pool nur auf 10, 20, 50 oder 100 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="512d5-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="512d5-112">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren bestimmten Größenpool in [Den Pools für die größe](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="512d5-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="512d5-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="512d5-113">EXAMPLES</span></span>

### <span data-ttu-id="512d5-114">Beispiel 1: Ändern von Eigenschaften für einen Pool mit einem Bänder</span><span class="sxs-lookup"><span data-stu-id="512d5-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="512d5-115">Mit diesem Befehl werden die Eigenschaften für einen Pool mit dem Namen "elasticpool01" geändert.</span><span class="sxs-lookup"><span data-stu-id="512d5-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="512d5-116">Mit dem Befehl wird die Anzahl der DTUs für den Pool für den Flexiblen Pool auf 1000 und die minimalen und maximalen DTUs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="512d5-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="512d5-117">Beispiel 2: Ändern der maximalen Speichergröße eines Pool für einen flexiblen Speicher</span><span class="sxs-lookup"><span data-stu-id="512d5-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="512d5-118">Mit diesem Befehl werden die Eigenschaften für einen Pool mit dem Namen "elasticpool01" geändert.</span><span class="sxs-lookup"><span data-stu-id="512d5-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="512d5-119">Mit dem Befehl wird der maximale Speicher für einen Pool für einen Flexiblen Auf 2 TB bestimmt.</span><span class="sxs-lookup"><span data-stu-id="512d5-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="512d5-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="512d5-120">Example 3</span></span>

<span data-ttu-id="512d5-121">Ändert die Eigenschaften eines flexiblen Datenbankpools in Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="512d5-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="512d5-122">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="512d5-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="512d5-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="512d5-123">PARAMETERS</span></span>

### <span data-ttu-id="512d5-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="512d5-124">-AsJob</span></span>
<span data-ttu-id="512d5-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="512d5-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="512d5-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="512d5-126">-ComputeGeneration</span></span>
<span data-ttu-id="512d5-127">Die zuzuordnende Berechnungsgenerierung.</span><span class="sxs-lookup"><span data-stu-id="512d5-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="512d5-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="512d5-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="512d5-129">Gibt die maximale Anzahl von DTUs an, die jede einzelne Datenbank im Pool nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="512d5-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="512d5-130">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren bestimmten Größenpool in [Den Pools für die größe](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="512d5-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="512d5-131">Die Standardwerte für unterschiedliche Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="512d5-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="512d5-132">Basic.</span><span class="sxs-lookup"><span data-stu-id="512d5-132">Basic.</span></span>  <span data-ttu-id="512d5-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="512d5-133">5 DTUs</span></span>
- <span data-ttu-id="512d5-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="512d5-134">Standard.</span></span> <span data-ttu-id="512d5-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="512d5-135">100 DTUs</span></span>
- <span data-ttu-id="512d5-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="512d5-136">Premium.</span></span> <span data-ttu-id="512d5-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="512d5-137">125 DTUs</span></span>

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

### <span data-ttu-id="512d5-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="512d5-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="512d5-139">Gibt die Mindestanzahl von DTUs an, die der Pool für den Flexiblen Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="512d5-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="512d5-140">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren bestimmten Größenpool in [Den Pools für die größe](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="512d5-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="512d5-141">Der Standardwert ist Null (0).</span><span class="sxs-lookup"><span data-stu-id="512d5-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="512d5-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="512d5-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="512d5-143">Die maximale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="512d5-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="512d5-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="512d5-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="512d5-145">Die mindeste VCore-Zahl, die jede SqlAzure-Datenbank im Pool verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="512d5-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="512d5-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512d5-146">-DefaultProfile</span></span>
<span data-ttu-id="512d5-147">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="512d5-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="512d5-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="512d5-148">-Dtu</span></span>
<span data-ttu-id="512d5-149">Gibt die Gesamtanzahl der gemeinsam genutzten DTUs für den Pool für den Flexiblen Pool an.</span><span class="sxs-lookup"><span data-stu-id="512d5-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="512d5-150">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren bestimmten Größenpool in [Den Pools für die größe](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="512d5-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="512d5-151">Die Standardwerte für unterschiedliche Editionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="512d5-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="512d5-152">Basic.</span><span class="sxs-lookup"><span data-stu-id="512d5-152">Basic.</span></span> <span data-ttu-id="512d5-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="512d5-153">100 DTUs</span></span>
- <span data-ttu-id="512d5-154">Standard.</span><span class="sxs-lookup"><span data-stu-id="512d5-154">Standard.</span></span> <span data-ttu-id="512d5-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="512d5-155">100 DTUs</span></span>
- <span data-ttu-id="512d5-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="512d5-156">Premium.</span></span> <span data-ttu-id="512d5-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="512d5-157">125 DTUs</span></span>

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

### <span data-ttu-id="512d5-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="512d5-158">-Edition</span></span>
<span data-ttu-id="512d5-159">Gibt die Edition der Azure SQL-Datenbank für den Pool für den Pool an.</span><span class="sxs-lookup"><span data-stu-id="512d5-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="512d5-160">Sie können die Edition nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="512d5-160">You cannot change the edition.</span></span> <span data-ttu-id="512d5-161">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="512d5-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="512d5-162">Keine</span><span class="sxs-lookup"><span data-stu-id="512d5-162">None</span></span>
- <span data-ttu-id="512d5-163">Basic</span><span class="sxs-lookup"><span data-stu-id="512d5-163">Basic</span></span>
- <span data-ttu-id="512d5-164">Standard</span><span class="sxs-lookup"><span data-stu-id="512d5-164">Standard</span></span>
- <span data-ttu-id="512d5-165">Premium</span><span class="sxs-lookup"><span data-stu-id="512d5-165">Premium</span></span>
- <span data-ttu-id="512d5-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="512d5-166">DataWarehouse</span></span>
- <span data-ttu-id="512d5-167">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="512d5-167">Free</span></span>
- <span data-ttu-id="512d5-168">Stretch</span><span class="sxs-lookup"><span data-stu-id="512d5-168">Stretch</span></span>
- <span data-ttu-id="512d5-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="512d5-169">GeneralPurpose</span></span>
- <span data-ttu-id="512d5-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="512d5-170">BusinessCritical</span></span>

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

### <span data-ttu-id="512d5-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="512d5-171">-ElasticPoolName</span></span>
<span data-ttu-id="512d5-172">Gibt den Namen des Pool für den Flexiblen Pool an.</span><span class="sxs-lookup"><span data-stu-id="512d5-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="512d5-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="512d5-173">-LicenseType</span></span>
<span data-ttu-id="512d5-174">Der Lizenztyp für die Azure Sql-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="512d5-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="512d5-175">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="512d5-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="512d5-176">Die Wartungskonfigurations-ID für den SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="512d5-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="512d5-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512d5-177">-ResourceGroupName</span></span>
<span data-ttu-id="512d5-178">Gibt den Namen der Ressourcengruppe an, der der Pool für den Pool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="512d5-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="512d5-179">-Servername</span><span class="sxs-lookup"><span data-stu-id="512d5-179">-ServerName</span></span>
<span data-ttu-id="512d5-180">Gibt den Namen des Servers an, auf dem sich der Pool für die flexiblen Bänder befindet.</span><span class="sxs-lookup"><span data-stu-id="512d5-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="512d5-181">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="512d5-181">-StorageMB</span></span>
<span data-ttu-id="512d5-182">Gibt den Speichergrenzwert (in Mb) für den Pool für den Flexiblen Pool an.</span><span class="sxs-lookup"><span data-stu-id="512d5-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="512d5-183">Weitere Informationen finden Sie im New-AzSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="512d5-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="512d5-184">-Tags</span><span class="sxs-lookup"><span data-stu-id="512d5-184">-Tags</span></span>
<span data-ttu-id="512d5-185">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an, das dieses Cmdlet dem #A0 in Form einer Hashtabelle zurät.</span><span class="sxs-lookup"><span data-stu-id="512d5-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="512d5-186">Zum Beispiel: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="512d5-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="512d5-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="512d5-187">-VCore</span></span>
<span data-ttu-id="512d5-188">Die Gesamtanzahl der freigegebenen Vcore für den Sql Azure-Pool für flexible Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="512d5-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="512d5-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="512d5-189">-ZoneRedundant</span></span>
<span data-ttu-id="512d5-190">Die Zonenredundanz, die dem Azure Sql -Pool "Flexibler Pool" zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="512d5-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="512d5-191">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="512d5-191">-Confirm</span></span>
<span data-ttu-id="512d5-192">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="512d5-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="512d5-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512d5-193">-WhatIf</span></span>
<span data-ttu-id="512d5-194">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="512d5-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512d5-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="512d5-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="512d5-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512d5-196">CommonParameters</span></span>
<span data-ttu-id="512d5-197">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512d5-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512d5-198">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="512d5-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512d5-199">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="512d5-199">INPUTS</span></span>

### <span data-ttu-id="512d5-200">System.String</span><span class="sxs-lookup"><span data-stu-id="512d5-200">System.String</span></span>

## <span data-ttu-id="512d5-201">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="512d5-201">OUTPUTS</span></span>

### <span data-ttu-id="512d5-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="512d5-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="512d5-203">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="512d5-203">NOTES</span></span>

## <span data-ttu-id="512d5-204">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="512d5-204">RELATED LINKS</span></span>

[<span data-ttu-id="512d5-205">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="512d5-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="512d5-206">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="512d5-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="512d5-207">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="512d5-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="512d5-208">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="512d5-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="512d5-209">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="512d5-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
