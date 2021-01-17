---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459616"
---
# <span data-ttu-id="356ac-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="356ac-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="356ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="356ac-102">SYNOPSIS</span></span>
<span data-ttu-id="356ac-103">Ändert einen Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="356ac-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="356ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="356ac-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="356ac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="356ac-105">DESCRIPTION</span></span>
<span data-ttu-id="356ac-106">Das **Cmdlet "Set-AzRedisCache"** ändert einen Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="356ac-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="356ac-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="356ac-107">EXAMPLES</span></span>

### <span data-ttu-id="356ac-108">Beispiel 1: Ändern eines Caches für Redis</span><span class="sxs-lookup"><span data-stu-id="356ac-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="356ac-109">Mit diesem Befehl wird die "maxmemory-policy" für den Redis-Cache namens "MyCache" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="356ac-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="356ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="356ac-110">PARAMETERS</span></span>

### <span data-ttu-id="356ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356ac-111">-DefaultProfile</span></span>
<span data-ttu-id="356ac-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="356ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="356ac-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="356ac-113">-EnableNonSslPort</span></span>
<span data-ttu-id="356ac-114">Gibt an, ob der Nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="356ac-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="356ac-115">Der Standardwert ist $False (der Nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="356ac-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="356ac-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="356ac-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="356ac-117">Geben Sie die TLS-Version an, die von Clients zum Herstellen einer Verbindung mit dem Cache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="356ac-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="356ac-118">-Name</span><span class="sxs-lookup"><span data-stu-id="356ac-118">-Name</span></span>
<span data-ttu-id="356ac-119">Gibt den Namen des zu aktualisierenden Caches für Redis an.</span><span class="sxs-lookup"><span data-stu-id="356ac-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="356ac-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="356ac-120">-RedisConfiguration</span></span>
<span data-ttu-id="356ac-121">Gibt die Konfigurationseinstellungen von Redis an.</span><span class="sxs-lookup"><span data-stu-id="356ac-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="356ac-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="356ac-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="356ac-123">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="356ac-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="356ac-124">Gibt an, dass die Daten persistenz von Redis aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="356ac-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="356ac-125">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="356ac-125">Premium tier only.</span></span>
- <span data-ttu-id="356ac-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="356ac-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="356ac-127">Gibt die Verbindungszeichenfolge zum Speicherkonto für die Daten persistenz von Redis an.</span><span class="sxs-lookup"><span data-stu-id="356ac-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="356ac-128">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="356ac-128">Premium tier only.</span></span>
- <span data-ttu-id="356ac-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="356ac-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="356ac-130">Gibt die Sicherungshäufigkeit für die Daten persistenz von Redis an.</span><span class="sxs-lookup"><span data-stu-id="356ac-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="356ac-131">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="356ac-131">Premium tier only.</span></span> 
- <span data-ttu-id="356ac-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="356ac-132">maxmemory-reserved.</span></span>
<span data-ttu-id="356ac-133">Konfiguriert den Speicher, der für Prozesse ohne Cache reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="356ac-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="356ac-134">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="356ac-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="356ac-135">maxmemory-policy.</span></span>
<span data-ttu-id="356ac-136">Konfiguriert die Entfernungsrichtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="356ac-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="356ac-137">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-137">All pricing tiers.</span></span> 
- <span data-ttu-id="356ac-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="356ac-138">notify-keyspace-events.</span></span>
<span data-ttu-id="356ac-139">Konfiguriert Keyspacebenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="356ac-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="356ac-140">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="356ac-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="356ac-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="356ac-142">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="356ac-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="356ac-143">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="356ac-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="356ac-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="356ac-145">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="356ac-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="356ac-146">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="356ac-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="356ac-147">set-max-intset-entries.</span></span>
<span data-ttu-id="356ac-148">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="356ac-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="356ac-149">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="356ac-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="356ac-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="356ac-151">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="356ac-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="356ac-152">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="356ac-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="356ac-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="356ac-154">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="356ac-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="356ac-155">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="356ac-156">datenbanken.</span><span class="sxs-lookup"><span data-stu-id="356ac-156">databases.</span></span>
<span data-ttu-id="356ac-157">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="356ac-157">Configures the number of databases.</span></span>
<span data-ttu-id="356ac-158">Diese Eigenschaft kann nur beim Erstellen des Caches konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="356ac-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="356ac-159">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="356ac-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="356ac-160">Weitere Informationen finden Sie unter Verwalten des Azure Redis Cache mit Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="356ac-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="356ac-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="356ac-161">-ResourceGroupName</span></span>
<span data-ttu-id="356ac-162">Gibt den Namen der Ressourcengruppe an, die den Cache von Redis enthält.</span><span class="sxs-lookup"><span data-stu-id="356ac-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="356ac-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="356ac-163">-ShardCount</span></span>
<span data-ttu-id="356ac-164">Gibt die Anzahl der in einem Premium-Clustercache zu erstellenden Shards an.</span><span class="sxs-lookup"><span data-stu-id="356ac-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="356ac-165">-Size</span><span class="sxs-lookup"><span data-stu-id="356ac-165">-Size</span></span>
<span data-ttu-id="356ac-166">Gibt die Größe des Caches von Redis an.</span><span class="sxs-lookup"><span data-stu-id="356ac-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="356ac-167">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="356ac-167">Valid values are:</span></span> 
- <span data-ttu-id="356ac-168">P1</span><span class="sxs-lookup"><span data-stu-id="356ac-168">P1</span></span>
- <span data-ttu-id="356ac-169">P2</span><span class="sxs-lookup"><span data-stu-id="356ac-169">P2</span></span>
- <span data-ttu-id="356ac-170">P3</span><span class="sxs-lookup"><span data-stu-id="356ac-170">P3</span></span>
- <span data-ttu-id="356ac-171">P4</span><span class="sxs-lookup"><span data-stu-id="356ac-171">P4</span></span>
- <span data-ttu-id="356ac-172">P5</span><span class="sxs-lookup"><span data-stu-id="356ac-172">P5</span></span>
- <span data-ttu-id="356ac-173">C0</span><span class="sxs-lookup"><span data-stu-id="356ac-173">C0</span></span>
- <span data-ttu-id="356ac-174">C1</span><span class="sxs-lookup"><span data-stu-id="356ac-174">C1</span></span>
- <span data-ttu-id="356ac-175">C2</span><span class="sxs-lookup"><span data-stu-id="356ac-175">C2</span></span>
- <span data-ttu-id="356ac-176">C3</span><span class="sxs-lookup"><span data-stu-id="356ac-176">C3</span></span>
- <span data-ttu-id="356ac-177">C4</span><span class="sxs-lookup"><span data-stu-id="356ac-177">C4</span></span>
- <span data-ttu-id="356ac-178">C5</span><span class="sxs-lookup"><span data-stu-id="356ac-178">C5</span></span>
- <span data-ttu-id="356ac-179">C6</span><span class="sxs-lookup"><span data-stu-id="356ac-179">C6</span></span>
- <span data-ttu-id="356ac-180">250 MB</span><span class="sxs-lookup"><span data-stu-id="356ac-180">250MB</span></span>
- <span data-ttu-id="356ac-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="356ac-181">1GB</span></span>
- <span data-ttu-id="356ac-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="356ac-182">2.5GB</span></span>
- <span data-ttu-id="356ac-183">6 GB</span><span class="sxs-lookup"><span data-stu-id="356ac-183">6GB</span></span>
- <span data-ttu-id="356ac-184">13 GB</span><span class="sxs-lookup"><span data-stu-id="356ac-184">13GB</span></span>
- <span data-ttu-id="356ac-185">26 GB</span><span class="sxs-lookup"><span data-stu-id="356ac-185">26GB</span></span>
- <span data-ttu-id="356ac-186">53 GB</span><span class="sxs-lookup"><span data-stu-id="356ac-186">53GB</span></span>
- <span data-ttu-id="356ac-187">120 GB Der Standardwert ist 1 GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="356ac-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="356ac-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="356ac-188">-Sku</span></span>
<span data-ttu-id="356ac-189">Gibt die SKU des zu erstellenden Caches für Redis an.</span><span class="sxs-lookup"><span data-stu-id="356ac-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="356ac-190">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="356ac-190">Valid values are:</span></span> 
- <span data-ttu-id="356ac-191">Standard</span><span class="sxs-lookup"><span data-stu-id="356ac-191">Basic</span></span>
- <span data-ttu-id="356ac-192">Standard</span><span class="sxs-lookup"><span data-stu-id="356ac-192">Standard</span></span>
- <span data-ttu-id="356ac-193">Premium Der Standardwert ist "Standard".</span><span class="sxs-lookup"><span data-stu-id="356ac-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="356ac-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="356ac-194">-Tag</span></span>
<span data-ttu-id="356ac-195">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="356ac-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="356ac-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="356ac-196">-TenantSettings</span></span>
<span data-ttu-id="356ac-197">Dieser Parameter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="356ac-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="356ac-198">-Confirm</span><span class="sxs-lookup"><span data-stu-id="356ac-198">-Confirm</span></span>
<span data-ttu-id="356ac-199">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="356ac-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356ac-200">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="356ac-200">-WhatIf</span></span>
<span data-ttu-id="356ac-201">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="356ac-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="356ac-202">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="356ac-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356ac-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356ac-203">CommonParameters</span></span>
<span data-ttu-id="356ac-204">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356ac-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356ac-205">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="356ac-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356ac-206">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="356ac-206">INPUTS</span></span>

### <span data-ttu-id="356ac-207">System.String</span><span class="sxs-lookup"><span data-stu-id="356ac-207">System.String</span></span>

### <span data-ttu-id="356ac-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="356ac-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="356ac-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="356ac-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="356ac-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="356ac-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="356ac-211">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="356ac-211">OUTPUTS</span></span>

### <span data-ttu-id="356ac-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="356ac-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="356ac-213">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="356ac-213">NOTES</span></span>

## <span data-ttu-id="356ac-214">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="356ac-214">RELATED LINKS</span></span>

[<span data-ttu-id="356ac-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="356ac-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="356ac-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="356ac-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="356ac-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="356ac-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


