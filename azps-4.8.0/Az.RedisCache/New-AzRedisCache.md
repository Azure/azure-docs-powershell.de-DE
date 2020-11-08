---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007883"
---
# <span data-ttu-id="183a9-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="183a9-101">New-AzRedisCache</span></span>

## <span data-ttu-id="183a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="183a9-102">SYNOPSIS</span></span>
<span data-ttu-id="183a9-103">Erstellt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="183a9-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="183a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="183a9-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="183a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="183a9-105">DESCRIPTION</span></span>
<span data-ttu-id="183a9-106">Mit dem Cmdlet " **New-AzRedisCache** " wird ein Azure-Teiler-Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="183a9-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="183a9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="183a9-107">EXAMPLES</span></span>

### <span data-ttu-id="183a9-108">Beispiel 1: Erstellen eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="183a9-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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

<span data-ttu-id="183a9-109">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="183a9-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="183a9-110">Beispiel 2: Erstellen eines Standard mäßigen SKUs-Caches</span><span class="sxs-lookup"><span data-stu-id="183a9-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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

<span data-ttu-id="183a9-111">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="183a9-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="183a9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="183a9-112">PARAMETERS</span></span>

### <span data-ttu-id="183a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183a9-113">-DefaultProfile</span></span>
<span data-ttu-id="183a9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="183a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="183a9-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="183a9-115">-EnableNonSslPort</span></span>
<span data-ttu-id="183a9-116">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="183a9-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="183a9-117">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="183a9-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="183a9-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="183a9-118">-Location</span></span>
<span data-ttu-id="183a9-119">Gibt den Speicherort an, an dem ein a-a/a-Cache erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="183a9-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="183a9-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="183a9-120">Valid values are:</span></span> 
- <span data-ttu-id="183a9-121">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="183a9-121">North Central US</span></span>
- <span data-ttu-id="183a9-122">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="183a9-122">South Central US</span></span>
- <span data-ttu-id="183a9-123">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="183a9-123">Central US</span></span>
- <span data-ttu-id="183a9-124">West Europa</span><span class="sxs-lookup"><span data-stu-id="183a9-124">West Europe</span></span>
- <span data-ttu-id="183a9-125">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="183a9-125">North Europe</span></span>
- <span data-ttu-id="183a9-126">West-US</span><span class="sxs-lookup"><span data-stu-id="183a9-126">West US</span></span>
- <span data-ttu-id="183a9-127">East US</span><span class="sxs-lookup"><span data-stu-id="183a9-127">East US</span></span>
- <span data-ttu-id="183a9-128">East US 2</span><span class="sxs-lookup"><span data-stu-id="183a9-128">East US 2</span></span>
- <span data-ttu-id="183a9-129">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="183a9-129">Japan East</span></span>
- <span data-ttu-id="183a9-130">Japan West</span><span class="sxs-lookup"><span data-stu-id="183a9-130">Japan West</span></span>
- <span data-ttu-id="183a9-131">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="183a9-131">Brazil South</span></span>
- <span data-ttu-id="183a9-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="183a9-132">Southeast Asia</span></span>
- <span data-ttu-id="183a9-133">Ostasien</span><span class="sxs-lookup"><span data-stu-id="183a9-133">East Asia</span></span>
- <span data-ttu-id="183a9-134">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="183a9-134">Australia East</span></span>
- <span data-ttu-id="183a9-135">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="183a9-135">Australia Southeast</span></span>

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

### <span data-ttu-id="183a9-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="183a9-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="183a9-137">Geben Sie die TLS-Version an, die von Clients zum Herstellen einer Verbindung mit dem Cache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="183a9-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="183a9-138">-Name</span><span class="sxs-lookup"><span data-stu-id="183a9-138">-Name</span></span>
<span data-ttu-id="183a9-139">Gibt den Namen des zu erstellbaren zu erstellbaren zu erstellbaren zu.</span><span class="sxs-lookup"><span data-stu-id="183a9-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="183a9-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="183a9-140">-RedisConfiguration</span></span>
<span data-ttu-id="183a9-141">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="183a9-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="183a9-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="183a9-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="183a9-143">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="183a9-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="183a9-144">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="183a9-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="183a9-145">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="183a9-145">Premium tier only.</span></span>
- <span data-ttu-id="183a9-146">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="183a9-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="183a9-147">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="183a9-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="183a9-148">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="183a9-148">Premium tier only.</span></span>
- <span data-ttu-id="183a9-149">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="183a9-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="183a9-150">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="183a9-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="183a9-151">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="183a9-151">Premium tier only.</span></span> 
- <span data-ttu-id="183a9-152">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="183a9-152">maxmemory-reserved.</span></span>
<span data-ttu-id="183a9-153">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="183a9-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="183a9-154">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="183a9-155">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="183a9-155">maxmemory-policy.</span></span>
<span data-ttu-id="183a9-156">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="183a9-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="183a9-157">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-157">All pricing tiers.</span></span> 
- <span data-ttu-id="183a9-158">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="183a9-158">notify-keyspace-events.</span></span>
<span data-ttu-id="183a9-159">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="183a9-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="183a9-160">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="183a9-161">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="183a9-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="183a9-162">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="183a9-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="183a9-163">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="183a9-164">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="183a9-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="183a9-165">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="183a9-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="183a9-166">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="183a9-167">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="183a9-167">set-max-intset-entries.</span></span>
<span data-ttu-id="183a9-168">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="183a9-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="183a9-169">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="183a9-170">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="183a9-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="183a9-171">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="183a9-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="183a9-172">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="183a9-173">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="183a9-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="183a9-174">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="183a9-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="183a9-175">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="183a9-176">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="183a9-176">databases.</span></span>
<span data-ttu-id="183a9-177">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="183a9-177">Configures the number of databases.</span></span>
<span data-ttu-id="183a9-178">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="183a9-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="183a9-179">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="183a9-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="183a9-180">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="183a9-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="183a9-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="183a9-181">-ResourceGroupName</span></span>
<span data-ttu-id="183a9-182">Gibt den Namen der Ressourcengruppe an, in der der "a/a-Cache" erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="183a9-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="183a9-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="183a9-183">-ShardCount</span></span>
<span data-ttu-id="183a9-184">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="183a9-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="183a9-185">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="183a9-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="183a9-186">1</span><span class="sxs-lookup"><span data-stu-id="183a9-186">1</span></span>
- <span data-ttu-id="183a9-187">2</span><span class="sxs-lookup"><span data-stu-id="183a9-187">2</span></span>
- <span data-ttu-id="183a9-188">3</span><span class="sxs-lookup"><span data-stu-id="183a9-188">3</span></span>
- <span data-ttu-id="183a9-189">4</span><span class="sxs-lookup"><span data-stu-id="183a9-189">4</span></span>
- <span data-ttu-id="183a9-190">5</span><span class="sxs-lookup"><span data-stu-id="183a9-190">5</span></span>
- <span data-ttu-id="183a9-191">6</span><span class="sxs-lookup"><span data-stu-id="183a9-191">6</span></span>
- <span data-ttu-id="183a9-192">7</span><span class="sxs-lookup"><span data-stu-id="183a9-192">7</span></span>
- <span data-ttu-id="183a9-193">8</span><span class="sxs-lookup"><span data-stu-id="183a9-193">8</span></span>
- <span data-ttu-id="183a9-194">9</span><span class="sxs-lookup"><span data-stu-id="183a9-194">9</span></span> 
- <span data-ttu-id="183a9-195">10</span><span class="sxs-lookup"><span data-stu-id="183a9-195">10</span></span>

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

### <span data-ttu-id="183a9-196">-Size</span><span class="sxs-lookup"><span data-stu-id="183a9-196">-Size</span></span>
<span data-ttu-id="183a9-197">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="183a9-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="183a9-198">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="183a9-198">Valid values are:</span></span> 
- <span data-ttu-id="183a9-199">P1</span><span class="sxs-lookup"><span data-stu-id="183a9-199">P1</span></span>
- <span data-ttu-id="183a9-200">P2</span><span class="sxs-lookup"><span data-stu-id="183a9-200">P2</span></span>
- <span data-ttu-id="183a9-201">P3</span><span class="sxs-lookup"><span data-stu-id="183a9-201">P3</span></span>
- <span data-ttu-id="183a9-202">P4</span><span class="sxs-lookup"><span data-stu-id="183a9-202">P4</span></span>
- <span data-ttu-id="183a9-203">P5</span><span class="sxs-lookup"><span data-stu-id="183a9-203">P5</span></span>
- <span data-ttu-id="183a9-204">C0</span><span class="sxs-lookup"><span data-stu-id="183a9-204">C0</span></span>
- <span data-ttu-id="183a9-205">C1</span><span class="sxs-lookup"><span data-stu-id="183a9-205">C1</span></span>
- <span data-ttu-id="183a9-206">C2</span><span class="sxs-lookup"><span data-stu-id="183a9-206">C2</span></span>
- <span data-ttu-id="183a9-207">C3</span><span class="sxs-lookup"><span data-stu-id="183a9-207">C3</span></span>
- <span data-ttu-id="183a9-208">C4</span><span class="sxs-lookup"><span data-stu-id="183a9-208">C4</span></span>
- <span data-ttu-id="183a9-209">C5</span><span class="sxs-lookup"><span data-stu-id="183a9-209">C5</span></span>
- <span data-ttu-id="183a9-210">C6</span><span class="sxs-lookup"><span data-stu-id="183a9-210">C6</span></span>
- <span data-ttu-id="183a9-211">250MB</span><span class="sxs-lookup"><span data-stu-id="183a9-211">250MB</span></span>
- <span data-ttu-id="183a9-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="183a9-212">1GB</span></span>
- <span data-ttu-id="183a9-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="183a9-213">2.5GB</span></span>
- <span data-ttu-id="183a9-214">6GB</span><span class="sxs-lookup"><span data-stu-id="183a9-214">6GB</span></span>
- <span data-ttu-id="183a9-215">13GB</span><span class="sxs-lookup"><span data-stu-id="183a9-215">13GB</span></span>
- <span data-ttu-id="183a9-216">26GB</span><span class="sxs-lookup"><span data-stu-id="183a9-216">26GB</span></span>
- <span data-ttu-id="183a9-217">53GB der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="183a9-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="183a9-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="183a9-218">-Sku</span></span>
<span data-ttu-id="183a9-219">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="183a9-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="183a9-220">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="183a9-220">Valid values are:</span></span> 
- <span data-ttu-id="183a9-221">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="183a9-221">Basic</span></span>
- <span data-ttu-id="183a9-222">Standard</span><span class="sxs-lookup"><span data-stu-id="183a9-222">Standard</span></span>
- <span data-ttu-id="183a9-223">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="183a9-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="183a9-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="183a9-224">-StaticIP</span></span>
<span data-ttu-id="183a9-225">Gibt eine eindeutige IP-Adresse im Subnetz für den Cache für den "a/a-Cache" an.</span><span class="sxs-lookup"><span data-stu-id="183a9-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="183a9-226">Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.</span><span class="sxs-lookup"><span data-stu-id="183a9-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="183a9-227">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="183a9-227">-SubnetId</span></span>
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

### <span data-ttu-id="183a9-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="183a9-228">-Tag</span></span>
<span data-ttu-id="183a9-229">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="183a9-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="183a9-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="183a9-230">-TenantSettings</span></span>
<span data-ttu-id="183a9-231">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="183a9-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="183a9-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="183a9-232">-Zone</span></span>
<span data-ttu-id="183a9-233">Liste der Zonen.</span><span class="sxs-lookup"><span data-stu-id="183a9-233">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183a9-234">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="183a9-234">-Confirm</span></span>
<span data-ttu-id="183a9-235">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="183a9-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="183a9-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="183a9-236">-WhatIf</span></span>
<span data-ttu-id="183a9-237">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="183a9-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="183a9-238">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="183a9-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="183a9-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183a9-239">CommonParameters</span></span>
<span data-ttu-id="183a9-240">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="183a9-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183a9-241">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="183a9-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183a9-242">Eingaben</span><span class="sxs-lookup"><span data-stu-id="183a9-242">INPUTS</span></span>

### <span data-ttu-id="183a9-243">System. String</span><span class="sxs-lookup"><span data-stu-id="183a9-243">System.String</span></span>

### <span data-ttu-id="183a9-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="183a9-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="183a9-245">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="183a9-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="183a9-246">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="183a9-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="183a9-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="183a9-247">System.String[]</span></span>

## <span data-ttu-id="183a9-248">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="183a9-248">OUTPUTS</span></span>

### <span data-ttu-id="183a9-249">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="183a9-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="183a9-250">Notizen</span><span class="sxs-lookup"><span data-stu-id="183a9-250">NOTES</span></span>

## <span data-ttu-id="183a9-251">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="183a9-251">RELATED LINKS</span></span>

[<span data-ttu-id="183a9-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="183a9-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="183a9-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="183a9-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="183a9-254">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="183a9-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


