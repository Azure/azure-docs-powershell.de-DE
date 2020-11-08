---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178683"
---
# <span data-ttu-id="af0b1-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af0b1-101">New-AzRedisCache</span></span>

## <span data-ttu-id="af0b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="af0b1-103">Erstellt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="af0b1-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="af0b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af0b1-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af0b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af0b1-105">DESCRIPTION</span></span>
<span data-ttu-id="af0b1-106">Mit dem Cmdlet " **New-AzRedisCache** " wird ein Azure-Teiler-Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="af0b1-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="af0b1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af0b1-107">EXAMPLES</span></span>

### <span data-ttu-id="af0b1-108">Beispiel 1: Erstellen eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="af0b1-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="af0b1-109">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="af0b1-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="af0b1-110">Beispiel 2: Erstellen eines Standard mäßigen SKUs-Caches</span><span class="sxs-lookup"><span data-stu-id="af0b1-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="af0b1-111">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="af0b1-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="af0b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="af0b1-112">PARAMETERS</span></span>

### <span data-ttu-id="af0b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af0b1-113">-DefaultProfile</span></span>
<span data-ttu-id="af0b1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af0b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af0b1-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="af0b1-115">-EnableNonSslPort</span></span>
<span data-ttu-id="af0b1-116">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="af0b1-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="af0b1-117">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="af0b1-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="af0b1-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="af0b1-118">-Location</span></span>
<span data-ttu-id="af0b1-119">Gibt den Speicherort an, an dem ein a-a/a-Cache erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="af0b1-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="af0b1-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="af0b1-120">Valid values are:</span></span> 
- <span data-ttu-id="af0b1-121">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="af0b1-121">North Central US</span></span>
- <span data-ttu-id="af0b1-122">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="af0b1-122">South Central US</span></span>
- <span data-ttu-id="af0b1-123">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="af0b1-123">Central US</span></span>
- <span data-ttu-id="af0b1-124">West Europa</span><span class="sxs-lookup"><span data-stu-id="af0b1-124">West Europe</span></span>
- <span data-ttu-id="af0b1-125">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="af0b1-125">North Europe</span></span>
- <span data-ttu-id="af0b1-126">West-US</span><span class="sxs-lookup"><span data-stu-id="af0b1-126">West US</span></span>
- <span data-ttu-id="af0b1-127">East US</span><span class="sxs-lookup"><span data-stu-id="af0b1-127">East US</span></span>
- <span data-ttu-id="af0b1-128">East US 2</span><span class="sxs-lookup"><span data-stu-id="af0b1-128">East US 2</span></span>
- <span data-ttu-id="af0b1-129">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="af0b1-129">Japan East</span></span>
- <span data-ttu-id="af0b1-130">Japan West</span><span class="sxs-lookup"><span data-stu-id="af0b1-130">Japan West</span></span>
- <span data-ttu-id="af0b1-131">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="af0b1-131">Brazil South</span></span>
- <span data-ttu-id="af0b1-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="af0b1-132">Southeast Asia</span></span>
- <span data-ttu-id="af0b1-133">Ostasien</span><span class="sxs-lookup"><span data-stu-id="af0b1-133">East Asia</span></span>
- <span data-ttu-id="af0b1-134">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="af0b1-134">Australia East</span></span>
- <span data-ttu-id="af0b1-135">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="af0b1-135">Australia Southeast</span></span>

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

### <span data-ttu-id="af0b1-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="af0b1-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="af0b1-137">Geben Sie die TLS-Version an, die von Clients zum Herstellen einer Verbindung mit dem Cache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="af0b1-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="af0b1-138">-Name</span><span class="sxs-lookup"><span data-stu-id="af0b1-138">-Name</span></span>
<span data-ttu-id="af0b1-139">Gibt den Namen des zu erstellbaren zu erstellbaren zu erstellbaren zu.</span><span class="sxs-lookup"><span data-stu-id="af0b1-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="af0b1-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="af0b1-140">-RedisConfiguration</span></span>
<span data-ttu-id="af0b1-141">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="af0b1-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="af0b1-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="af0b1-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af0b1-143">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af0b1-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="af0b1-144">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="af0b1-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="af0b1-145">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="af0b1-145">Premium tier only.</span></span>
- <span data-ttu-id="af0b1-146">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="af0b1-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="af0b1-147">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="af0b1-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="af0b1-148">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="af0b1-148">Premium tier only.</span></span>
- <span data-ttu-id="af0b1-149">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="af0b1-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="af0b1-150">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="af0b1-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="af0b1-151">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="af0b1-151">Premium tier only.</span></span> 
- <span data-ttu-id="af0b1-152">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="af0b1-152">maxmemory-reserved.</span></span>
<span data-ttu-id="af0b1-153">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="af0b1-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="af0b1-154">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="af0b1-155">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="af0b1-155">maxmemory-policy.</span></span>
<span data-ttu-id="af0b1-156">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="af0b1-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="af0b1-157">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-157">All pricing tiers.</span></span> 
- <span data-ttu-id="af0b1-158">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="af0b1-158">notify-keyspace-events.</span></span>
<span data-ttu-id="af0b1-159">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="af0b1-160">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="af0b1-161">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="af0b1-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="af0b1-162">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="af0b1-163">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="af0b1-164">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="af0b1-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="af0b1-165">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="af0b1-166">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="af0b1-167">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="af0b1-167">set-max-intset-entries.</span></span>
<span data-ttu-id="af0b1-168">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="af0b1-169">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="af0b1-170">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="af0b1-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="af0b1-171">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="af0b1-172">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="af0b1-173">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="af0b1-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="af0b1-174">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="af0b1-175">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="af0b1-176">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="af0b1-176">databases.</span></span>
<span data-ttu-id="af0b1-177">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="af0b1-177">Configures the number of databases.</span></span>
<span data-ttu-id="af0b1-178">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="af0b1-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="af0b1-179">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="af0b1-180">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="af0b1-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="af0b1-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af0b1-181">-ResourceGroupName</span></span>
<span data-ttu-id="af0b1-182">Gibt den Namen der Ressourcengruppe an, in der der "a/a-Cache" erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="af0b1-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="af0b1-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="af0b1-183">-ShardCount</span></span>
<span data-ttu-id="af0b1-184">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="af0b1-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="af0b1-185">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="af0b1-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af0b1-186">1</span><span class="sxs-lookup"><span data-stu-id="af0b1-186">1</span></span>
- <span data-ttu-id="af0b1-187">2</span><span class="sxs-lookup"><span data-stu-id="af0b1-187">2</span></span>
- <span data-ttu-id="af0b1-188">3</span><span class="sxs-lookup"><span data-stu-id="af0b1-188">3</span></span>
- <span data-ttu-id="af0b1-189">4</span><span class="sxs-lookup"><span data-stu-id="af0b1-189">4</span></span>
- <span data-ttu-id="af0b1-190">5</span><span class="sxs-lookup"><span data-stu-id="af0b1-190">5</span></span>
- <span data-ttu-id="af0b1-191">6</span><span class="sxs-lookup"><span data-stu-id="af0b1-191">6</span></span>
- <span data-ttu-id="af0b1-192">7</span><span class="sxs-lookup"><span data-stu-id="af0b1-192">7</span></span>
- <span data-ttu-id="af0b1-193">8</span><span class="sxs-lookup"><span data-stu-id="af0b1-193">8</span></span>
- <span data-ttu-id="af0b1-194">9</span><span class="sxs-lookup"><span data-stu-id="af0b1-194">9</span></span> 
- <span data-ttu-id="af0b1-195">10</span><span class="sxs-lookup"><span data-stu-id="af0b1-195">10</span></span>

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

### <span data-ttu-id="af0b1-196">-Size</span><span class="sxs-lookup"><span data-stu-id="af0b1-196">-Size</span></span>
<span data-ttu-id="af0b1-197">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="af0b1-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="af0b1-198">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="af0b1-198">Valid values are:</span></span> 
- <span data-ttu-id="af0b1-199">P1</span><span class="sxs-lookup"><span data-stu-id="af0b1-199">P1</span></span>
- <span data-ttu-id="af0b1-200">P2</span><span class="sxs-lookup"><span data-stu-id="af0b1-200">P2</span></span>
- <span data-ttu-id="af0b1-201">P3</span><span class="sxs-lookup"><span data-stu-id="af0b1-201">P3</span></span>
- <span data-ttu-id="af0b1-202">P4</span><span class="sxs-lookup"><span data-stu-id="af0b1-202">P4</span></span>
- <span data-ttu-id="af0b1-203">P5</span><span class="sxs-lookup"><span data-stu-id="af0b1-203">P5</span></span>
- <span data-ttu-id="af0b1-204">C0</span><span class="sxs-lookup"><span data-stu-id="af0b1-204">C0</span></span>
- <span data-ttu-id="af0b1-205">C1</span><span class="sxs-lookup"><span data-stu-id="af0b1-205">C1</span></span>
- <span data-ttu-id="af0b1-206">C2</span><span class="sxs-lookup"><span data-stu-id="af0b1-206">C2</span></span>
- <span data-ttu-id="af0b1-207">C3</span><span class="sxs-lookup"><span data-stu-id="af0b1-207">C3</span></span>
- <span data-ttu-id="af0b1-208">C4</span><span class="sxs-lookup"><span data-stu-id="af0b1-208">C4</span></span>
- <span data-ttu-id="af0b1-209">C5</span><span class="sxs-lookup"><span data-stu-id="af0b1-209">C5</span></span>
- <span data-ttu-id="af0b1-210">C6</span><span class="sxs-lookup"><span data-stu-id="af0b1-210">C6</span></span>
- <span data-ttu-id="af0b1-211">250MB</span><span class="sxs-lookup"><span data-stu-id="af0b1-211">250MB</span></span>
- <span data-ttu-id="af0b1-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="af0b1-212">1GB</span></span>
- <span data-ttu-id="af0b1-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="af0b1-213">2.5GB</span></span>
- <span data-ttu-id="af0b1-214">6GB</span><span class="sxs-lookup"><span data-stu-id="af0b1-214">6GB</span></span>
- <span data-ttu-id="af0b1-215">13GB</span><span class="sxs-lookup"><span data-stu-id="af0b1-215">13GB</span></span>
- <span data-ttu-id="af0b1-216">26GB</span><span class="sxs-lookup"><span data-stu-id="af0b1-216">26GB</span></span>
- <span data-ttu-id="af0b1-217">53GB der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="af0b1-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="af0b1-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="af0b1-218">-Sku</span></span>
<span data-ttu-id="af0b1-219">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="af0b1-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="af0b1-220">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="af0b1-220">Valid values are:</span></span> 
- <span data-ttu-id="af0b1-221">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="af0b1-221">Basic</span></span>
- <span data-ttu-id="af0b1-222">Standard</span><span class="sxs-lookup"><span data-stu-id="af0b1-222">Standard</span></span>
- <span data-ttu-id="af0b1-223">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="af0b1-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="af0b1-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="af0b1-224">-StaticIP</span></span>
<span data-ttu-id="af0b1-225">Gibt eine eindeutige IP-Adresse im Subnetz für den Cache für den "a/a-Cache" an.</span><span class="sxs-lookup"><span data-stu-id="af0b1-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="af0b1-226">Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.</span><span class="sxs-lookup"><span data-stu-id="af0b1-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="af0b1-227">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="af0b1-227">-SubnetId</span></span>
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

### <span data-ttu-id="af0b1-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="af0b1-228">-Tag</span></span>
<span data-ttu-id="af0b1-229">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="af0b1-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="af0b1-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="af0b1-230">-TenantSettings</span></span>
<span data-ttu-id="af0b1-231">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="af0b1-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="af0b1-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="af0b1-232">-Zone</span></span>
<span data-ttu-id="af0b1-233">Liste der Zonen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-233">List of zones.</span></span>

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

### <span data-ttu-id="af0b1-234">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af0b1-234">-Confirm</span></span>
<span data-ttu-id="af0b1-235">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af0b1-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af0b1-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af0b1-236">-WhatIf</span></span>
<span data-ttu-id="af0b1-237">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af0b1-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af0b1-238">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af0b1-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af0b1-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af0b1-239">CommonParameters</span></span>
<span data-ttu-id="af0b1-240">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af0b1-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af0b1-241">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af0b1-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af0b1-242">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af0b1-242">INPUTS</span></span>

### <span data-ttu-id="af0b1-243">System. String</span><span class="sxs-lookup"><span data-stu-id="af0b1-243">System.String</span></span>

### <span data-ttu-id="af0b1-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="af0b1-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="af0b1-245">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af0b1-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af0b1-246">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af0b1-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af0b1-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="af0b1-247">System.String[]</span></span>

## <span data-ttu-id="af0b1-248">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af0b1-248">OUTPUTS</span></span>

### <span data-ttu-id="af0b1-249">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="af0b1-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="af0b1-250">Notizen</span><span class="sxs-lookup"><span data-stu-id="af0b1-250">NOTES</span></span>

## <span data-ttu-id="af0b1-251">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af0b1-251">RELATED LINKS</span></span>

[<span data-ttu-id="af0b1-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af0b1-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="af0b1-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af0b1-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="af0b1-254">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af0b1-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


