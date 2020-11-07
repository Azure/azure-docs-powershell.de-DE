---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662626"
---
# <span data-ttu-id="d907c-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d907c-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="d907c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d907c-102">SYNOPSIS</span></span>
<span data-ttu-id="d907c-103">Erstellt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="d907c-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d907c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d907c-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d907c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d907c-105">DESCRIPTION</span></span>
<span data-ttu-id="d907c-106">Mit dem Cmdlet " **New-AzureRmRedisCache** " wird ein Azure-Teiler-Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="d907c-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="d907c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d907c-107">EXAMPLES</span></span>

### <span data-ttu-id="d907c-108">Beispiel 1: Erstellen eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="d907c-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

<span data-ttu-id="d907c-109">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="d907c-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="d907c-110">Beispiel 2: Erstellen eines Standard mäßigen SKUs-Caches</span><span class="sxs-lookup"><span data-stu-id="d907c-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

<span data-ttu-id="d907c-111">Mit diesem Befehl wird ein a/a-Cache erstellt, oder der Zwischenspeicher für den "a/a" wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d907c-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="d907c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d907c-112">PARAMETERS</span></span>

### <span data-ttu-id="d907c-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="d907c-113">-EnableNonSslPort</span></span>
<span data-ttu-id="d907c-114">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d907c-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="d907c-115">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="d907c-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="d907c-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="d907c-116">-Location</span></span>
<span data-ttu-id="d907c-117">Gibt den Speicherort an, an dem ein a-a/a-Cache erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d907c-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="d907c-118">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d907c-118">Valid values are:</span></span> 

- <span data-ttu-id="d907c-119">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="d907c-119">North Central US</span></span>
- <span data-ttu-id="d907c-120">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="d907c-120">South Central US</span></span>
- <span data-ttu-id="d907c-121">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="d907c-121">Central US</span></span>
- <span data-ttu-id="d907c-122">West Europa</span><span class="sxs-lookup"><span data-stu-id="d907c-122">West Europe</span></span>
- <span data-ttu-id="d907c-123">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="d907c-123">North Europe</span></span>
- <span data-ttu-id="d907c-124">West-US</span><span class="sxs-lookup"><span data-stu-id="d907c-124">West US</span></span>
- <span data-ttu-id="d907c-125">East US</span><span class="sxs-lookup"><span data-stu-id="d907c-125">East US</span></span>
- <span data-ttu-id="d907c-126">East US 2</span><span class="sxs-lookup"><span data-stu-id="d907c-126">East US 2</span></span>
- <span data-ttu-id="d907c-127">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="d907c-127">Japan East</span></span>
- <span data-ttu-id="d907c-128">Japan West</span><span class="sxs-lookup"><span data-stu-id="d907c-128">Japan West</span></span>
- <span data-ttu-id="d907c-129">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="d907c-129">Brazil South</span></span>
- <span data-ttu-id="d907c-130">Südostasien</span><span class="sxs-lookup"><span data-stu-id="d907c-130">Southeast Asia</span></span>
- <span data-ttu-id="d907c-131">Ostasien</span><span class="sxs-lookup"><span data-stu-id="d907c-131">East Asia</span></span>
- <span data-ttu-id="d907c-132">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="d907c-132">Australia East</span></span>
- <span data-ttu-id="d907c-133">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="d907c-133">Australia Southeast</span></span>

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

### <span data-ttu-id="d907c-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="d907c-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="d907c-135">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="d907c-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="d907c-136">Verwenden Sie den *RedisConfiguration* -Parameter, um die maxmemory-Richtlinie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d907c-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="d907c-137">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d907c-137">For example:</span></span> 

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

### <span data-ttu-id="d907c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d907c-138">-Name</span></span>
<span data-ttu-id="d907c-139">Gibt den Namen des zu erstellbaren zu erstellbaren zu erstellbaren zu.</span><span class="sxs-lookup"><span data-stu-id="d907c-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="d907c-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="d907c-140">-RedisConfiguration</span></span>
<span data-ttu-id="d907c-141">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d907c-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="d907c-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d907c-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d907c-143">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d907c-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="d907c-144">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d907c-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="d907c-145">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="d907c-145">Premium tier only.</span></span>
- <span data-ttu-id="d907c-146">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d907c-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="d907c-147">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="d907c-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="d907c-148">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="d907c-148">Premium tier only.</span></span>
- <span data-ttu-id="d907c-149">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="d907c-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="d907c-150">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="d907c-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="d907c-151">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="d907c-151">Premium tier only.</span></span> 
- <span data-ttu-id="d907c-152">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="d907c-152">maxmemory-reserved.</span></span>
<span data-ttu-id="d907c-153">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d907c-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="d907c-154">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d907c-155">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d907c-155">maxmemory-policy.</span></span>
<span data-ttu-id="d907c-156">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="d907c-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="d907c-157">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-157">All pricing tiers.</span></span> 
- <span data-ttu-id="d907c-158">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d907c-158">notify-keyspace-events.</span></span>
<span data-ttu-id="d907c-159">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="d907c-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="d907c-160">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="d907c-161">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="d907c-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="d907c-162">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d907c-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d907c-163">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d907c-164">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="d907c-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="d907c-165">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d907c-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d907c-166">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d907c-167">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="d907c-167">set-max-intset-entries.</span></span>
<span data-ttu-id="d907c-168">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d907c-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d907c-169">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d907c-170">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="d907c-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="d907c-171">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d907c-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d907c-172">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d907c-173">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="d907c-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="d907c-174">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d907c-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d907c-175">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d907c-176">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="d907c-176">databases.</span></span>
<span data-ttu-id="d907c-177">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="d907c-177">Configures the number of databases.</span></span>
<span data-ttu-id="d907c-178">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d907c-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="d907c-179">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d907c-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="d907c-180">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="d907c-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="d907c-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="d907c-181">-RedisVersion</span></span>
<span data-ttu-id="d907c-182">Dieser Parameter ist veraltet und wird aus zukünftigen Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="d907c-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="d907c-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d907c-183">-ResourceGroupName</span></span>
<span data-ttu-id="d907c-184">Gibt den Namen der Ressourcengruppe an, in der der "a/a-Cache" erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d907c-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="d907c-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="d907c-185">-ShardCount</span></span>
<span data-ttu-id="d907c-186">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="d907c-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="d907c-187">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d907c-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d907c-188">1</span><span class="sxs-lookup"><span data-stu-id="d907c-188">1</span></span>
- <span data-ttu-id="d907c-189">2</span><span class="sxs-lookup"><span data-stu-id="d907c-189">2</span></span>
- <span data-ttu-id="d907c-190">3</span><span class="sxs-lookup"><span data-stu-id="d907c-190">3</span></span>
- <span data-ttu-id="d907c-191">4</span><span class="sxs-lookup"><span data-stu-id="d907c-191">4</span></span>
- <span data-ttu-id="d907c-192">5</span><span class="sxs-lookup"><span data-stu-id="d907c-192">5</span></span>
- <span data-ttu-id="d907c-193">6</span><span class="sxs-lookup"><span data-stu-id="d907c-193">6</span></span>
- <span data-ttu-id="d907c-194">7</span><span class="sxs-lookup"><span data-stu-id="d907c-194">7</span></span>
- <span data-ttu-id="d907c-195">8</span><span class="sxs-lookup"><span data-stu-id="d907c-195">8</span></span>
- <span data-ttu-id="d907c-196">9</span><span class="sxs-lookup"><span data-stu-id="d907c-196">9</span></span> 
- <span data-ttu-id="d907c-197">10</span><span class="sxs-lookup"><span data-stu-id="d907c-197">10</span></span>

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

### <span data-ttu-id="d907c-198">-Size</span><span class="sxs-lookup"><span data-stu-id="d907c-198">-Size</span></span>
<span data-ttu-id="d907c-199">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="d907c-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="d907c-200">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d907c-200">Valid values are:</span></span> 

- <span data-ttu-id="d907c-201">P1</span><span class="sxs-lookup"><span data-stu-id="d907c-201">P1</span></span>
- <span data-ttu-id="d907c-202">P2</span><span class="sxs-lookup"><span data-stu-id="d907c-202">P2</span></span>
- <span data-ttu-id="d907c-203">P3</span><span class="sxs-lookup"><span data-stu-id="d907c-203">P3</span></span>
- <span data-ttu-id="d907c-204">P4</span><span class="sxs-lookup"><span data-stu-id="d907c-204">P4</span></span>
- <span data-ttu-id="d907c-205">C0</span><span class="sxs-lookup"><span data-stu-id="d907c-205">C0</span></span>
- <span data-ttu-id="d907c-206">C1</span><span class="sxs-lookup"><span data-stu-id="d907c-206">C1</span></span>
- <span data-ttu-id="d907c-207">C2</span><span class="sxs-lookup"><span data-stu-id="d907c-207">C2</span></span>
- <span data-ttu-id="d907c-208">C3</span><span class="sxs-lookup"><span data-stu-id="d907c-208">C3</span></span>
- <span data-ttu-id="d907c-209">C4</span><span class="sxs-lookup"><span data-stu-id="d907c-209">C4</span></span>
- <span data-ttu-id="d907c-210">C5</span><span class="sxs-lookup"><span data-stu-id="d907c-210">C5</span></span>
- <span data-ttu-id="d907c-211">C6</span><span class="sxs-lookup"><span data-stu-id="d907c-211">C6</span></span>
- <span data-ttu-id="d907c-212">250MB</span><span class="sxs-lookup"><span data-stu-id="d907c-212">250MB</span></span>
- <span data-ttu-id="d907c-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="d907c-213">1GB</span></span>
- <span data-ttu-id="d907c-214">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="d907c-214">2.5GB</span></span>
- <span data-ttu-id="d907c-215">6GB</span><span class="sxs-lookup"><span data-stu-id="d907c-215">6GB</span></span>
- <span data-ttu-id="d907c-216">13GB</span><span class="sxs-lookup"><span data-stu-id="d907c-216">13GB</span></span>
- <span data-ttu-id="d907c-217">26GB</span><span class="sxs-lookup"><span data-stu-id="d907c-217">26GB</span></span>
- <span data-ttu-id="d907c-218">53GB</span><span class="sxs-lookup"><span data-stu-id="d907c-218">53GB</span></span>

<span data-ttu-id="d907c-219">Der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="d907c-219">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="d907c-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="d907c-220">-Sku</span></span>
<span data-ttu-id="d907c-221">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="d907c-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="d907c-222">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d907c-222">Valid values are:</span></span> 

- <span data-ttu-id="d907c-223">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="d907c-223">Basic</span></span>
- <span data-ttu-id="d907c-224">Standard</span><span class="sxs-lookup"><span data-stu-id="d907c-224">Standard</span></span>
- <span data-ttu-id="d907c-225">Premium</span><span class="sxs-lookup"><span data-stu-id="d907c-225">Premium</span></span>

<span data-ttu-id="d907c-226">Der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="d907c-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="d907c-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="d907c-227">-StaticIP</span></span>
<span data-ttu-id="d907c-228">Gibt eine eindeutige IP-Adresse im Subnetz für den Cache für den "a/a-Cache" an.</span><span class="sxs-lookup"><span data-stu-id="d907c-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="d907c-229">Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.</span><span class="sxs-lookup"><span data-stu-id="d907c-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="d907c-230">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="d907c-230">-Subnet</span></span>
<span data-ttu-id="d907c-231">Gibt den Namen des Subnets an, in dem der "a-Cache" bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d907c-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="d907c-232">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="d907c-232">-SubnetId</span></span>
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

### <span data-ttu-id="d907c-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="d907c-233">-TenantSettings</span></span>
<span data-ttu-id="d907c-234">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="d907c-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="d907c-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d907c-235">-VirtualNetwork</span></span>
<span data-ttu-id="d907c-236">Gibt die Ressourcen-ID des virtuellen Netzwerks an, in dem der "a-Cache" bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d907c-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="d907c-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d907c-237">-DefaultProfile</span></span>
<span data-ttu-id="d907c-238">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d907c-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d907c-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d907c-239">CommonParameters</span></span>
<span data-ttu-id="d907c-240">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d907c-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d907c-241">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d907c-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d907c-242">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d907c-242">INPUTS</span></span>

### <span data-ttu-id="d907c-243">Keine</span><span class="sxs-lookup"><span data-stu-id="d907c-243">None</span></span>
<span data-ttu-id="d907c-244">Sie können die Eingabe an dieses Cmdlet nach Name, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="d907c-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="d907c-245">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d907c-245">OUTPUTS</span></span>

### <span data-ttu-id="d907c-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d907c-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="d907c-247">Dieses Cmdlet gibt alle Attribute eines a-4-a-Caches einschließlich primärer und sekundärer Zugriffstasten zurück.</span><span class="sxs-lookup"><span data-stu-id="d907c-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="d907c-248">Notizen</span><span class="sxs-lookup"><span data-stu-id="d907c-248">NOTES</span></span>

## <span data-ttu-id="d907c-249">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d907c-249">RELATED LINKS</span></span>

[<span data-ttu-id="d907c-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d907c-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d907c-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d907c-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="d907c-252">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d907c-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


