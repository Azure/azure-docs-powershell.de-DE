---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481002"
---
# <span data-ttu-id="6fd4a-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd4a-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="6fd4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fd4a-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd4a-103">Erstellt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fd4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fd4a-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fd4a-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd4a-106">Mit dem Cmdlet " **New-AzureRmRedisCache** " wird ein Azure-Teiler-Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="6fd4a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fd4a-107">EXAMPLES</span></span>

### <span data-ttu-id="6fd4a-108">Beispiel 1: Erstellen eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="6fd4a-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="6fd4a-109">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="6fd4a-110">Beispiel 2: Erstellen eines Standard mäßigen SKUs-Caches</span><span class="sxs-lookup"><span data-stu-id="6fd4a-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="6fd4a-111">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="6fd4a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fd4a-112">PARAMETERS</span></span>

### <span data-ttu-id="6fd4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd4a-113">-DefaultProfile</span></span>
<span data-ttu-id="6fd4a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fd4a-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="6fd4a-115">-EnableNonSslPort</span></span>
<span data-ttu-id="6fd4a-116">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="6fd4a-117">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="6fd4a-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="6fd4a-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="6fd4a-118">-Location</span></span>
<span data-ttu-id="6fd4a-119">Gibt den Speicherort an, an dem ein a-a/a-Cache erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="6fd4a-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="6fd4a-120">Valid values are:</span></span> 

- <span data-ttu-id="6fd4a-121">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="6fd4a-121">North Central US</span></span>
- <span data-ttu-id="6fd4a-122">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="6fd4a-122">South Central US</span></span>
- <span data-ttu-id="6fd4a-123">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="6fd4a-123">Central US</span></span>
- <span data-ttu-id="6fd4a-124">West Europa</span><span class="sxs-lookup"><span data-stu-id="6fd4a-124">West Europe</span></span>
- <span data-ttu-id="6fd4a-125">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="6fd4a-125">North Europe</span></span>
- <span data-ttu-id="6fd4a-126">West-US</span><span class="sxs-lookup"><span data-stu-id="6fd4a-126">West US</span></span>
- <span data-ttu-id="6fd4a-127">East US</span><span class="sxs-lookup"><span data-stu-id="6fd4a-127">East US</span></span>
- <span data-ttu-id="6fd4a-128">East US 2</span><span class="sxs-lookup"><span data-stu-id="6fd4a-128">East US 2</span></span>
- <span data-ttu-id="6fd4a-129">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="6fd4a-129">Japan East</span></span>
- <span data-ttu-id="6fd4a-130">Japan West</span><span class="sxs-lookup"><span data-stu-id="6fd4a-130">Japan West</span></span>
- <span data-ttu-id="6fd4a-131">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="6fd4a-131">Brazil South</span></span>
- <span data-ttu-id="6fd4a-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="6fd4a-132">Southeast Asia</span></span>
- <span data-ttu-id="6fd4a-133">Ostasien</span><span class="sxs-lookup"><span data-stu-id="6fd4a-133">East Asia</span></span>
- <span data-ttu-id="6fd4a-134">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="6fd4a-134">Australia East</span></span>
- <span data-ttu-id="6fd4a-135">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="6fd4a-135">Australia Southeast</span></span>

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

### <span data-ttu-id="6fd4a-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="6fd4a-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="6fd4a-137">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="6fd4a-138">Verwenden Sie den *RedisConfiguration* -Parameter, um die maxmemory-Richtlinie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="6fd4a-139">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6fd4a-139">For example:</span></span> 

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

### <span data-ttu-id="6fd4a-140">-Name</span><span class="sxs-lookup"><span data-stu-id="6fd4a-140">-Name</span></span>
<span data-ttu-id="6fd4a-141">Gibt den Namen des zu erstellbaren zu erstellbaren zu erstellbaren zu.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="6fd4a-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fd4a-142">-RedisConfiguration</span></span>
<span data-ttu-id="6fd4a-143">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="6fd4a-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6fd4a-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6fd4a-145">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="6fd4a-146">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="6fd4a-147">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-147">Premium tier only.</span></span>
- <span data-ttu-id="6fd4a-148">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="6fd4a-149">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="6fd4a-150">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-150">Premium tier only.</span></span>
- <span data-ttu-id="6fd4a-151">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="6fd4a-152">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="6fd4a-153">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-153">Premium tier only.</span></span> 
- <span data-ttu-id="6fd4a-154">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-154">maxmemory-reserved.</span></span>
<span data-ttu-id="6fd4a-155">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="6fd4a-156">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6fd4a-157">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-157">maxmemory-policy.</span></span>
<span data-ttu-id="6fd4a-158">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="6fd4a-159">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-159">All pricing tiers.</span></span> 
- <span data-ttu-id="6fd4a-160">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-160">notify-keyspace-events.</span></span>
<span data-ttu-id="6fd4a-161">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="6fd4a-162">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="6fd4a-163">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="6fd4a-164">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6fd4a-165">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6fd4a-166">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="6fd4a-167">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6fd4a-168">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6fd4a-169">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-169">set-max-intset-entries.</span></span>
<span data-ttu-id="6fd4a-170">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6fd4a-171">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6fd4a-172">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="6fd4a-173">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6fd4a-174">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6fd4a-175">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="6fd4a-176">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6fd4a-177">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6fd4a-178">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-178">databases.</span></span>
<span data-ttu-id="6fd4a-179">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-179">Configures the number of databases.</span></span>
<span data-ttu-id="6fd4a-180">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="6fd4a-181">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="6fd4a-182">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="6fd4a-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="6fd4a-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="6fd4a-183">-RedisVersion</span></span>
<span data-ttu-id="6fd4a-184">Dieser Parameter ist veraltet und wird aus zukünftigen Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="6fd4a-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd4a-185">-ResourceGroupName</span></span>
<span data-ttu-id="6fd4a-186">Gibt den Namen der Ressourcengruppe an, in der der "a/a-Cache" erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="6fd4a-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="6fd4a-187">-ShardCount</span></span>
<span data-ttu-id="6fd4a-188">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="6fd4a-189">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6fd4a-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6fd4a-190">1</span><span class="sxs-lookup"><span data-stu-id="6fd4a-190">1</span></span>
- <span data-ttu-id="6fd4a-191">2</span><span class="sxs-lookup"><span data-stu-id="6fd4a-191">2</span></span>
- <span data-ttu-id="6fd4a-192">3</span><span class="sxs-lookup"><span data-stu-id="6fd4a-192">3</span></span>
- <span data-ttu-id="6fd4a-193">4</span><span class="sxs-lookup"><span data-stu-id="6fd4a-193">4</span></span>
- <span data-ttu-id="6fd4a-194">5</span><span class="sxs-lookup"><span data-stu-id="6fd4a-194">5</span></span>
- <span data-ttu-id="6fd4a-195">6</span><span class="sxs-lookup"><span data-stu-id="6fd4a-195">6</span></span>
- <span data-ttu-id="6fd4a-196">7</span><span class="sxs-lookup"><span data-stu-id="6fd4a-196">7</span></span>
- <span data-ttu-id="6fd4a-197">8</span><span class="sxs-lookup"><span data-stu-id="6fd4a-197">8</span></span>
- <span data-ttu-id="6fd4a-198">9</span><span class="sxs-lookup"><span data-stu-id="6fd4a-198">9</span></span> 
- <span data-ttu-id="6fd4a-199">10</span><span class="sxs-lookup"><span data-stu-id="6fd4a-199">10</span></span>

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

### <span data-ttu-id="6fd4a-200">-Size</span><span class="sxs-lookup"><span data-stu-id="6fd4a-200">-Size</span></span>
<span data-ttu-id="6fd4a-201">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="6fd4a-202">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="6fd4a-202">Valid values are:</span></span> 

- <span data-ttu-id="6fd4a-203">P1</span><span class="sxs-lookup"><span data-stu-id="6fd4a-203">P1</span></span>
- <span data-ttu-id="6fd4a-204">P2</span><span class="sxs-lookup"><span data-stu-id="6fd4a-204">P2</span></span>
- <span data-ttu-id="6fd4a-205">P3</span><span class="sxs-lookup"><span data-stu-id="6fd4a-205">P3</span></span>
- <span data-ttu-id="6fd4a-206">P4</span><span class="sxs-lookup"><span data-stu-id="6fd4a-206">P4</span></span>
- <span data-ttu-id="6fd4a-207">C0</span><span class="sxs-lookup"><span data-stu-id="6fd4a-207">C0</span></span>
- <span data-ttu-id="6fd4a-208">C1</span><span class="sxs-lookup"><span data-stu-id="6fd4a-208">C1</span></span>
- <span data-ttu-id="6fd4a-209">C2</span><span class="sxs-lookup"><span data-stu-id="6fd4a-209">C2</span></span>
- <span data-ttu-id="6fd4a-210">C3</span><span class="sxs-lookup"><span data-stu-id="6fd4a-210">C3</span></span>
- <span data-ttu-id="6fd4a-211">C4</span><span class="sxs-lookup"><span data-stu-id="6fd4a-211">C4</span></span>
- <span data-ttu-id="6fd4a-212">C5</span><span class="sxs-lookup"><span data-stu-id="6fd4a-212">C5</span></span>
- <span data-ttu-id="6fd4a-213">C6</span><span class="sxs-lookup"><span data-stu-id="6fd4a-213">C6</span></span>
- <span data-ttu-id="6fd4a-214">250MB</span><span class="sxs-lookup"><span data-stu-id="6fd4a-214">250MB</span></span>
- <span data-ttu-id="6fd4a-215">1 GB</span><span class="sxs-lookup"><span data-stu-id="6fd4a-215">1GB</span></span>
- <span data-ttu-id="6fd4a-216">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="6fd4a-216">2.5GB</span></span>
- <span data-ttu-id="6fd4a-217">6GB</span><span class="sxs-lookup"><span data-stu-id="6fd4a-217">6GB</span></span>
- <span data-ttu-id="6fd4a-218">13GB</span><span class="sxs-lookup"><span data-stu-id="6fd4a-218">13GB</span></span>
- <span data-ttu-id="6fd4a-219">26GB</span><span class="sxs-lookup"><span data-stu-id="6fd4a-219">26GB</span></span>
- <span data-ttu-id="6fd4a-220">53GB</span><span class="sxs-lookup"><span data-stu-id="6fd4a-220">53GB</span></span>

<span data-ttu-id="6fd4a-221">Der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="6fd4a-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="6fd4a-222">-Sku</span></span>
<span data-ttu-id="6fd4a-223">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="6fd4a-224">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="6fd4a-224">Valid values are:</span></span> 

- <span data-ttu-id="6fd4a-225">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="6fd4a-225">Basic</span></span>
- <span data-ttu-id="6fd4a-226">Standard</span><span class="sxs-lookup"><span data-stu-id="6fd4a-226">Standard</span></span>
- <span data-ttu-id="6fd4a-227">Premium</span><span class="sxs-lookup"><span data-stu-id="6fd4a-227">Premium</span></span>

<span data-ttu-id="6fd4a-228">Der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="6fd4a-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="6fd4a-229">-StaticIP</span></span>
<span data-ttu-id="6fd4a-230">Gibt eine eindeutige IP-Adresse im Subnetz für den Cache für den "a/a-Cache" an.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="6fd4a-231">Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="6fd4a-232">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="6fd4a-232">-Subnet</span></span>
<span data-ttu-id="6fd4a-233">Gibt den Namen des Subnets an, in dem der "a-Cache" bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="6fd4a-234">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="6fd4a-234">-SubnetId</span></span>
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

### <span data-ttu-id="6fd4a-235">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fd4a-235">-Tag</span></span>
<span data-ttu-id="6fd4a-236">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="6fd4a-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="6fd4a-237">-TenantSettings</span></span>
<span data-ttu-id="6fd4a-238">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="6fd4a-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6fd4a-239">-VirtualNetwork</span></span>
<span data-ttu-id="6fd4a-240">Gibt die Ressourcen-ID des virtuellen Netzwerks an, in dem der "a-Cache" bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="6fd4a-241">-Zone</span><span class="sxs-lookup"><span data-stu-id="6fd4a-241">-Zone</span></span>
<span data-ttu-id="6fd4a-242">Liste der Zonen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd4a-243">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fd4a-243">-Confirm</span></span>
<span data-ttu-id="6fd4a-244">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd4a-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd4a-245">-WhatIf</span></span>
<span data-ttu-id="6fd4a-246">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fd4a-247">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd4a-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd4a-248">CommonParameters</span></span>
<span data-ttu-id="6fd4a-249">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd4a-250">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd4a-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd4a-251">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fd4a-251">INPUTS</span></span>

### <span data-ttu-id="6fd4a-252">Keine</span><span class="sxs-lookup"><span data-stu-id="6fd4a-252">None</span></span>
<span data-ttu-id="6fd4a-253">Sie können die Eingabe an dieses Cmdlet nach Name, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="6fd4a-254">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fd4a-254">OUTPUTS</span></span>

### <span data-ttu-id="6fd4a-255">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6fd4a-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="6fd4a-256">Dieses Cmdlet gibt alle Attribute eines a-4-a-Caches einschließlich primärer und sekundärer Zugriffstasten zurück.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="6fd4a-257">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fd4a-257">NOTES</span></span>

## <span data-ttu-id="6fd4a-258">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fd4a-258">RELATED LINKS</span></span>

[<span data-ttu-id="6fd4a-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd4a-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="6fd4a-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd4a-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6fd4a-261">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd4a-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


