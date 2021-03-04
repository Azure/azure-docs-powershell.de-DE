---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943930"
---
# <span data-ttu-id="c2eac-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2eac-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="c2eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2eac-102">SYNOPSIS</span></span>
<span data-ttu-id="c2eac-103">Ändert einen Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="c2eac-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="c2eac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2eac-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2eac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2eac-105">DESCRIPTION</span></span>
<span data-ttu-id="c2eac-106">Das **Cmdlet Set-AzRedisCache** ändert einen Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="c2eac-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="c2eac-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2eac-107">EXAMPLES</span></span>

### <span data-ttu-id="c2eac-108">Beispiel 1: Ändern eines Redis-Caches</span><span class="sxs-lookup"><span data-stu-id="c2eac-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="c2eac-109">Mit diesem Befehl wird die maxmemory-richtlinie für den Redis-Cache mit dem Namen MyCache aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c2eac-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="c2eac-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c2eac-110">PARAMETERS</span></span>

### <span data-ttu-id="c2eac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2eac-111">-DefaultProfile</span></span>
<span data-ttu-id="c2eac-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2eac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2eac-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="c2eac-113">-EnableNonSslPort</span></span>
<span data-ttu-id="c2eac-114">Gibt an, ob der Nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c2eac-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="c2eac-115">Der Standardwert ist $False (der Nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="c2eac-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c2eac-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="c2eac-117">Geben Sie die TLS-Version an, die von Clients zum Herstellen einer Verbindung mit dem Cache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c2eac-117">Specify the TLS version required by clients to connect to cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c2eac-118">-Name</span></span>
<span data-ttu-id="c2eac-119">Gibt den Namen des zu aktualisierenden Redis-Caches an.</span><span class="sxs-lookup"><span data-stu-id="c2eac-119">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2eac-120">-RedisConfiguration</span></span>
<span data-ttu-id="c2eac-121">Gibt Die Konfigurationseinstellungen von Redis an.</span><span class="sxs-lookup"><span data-stu-id="c2eac-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="c2eac-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="c2eac-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2eac-123">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="c2eac-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="c2eac-124">Gibt an, dass die Datenpersistenz von Redis aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c2eac-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="c2eac-125">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="c2eac-125">Premium tier only.</span></span>
- <span data-ttu-id="c2eac-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="c2eac-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="c2eac-127">Gibt die Verbindungszeichenfolge zum Speicherkonto für die Datenpersistenz von Redis an.</span><span class="sxs-lookup"><span data-stu-id="c2eac-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="c2eac-128">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="c2eac-128">Premium tier only.</span></span>
- <span data-ttu-id="c2eac-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="c2eac-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="c2eac-130">Gibt die Sicherungshäufigkeit für die Datenpersistenz von Redis an.</span><span class="sxs-lookup"><span data-stu-id="c2eac-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="c2eac-131">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="c2eac-131">Premium tier only.</span></span> 
- <span data-ttu-id="c2eac-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="c2eac-132">maxmemory-reserved.</span></span>
<span data-ttu-id="c2eac-133">Konfiguriert den Speicher, der für Prozesse ohne Cache reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="c2eac-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="c2eac-134">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c2eac-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="c2eac-135">maxmemory-policy.</span></span>
<span data-ttu-id="c2eac-136">Konfiguriert die Räumungsrichtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="c2eac-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="c2eac-137">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-137">All pricing tiers.</span></span> 
- <span data-ttu-id="c2eac-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="c2eac-138">notify-keyspace-events.</span></span>
<span data-ttu-id="c2eac-139">Konfiguriert Keyspacebenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="c2eac-140">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="c2eac-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="c2eac-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="c2eac-142">Konfiguriert die Speicheroptimierung für kleine Aggregatdatentypen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c2eac-143">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c2eac-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="c2eac-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="c2eac-145">Konfiguriert die Speicheroptimierung für kleine Aggregatdatentypen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c2eac-146">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c2eac-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="c2eac-147">set-max-intset-entries.</span></span>
<span data-ttu-id="c2eac-148">Konfiguriert die Speicheroptimierung für kleine Aggregatdatentypen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c2eac-149">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c2eac-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="c2eac-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="c2eac-151">Konfiguriert die Speicheroptimierung für kleine Aggregatdatentypen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c2eac-152">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c2eac-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="c2eac-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="c2eac-154">Konfiguriert die Speicheroptimierung für kleine Aggregatdatentypen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c2eac-155">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c2eac-156">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="c2eac-156">databases.</span></span>
<span data-ttu-id="c2eac-157">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="c2eac-157">Configures the number of databases.</span></span>
<span data-ttu-id="c2eac-158">Diese Eigenschaft kann nur bei der Cacheerstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c2eac-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="c2eac-159">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="c2eac-160">Weitere Informationen finden Sie unter Verwalten von Azure Redis Cache mit Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="c2eac-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2eac-161">-ResourceGroupName</span></span>
<span data-ttu-id="c2eac-162">Gibt den Namen der Ressourcengruppe an, die den Redis-Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="c2eac-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="c2eac-163">-ShardCount</span></span>
<span data-ttu-id="c2eac-164">Gibt die Anzahl der Shards an, die in einem Premium-Clustercache erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-165">-Size</span><span class="sxs-lookup"><span data-stu-id="c2eac-165">-Size</span></span>
<span data-ttu-id="c2eac-166">Gibt die Größe des Redis Cache an.</span><span class="sxs-lookup"><span data-stu-id="c2eac-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="c2eac-167">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c2eac-167">Valid values are:</span></span> 
- <span data-ttu-id="c2eac-168">P1</span><span class="sxs-lookup"><span data-stu-id="c2eac-168">P1</span></span>
- <span data-ttu-id="c2eac-169">P2</span><span class="sxs-lookup"><span data-stu-id="c2eac-169">P2</span></span>
- <span data-ttu-id="c2eac-170">P3</span><span class="sxs-lookup"><span data-stu-id="c2eac-170">P3</span></span>
- <span data-ttu-id="c2eac-171">P4</span><span class="sxs-lookup"><span data-stu-id="c2eac-171">P4</span></span>
- <span data-ttu-id="c2eac-172">P5</span><span class="sxs-lookup"><span data-stu-id="c2eac-172">P5</span></span>
- <span data-ttu-id="c2eac-173">C0</span><span class="sxs-lookup"><span data-stu-id="c2eac-173">C0</span></span>
- <span data-ttu-id="c2eac-174">C1</span><span class="sxs-lookup"><span data-stu-id="c2eac-174">C1</span></span>
- <span data-ttu-id="c2eac-175">C2</span><span class="sxs-lookup"><span data-stu-id="c2eac-175">C2</span></span>
- <span data-ttu-id="c2eac-176">C3</span><span class="sxs-lookup"><span data-stu-id="c2eac-176">C3</span></span>
- <span data-ttu-id="c2eac-177">C4</span><span class="sxs-lookup"><span data-stu-id="c2eac-177">C4</span></span>
- <span data-ttu-id="c2eac-178">C5</span><span class="sxs-lookup"><span data-stu-id="c2eac-178">C5</span></span>
- <span data-ttu-id="c2eac-179">C6</span><span class="sxs-lookup"><span data-stu-id="c2eac-179">C6</span></span>
- <span data-ttu-id="c2eac-180">250 MB</span><span class="sxs-lookup"><span data-stu-id="c2eac-180">250MB</span></span>
- <span data-ttu-id="c2eac-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="c2eac-181">1GB</span></span>
- <span data-ttu-id="c2eac-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="c2eac-182">2.5GB</span></span>
- <span data-ttu-id="c2eac-183">6 GB</span><span class="sxs-lookup"><span data-stu-id="c2eac-183">6GB</span></span>
- <span data-ttu-id="c2eac-184">13 GB</span><span class="sxs-lookup"><span data-stu-id="c2eac-184">13GB</span></span>
- <span data-ttu-id="c2eac-185">26 GB</span><span class="sxs-lookup"><span data-stu-id="c2eac-185">26GB</span></span>
- <span data-ttu-id="c2eac-186">53 GB</span><span class="sxs-lookup"><span data-stu-id="c2eac-186">53GB</span></span>
- <span data-ttu-id="c2eac-187">120 GB Der Standardwert ist 1 GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="c2eac-187">120GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-188">-Sku</span><span class="sxs-lookup"><span data-stu-id="c2eac-188">-Sku</span></span>
<span data-ttu-id="c2eac-189">Gibt die SKU des zu erstellenden Redis-Caches an.</span><span class="sxs-lookup"><span data-stu-id="c2eac-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="c2eac-190">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c2eac-190">Valid values are:</span></span> 
- <span data-ttu-id="c2eac-191">Basic</span><span class="sxs-lookup"><span data-stu-id="c2eac-191">Basic</span></span>
- <span data-ttu-id="c2eac-192">Standard</span><span class="sxs-lookup"><span data-stu-id="c2eac-192">Standard</span></span>
- <span data-ttu-id="c2eac-193">Premium Der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="c2eac-193">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2eac-194">-Tag</span></span>
<span data-ttu-id="c2eac-195">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2eac-195">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="c2eac-196">-TenantSettings</span></span>
<span data-ttu-id="c2eac-197">Dieser Parameter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c2eac-197">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-198">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2eac-198">-Confirm</span></span>
<span data-ttu-id="c2eac-199">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2eac-199">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2eac-200">-WhatIf</span></span>
<span data-ttu-id="c2eac-201">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2eac-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2eac-202">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2eac-202">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2eac-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2eac-203">CommonParameters</span></span>
<span data-ttu-id="c2eac-204">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2eac-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2eac-205">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2eac-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2eac-206">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2eac-206">INPUTS</span></span>

### <span data-ttu-id="c2eac-207">System.String</span><span class="sxs-lookup"><span data-stu-id="c2eac-207">System.String</span></span>

### <span data-ttu-id="c2eac-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2eac-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c2eac-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c2eac-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c2eac-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c2eac-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c2eac-211">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2eac-211">OUTPUTS</span></span>

### <span data-ttu-id="c2eac-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c2eac-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="c2eac-213">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c2eac-213">NOTES</span></span>

## <span data-ttu-id="c2eac-214">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c2eac-214">RELATED LINKS</span></span>

[<span data-ttu-id="c2eac-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2eac-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c2eac-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2eac-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c2eac-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2eac-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


