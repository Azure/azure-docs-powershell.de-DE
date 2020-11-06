---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482778"
---
# <span data-ttu-id="49423-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="49423-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="49423-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49423-102">SYNOPSIS</span></span>
<span data-ttu-id="49423-103">Ändert einen "a-a-Cache".</span><span class="sxs-lookup"><span data-stu-id="49423-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49423-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49423-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49423-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49423-105">DESCRIPTION</span></span>
<span data-ttu-id="49423-106">Das Cmdlet " **Satz-AzureRmRedisCache** " ändert einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="49423-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="49423-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49423-107">EXAMPLES</span></span>

### <span data-ttu-id="49423-108">Beispiel 1: Ändern eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="49423-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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

<span data-ttu-id="49423-109">Mit diesem Befehl wird die maxmemory-Richtlinie für den Namen "myCache" für den "a-Cache" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="49423-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="49423-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="49423-110">PARAMETERS</span></span>

### <span data-ttu-id="49423-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49423-111">-DefaultProfile</span></span>
<span data-ttu-id="49423-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49423-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49423-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="49423-113">-EnableNonSslPort</span></span>
<span data-ttu-id="49423-114">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="49423-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="49423-115">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="49423-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="49423-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="49423-117">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="49423-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="49423-118">Verwenden Sie den *RedisConfiguration* -Parameter, um die maxmemory-Richtlinie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="49423-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="49423-119">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="49423-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-120">-Name</span><span class="sxs-lookup"><span data-stu-id="49423-120">-Name</span></span>
<span data-ttu-id="49423-121">Gibt den Namen des zu aktualisierbaren "zu aktualisierbaren Speichers" an.</span><span class="sxs-lookup"><span data-stu-id="49423-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="49423-122">-RedisConfiguration</span></span>
<span data-ttu-id="49423-123">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="49423-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="49423-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="49423-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49423-125">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="49423-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="49423-126">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="49423-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="49423-127">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="49423-127">Premium tier only.</span></span>
- <span data-ttu-id="49423-128">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="49423-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="49423-129">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="49423-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="49423-130">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="49423-130">Premium tier only.</span></span>
- <span data-ttu-id="49423-131">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="49423-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="49423-132">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="49423-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="49423-133">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="49423-133">Premium tier only.</span></span> 
- <span data-ttu-id="49423-134">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="49423-134">maxmemory-reserved.</span></span>
<span data-ttu-id="49423-135">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="49423-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="49423-136">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="49423-137">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="49423-137">maxmemory-policy.</span></span>
<span data-ttu-id="49423-138">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="49423-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="49423-139">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="49423-139">All pricing tiers.</span></span> 
- <span data-ttu-id="49423-140">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="49423-140">notify-keyspace-events.</span></span>
<span data-ttu-id="49423-141">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="49423-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="49423-142">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="49423-143">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="49423-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="49423-144">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="49423-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="49423-145">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="49423-146">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="49423-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="49423-147">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="49423-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="49423-148">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="49423-149">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="49423-149">set-max-intset-entries.</span></span>
<span data-ttu-id="49423-150">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="49423-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="49423-151">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="49423-152">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="49423-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="49423-153">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="49423-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="49423-154">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="49423-155">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="49423-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="49423-156">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="49423-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="49423-157">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="49423-158">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="49423-158">databases.</span></span>
<span data-ttu-id="49423-159">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="49423-159">Configures the number of databases.</span></span>
<span data-ttu-id="49423-160">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="49423-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="49423-161">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="49423-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="49423-162">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="49423-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49423-163">-ResourceGroupName</span></span>
<span data-ttu-id="49423-164">Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="49423-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="49423-165">-ShardCount</span></span>
<span data-ttu-id="49423-166">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="49423-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-167">-Size</span><span class="sxs-lookup"><span data-stu-id="49423-167">-Size</span></span>
<span data-ttu-id="49423-168">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="49423-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="49423-169">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="49423-169">Valid values are:</span></span> 

- <span data-ttu-id="49423-170">P1</span><span class="sxs-lookup"><span data-stu-id="49423-170">P1</span></span>
- <span data-ttu-id="49423-171">P2</span><span class="sxs-lookup"><span data-stu-id="49423-171">P2</span></span>
- <span data-ttu-id="49423-172">P3</span><span class="sxs-lookup"><span data-stu-id="49423-172">P3</span></span>
- <span data-ttu-id="49423-173">P4</span><span class="sxs-lookup"><span data-stu-id="49423-173">P4</span></span>
- <span data-ttu-id="49423-174">C0</span><span class="sxs-lookup"><span data-stu-id="49423-174">C0</span></span>
- <span data-ttu-id="49423-175">C1</span><span class="sxs-lookup"><span data-stu-id="49423-175">C1</span></span>
- <span data-ttu-id="49423-176">C2</span><span class="sxs-lookup"><span data-stu-id="49423-176">C2</span></span>
- <span data-ttu-id="49423-177">C3</span><span class="sxs-lookup"><span data-stu-id="49423-177">C3</span></span>
- <span data-ttu-id="49423-178">C4</span><span class="sxs-lookup"><span data-stu-id="49423-178">C4</span></span>
- <span data-ttu-id="49423-179">C5</span><span class="sxs-lookup"><span data-stu-id="49423-179">C5</span></span>
- <span data-ttu-id="49423-180">C6</span><span class="sxs-lookup"><span data-stu-id="49423-180">C6</span></span>
- <span data-ttu-id="49423-181">250MB</span><span class="sxs-lookup"><span data-stu-id="49423-181">250MB</span></span>
- <span data-ttu-id="49423-182">1 GB</span><span class="sxs-lookup"><span data-stu-id="49423-182">1GB</span></span>
- <span data-ttu-id="49423-183">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="49423-183">2.5GB</span></span>
- <span data-ttu-id="49423-184">6GB</span><span class="sxs-lookup"><span data-stu-id="49423-184">6GB</span></span>
- <span data-ttu-id="49423-185">13GB</span><span class="sxs-lookup"><span data-stu-id="49423-185">13GB</span></span>
- <span data-ttu-id="49423-186">26GB</span><span class="sxs-lookup"><span data-stu-id="49423-186">26GB</span></span>
- <span data-ttu-id="49423-187">53GB</span><span class="sxs-lookup"><span data-stu-id="49423-187">53GB</span></span>

<span data-ttu-id="49423-188">Der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="49423-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="49423-189">-Sku</span></span>
<span data-ttu-id="49423-190">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="49423-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="49423-191">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="49423-191">Valid values are:</span></span> 

- <span data-ttu-id="49423-192">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="49423-192">Basic</span></span>
- <span data-ttu-id="49423-193">Standard</span><span class="sxs-lookup"><span data-stu-id="49423-193">Standard</span></span>
- <span data-ttu-id="49423-194">Premium</span><span class="sxs-lookup"><span data-stu-id="49423-194">Premium</span></span>

<span data-ttu-id="49423-195">Der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="49423-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-196">-Tag</span><span class="sxs-lookup"><span data-stu-id="49423-196">-Tag</span></span>
<span data-ttu-id="49423-197">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="49423-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="49423-198">-TenantSettings</span></span>
<span data-ttu-id="49423-199">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="49423-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49423-200">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49423-200">-Confirm</span></span>
<span data-ttu-id="49423-201">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49423-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49423-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49423-202">-WhatIf</span></span>
<span data-ttu-id="49423-203">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49423-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49423-204">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49423-204">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49423-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49423-205">CommonParameters</span></span>
<span data-ttu-id="49423-206">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49423-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49423-207">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49423-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49423-208">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49423-208">INPUTS</span></span>

### <span data-ttu-id="49423-209">Keine</span><span class="sxs-lookup"><span data-stu-id="49423-209">None</span></span>
<span data-ttu-id="49423-210">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="49423-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="49423-211">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49423-211">OUTPUTS</span></span>

### <span data-ttu-id="49423-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="49423-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="49423-213">Gibt alle Attribute eines "4-a-Cache" zurück, einschließlich primärer und sekundärer Zugriffstasten.</span><span class="sxs-lookup"><span data-stu-id="49423-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="49423-214">Notizen</span><span class="sxs-lookup"><span data-stu-id="49423-214">NOTES</span></span>

## <span data-ttu-id="49423-215">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49423-215">RELATED LINKS</span></span>

[<span data-ttu-id="49423-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="49423-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="49423-217">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="49423-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="49423-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="49423-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


