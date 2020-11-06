---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481654"
---
# <span data-ttu-id="0cc9a-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0cc9a-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="0cc9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc9a-103">Ändert einen "a-a-Cache".</span><span class="sxs-lookup"><span data-stu-id="0cc9a-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cc9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cc9a-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cc9a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cc9a-105">DESCRIPTION</span></span>
<span data-ttu-id="0cc9a-106">Das Cmdlet " **Satz-AzureRmRedisCache** " ändert einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="0cc9a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cc9a-107">EXAMPLES</span></span>

### <span data-ttu-id="0cc9a-108">Beispiel 1: Ändern eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="0cc9a-108">Example 1: Modify a Redis Cache</span></span>
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
```

<span data-ttu-id="0cc9a-109">Mit diesem Befehl wird die maxmemory-Richtlinie für den Namen "myCache" für den "a-Cache" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="0cc9a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cc9a-110">PARAMETERS</span></span>

### <span data-ttu-id="0cc9a-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="0cc9a-111">-EnableNonSslPort</span></span>
<span data-ttu-id="0cc9a-112">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="0cc9a-113">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="0cc9a-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="0cc9a-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="0cc9a-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="0cc9a-115">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="0cc9a-116">Verwenden Sie den *RedisConfiguration* -Parameter, um die maxmemory-Richtlinie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="0cc9a-117">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0cc9a-117">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="0cc9a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0cc9a-118">-Name</span></span>
<span data-ttu-id="0cc9a-119">Gibt den Namen des zu aktualisierbaren "zu aktualisierbaren Speichers" an.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="0cc9a-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="0cc9a-120">-RedisConfiguration</span></span>
<span data-ttu-id="0cc9a-121">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="0cc9a-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0cc9a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cc9a-123">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="0cc9a-124">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="0cc9a-125">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-125">Premium tier only.</span></span>
- <span data-ttu-id="0cc9a-126">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="0cc9a-127">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="0cc9a-128">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-128">Premium tier only.</span></span>
- <span data-ttu-id="0cc9a-129">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="0cc9a-130">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="0cc9a-131">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-131">Premium tier only.</span></span> 
- <span data-ttu-id="0cc9a-132">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-132">maxmemory-reserved.</span></span>
<span data-ttu-id="0cc9a-133">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="0cc9a-134">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0cc9a-135">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-135">maxmemory-policy.</span></span>
<span data-ttu-id="0cc9a-136">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="0cc9a-137">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-137">All pricing tiers.</span></span> 
- <span data-ttu-id="0cc9a-138">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-138">notify-keyspace-events.</span></span>
<span data-ttu-id="0cc9a-139">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="0cc9a-140">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="0cc9a-141">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="0cc9a-142">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0cc9a-143">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0cc9a-144">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="0cc9a-145">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0cc9a-146">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0cc9a-147">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-147">set-max-intset-entries.</span></span>
<span data-ttu-id="0cc9a-148">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0cc9a-149">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0cc9a-150">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="0cc9a-151">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0cc9a-152">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0cc9a-153">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="0cc9a-154">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0cc9a-155">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0cc9a-156">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-156">databases.</span></span>
<span data-ttu-id="0cc9a-157">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-157">Configures the number of databases.</span></span>
<span data-ttu-id="0cc9a-158">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="0cc9a-159">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="0cc9a-160">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="0cc9a-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="0cc9a-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc9a-161">-ResourceGroupName</span></span>
<span data-ttu-id="0cc9a-162">Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="0cc9a-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="0cc9a-163">-ShardCount</span></span>
<span data-ttu-id="0cc9a-164">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="0cc9a-165">-Size</span><span class="sxs-lookup"><span data-stu-id="0cc9a-165">-Size</span></span>
<span data-ttu-id="0cc9a-166">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="0cc9a-167">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0cc9a-167">Valid values are:</span></span> 

- <span data-ttu-id="0cc9a-168">P1</span><span class="sxs-lookup"><span data-stu-id="0cc9a-168">P1</span></span>
- <span data-ttu-id="0cc9a-169">P2</span><span class="sxs-lookup"><span data-stu-id="0cc9a-169">P2</span></span>
- <span data-ttu-id="0cc9a-170">P3</span><span class="sxs-lookup"><span data-stu-id="0cc9a-170">P3</span></span>
- <span data-ttu-id="0cc9a-171">P4</span><span class="sxs-lookup"><span data-stu-id="0cc9a-171">P4</span></span>
- <span data-ttu-id="0cc9a-172">C0</span><span class="sxs-lookup"><span data-stu-id="0cc9a-172">C0</span></span>
- <span data-ttu-id="0cc9a-173">C1</span><span class="sxs-lookup"><span data-stu-id="0cc9a-173">C1</span></span>
- <span data-ttu-id="0cc9a-174">C2</span><span class="sxs-lookup"><span data-stu-id="0cc9a-174">C2</span></span>
- <span data-ttu-id="0cc9a-175">C3</span><span class="sxs-lookup"><span data-stu-id="0cc9a-175">C3</span></span>
- <span data-ttu-id="0cc9a-176">C4</span><span class="sxs-lookup"><span data-stu-id="0cc9a-176">C4</span></span>
- <span data-ttu-id="0cc9a-177">C5</span><span class="sxs-lookup"><span data-stu-id="0cc9a-177">C5</span></span>
- <span data-ttu-id="0cc9a-178">C6</span><span class="sxs-lookup"><span data-stu-id="0cc9a-178">C6</span></span>
- <span data-ttu-id="0cc9a-179">250MB</span><span class="sxs-lookup"><span data-stu-id="0cc9a-179">250MB</span></span>
- <span data-ttu-id="0cc9a-180">1 GB</span><span class="sxs-lookup"><span data-stu-id="0cc9a-180">1GB</span></span>
- <span data-ttu-id="0cc9a-181">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="0cc9a-181">2.5GB</span></span>
- <span data-ttu-id="0cc9a-182">6GB</span><span class="sxs-lookup"><span data-stu-id="0cc9a-182">6GB</span></span>
- <span data-ttu-id="0cc9a-183">13GB</span><span class="sxs-lookup"><span data-stu-id="0cc9a-183">13GB</span></span>
- <span data-ttu-id="0cc9a-184">26GB</span><span class="sxs-lookup"><span data-stu-id="0cc9a-184">26GB</span></span>
- <span data-ttu-id="0cc9a-185">53GB</span><span class="sxs-lookup"><span data-stu-id="0cc9a-185">53GB</span></span>

<span data-ttu-id="0cc9a-186">Der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-186">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cc9a-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="0cc9a-187">-Sku</span></span>
<span data-ttu-id="0cc9a-188">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="0cc9a-189">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0cc9a-189">Valid values are:</span></span> 

- <span data-ttu-id="0cc9a-190">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="0cc9a-190">Basic</span></span>
- <span data-ttu-id="0cc9a-191">Standard</span><span class="sxs-lookup"><span data-stu-id="0cc9a-191">Standard</span></span>
- <span data-ttu-id="0cc9a-192">Premium</span><span class="sxs-lookup"><span data-stu-id="0cc9a-192">Premium</span></span>

<span data-ttu-id="0cc9a-193">Der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="0cc9a-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="0cc9a-194">-TenantSettings</span></span>
<span data-ttu-id="0cc9a-195">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="0cc9a-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc9a-196">-DefaultProfile</span></span>
<span data-ttu-id="0cc9a-197">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc9a-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc9a-198">CommonParameters</span></span>
<span data-ttu-id="0cc9a-199">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc9a-200">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc9a-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc9a-201">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cc9a-201">INPUTS</span></span>

### <span data-ttu-id="0cc9a-202">Keine</span><span class="sxs-lookup"><span data-stu-id="0cc9a-202">None</span></span>
<span data-ttu-id="0cc9a-203">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0cc9a-204">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cc9a-204">OUTPUTS</span></span>

### <span data-ttu-id="0cc9a-205">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0cc9a-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="0cc9a-206">Gibt alle Attribute eines "4-a-Cache" zurück, einschließlich primärer und sekundärer Zugriffstasten.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="0cc9a-207">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cc9a-207">NOTES</span></span>

## <span data-ttu-id="0cc9a-208">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cc9a-208">RELATED LINKS</span></span>

[<span data-ttu-id="0cc9a-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0cc9a-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="0cc9a-210">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0cc9a-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0cc9a-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0cc9a-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


