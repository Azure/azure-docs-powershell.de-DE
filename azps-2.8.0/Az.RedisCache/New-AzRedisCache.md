---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824204"
---
# <span data-ttu-id="9c7b1-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c7b1-101">New-AzRedisCache</span></span>

## <span data-ttu-id="9c7b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7b1-103">Erstellt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="9c7b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c7b1-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c7b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c7b1-105">DESCRIPTION</span></span>
<span data-ttu-id="9c7b1-106">Mit dem Cmdlet " **New-AzRedisCache** " wird ein Azure-Teiler-Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="9c7b1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c7b1-107">EXAMPLES</span></span>

### <span data-ttu-id="9c7b1-108">Beispiel 1: Erstellen eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="9c7b1-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="9c7b1-109">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="9c7b1-110">Beispiel 2: Erstellen eines Standard mäßigen SKUs-Caches</span><span class="sxs-lookup"><span data-stu-id="9c7b1-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="9c7b1-111">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="9c7b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c7b1-112">PARAMETERS</span></span>

### <span data-ttu-id="9c7b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7b1-113">-DefaultProfile</span></span>
<span data-ttu-id="9c7b1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c7b1-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="9c7b1-115">-EnableNonSslPort</span></span>
<span data-ttu-id="9c7b1-116">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="9c7b1-117">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="9c7b1-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="9c7b1-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="9c7b1-118">-Location</span></span>
<span data-ttu-id="9c7b1-119">Gibt den Speicherort an, an dem ein a-a/a-Cache erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="9c7b1-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9c7b1-120">Valid values are:</span></span> 
- <span data-ttu-id="9c7b1-121">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="9c7b1-121">North Central US</span></span>
- <span data-ttu-id="9c7b1-122">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="9c7b1-122">South Central US</span></span>
- <span data-ttu-id="9c7b1-123">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="9c7b1-123">Central US</span></span>
- <span data-ttu-id="9c7b1-124">West Europa</span><span class="sxs-lookup"><span data-stu-id="9c7b1-124">West Europe</span></span>
- <span data-ttu-id="9c7b1-125">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="9c7b1-125">North Europe</span></span>
- <span data-ttu-id="9c7b1-126">West-US</span><span class="sxs-lookup"><span data-stu-id="9c7b1-126">West US</span></span>
- <span data-ttu-id="9c7b1-127">East US</span><span class="sxs-lookup"><span data-stu-id="9c7b1-127">East US</span></span>
- <span data-ttu-id="9c7b1-128">East US 2</span><span class="sxs-lookup"><span data-stu-id="9c7b1-128">East US 2</span></span>
- <span data-ttu-id="9c7b1-129">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="9c7b1-129">Japan East</span></span>
- <span data-ttu-id="9c7b1-130">Japan West</span><span class="sxs-lookup"><span data-stu-id="9c7b1-130">Japan West</span></span>
- <span data-ttu-id="9c7b1-131">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="9c7b1-131">Brazil South</span></span>
- <span data-ttu-id="9c7b1-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="9c7b1-132">Southeast Asia</span></span>
- <span data-ttu-id="9c7b1-133">Ostasien</span><span class="sxs-lookup"><span data-stu-id="9c7b1-133">East Asia</span></span>
- <span data-ttu-id="9c7b1-134">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="9c7b1-134">Australia East</span></span>
- <span data-ttu-id="9c7b1-135">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="9c7b1-135">Australia Southeast</span></span>

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

### <span data-ttu-id="9c7b1-136">-Name</span><span class="sxs-lookup"><span data-stu-id="9c7b1-136">-Name</span></span>
<span data-ttu-id="9c7b1-137">Gibt den Namen des zu erstellbaren zu erstellbaren zu erstellbaren zu.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="9c7b1-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c7b1-138">-RedisConfiguration</span></span>
<span data-ttu-id="9c7b1-139">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="9c7b1-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c7b1-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c7b1-141">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="9c7b1-142">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="9c7b1-143">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-143">Premium tier only.</span></span>
- <span data-ttu-id="9c7b1-144">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="9c7b1-145">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="9c7b1-146">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-146">Premium tier only.</span></span>
- <span data-ttu-id="9c7b1-147">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="9c7b1-148">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="9c7b1-149">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-149">Premium tier only.</span></span> 
- <span data-ttu-id="9c7b1-150">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-150">maxmemory-reserved.</span></span>
<span data-ttu-id="9c7b1-151">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="9c7b1-152">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9c7b1-153">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-153">maxmemory-policy.</span></span>
<span data-ttu-id="9c7b1-154">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="9c7b1-155">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-155">All pricing tiers.</span></span> 
- <span data-ttu-id="9c7b1-156">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-156">notify-keyspace-events.</span></span>
<span data-ttu-id="9c7b1-157">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="9c7b1-158">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="9c7b1-159">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="9c7b1-160">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9c7b1-161">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9c7b1-162">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="9c7b1-163">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9c7b1-164">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9c7b1-165">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-165">set-max-intset-entries.</span></span>
<span data-ttu-id="9c7b1-166">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9c7b1-167">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9c7b1-168">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="9c7b1-169">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9c7b1-170">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9c7b1-171">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="9c7b1-172">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9c7b1-173">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9c7b1-174">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-174">databases.</span></span>
<span data-ttu-id="9c7b1-175">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-175">Configures the number of databases.</span></span>
<span data-ttu-id="9c7b1-176">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="9c7b1-177">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="9c7b1-178">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="9c7b1-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="9c7b1-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c7b1-179">-ResourceGroupName</span></span>
<span data-ttu-id="9c7b1-180">Gibt den Namen der Ressourcengruppe an, in der der "a/a-Cache" erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="9c7b1-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="9c7b1-181">-ShardCount</span></span>
<span data-ttu-id="9c7b1-182">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="9c7b1-183">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c7b1-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c7b1-184">1</span><span class="sxs-lookup"><span data-stu-id="9c7b1-184">1</span></span>
- <span data-ttu-id="9c7b1-185">2</span><span class="sxs-lookup"><span data-stu-id="9c7b1-185">2</span></span>
- <span data-ttu-id="9c7b1-186">3</span><span class="sxs-lookup"><span data-stu-id="9c7b1-186">3</span></span>
- <span data-ttu-id="9c7b1-187">4</span><span class="sxs-lookup"><span data-stu-id="9c7b1-187">4</span></span>
- <span data-ttu-id="9c7b1-188">5</span><span class="sxs-lookup"><span data-stu-id="9c7b1-188">5</span></span>
- <span data-ttu-id="9c7b1-189">6</span><span class="sxs-lookup"><span data-stu-id="9c7b1-189">6</span></span>
- <span data-ttu-id="9c7b1-190">7</span><span class="sxs-lookup"><span data-stu-id="9c7b1-190">7</span></span>
- <span data-ttu-id="9c7b1-191">8</span><span class="sxs-lookup"><span data-stu-id="9c7b1-191">8</span></span>
- <span data-ttu-id="9c7b1-192">9</span><span class="sxs-lookup"><span data-stu-id="9c7b1-192">9</span></span> 
- <span data-ttu-id="9c7b1-193">10</span><span class="sxs-lookup"><span data-stu-id="9c7b1-193">10</span></span>

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

### <span data-ttu-id="9c7b1-194">-Size</span><span class="sxs-lookup"><span data-stu-id="9c7b1-194">-Size</span></span>
<span data-ttu-id="9c7b1-195">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="9c7b1-196">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9c7b1-196">Valid values are:</span></span> 
- <span data-ttu-id="9c7b1-197">P1</span><span class="sxs-lookup"><span data-stu-id="9c7b1-197">P1</span></span>
- <span data-ttu-id="9c7b1-198">P2</span><span class="sxs-lookup"><span data-stu-id="9c7b1-198">P2</span></span>
- <span data-ttu-id="9c7b1-199">P3</span><span class="sxs-lookup"><span data-stu-id="9c7b1-199">P3</span></span>
- <span data-ttu-id="9c7b1-200">P4</span><span class="sxs-lookup"><span data-stu-id="9c7b1-200">P4</span></span>
- <span data-ttu-id="9c7b1-201">C0</span><span class="sxs-lookup"><span data-stu-id="9c7b1-201">C0</span></span>
- <span data-ttu-id="9c7b1-202">C1</span><span class="sxs-lookup"><span data-stu-id="9c7b1-202">C1</span></span>
- <span data-ttu-id="9c7b1-203">C2</span><span class="sxs-lookup"><span data-stu-id="9c7b1-203">C2</span></span>
- <span data-ttu-id="9c7b1-204">C3</span><span class="sxs-lookup"><span data-stu-id="9c7b1-204">C3</span></span>
- <span data-ttu-id="9c7b1-205">C4</span><span class="sxs-lookup"><span data-stu-id="9c7b1-205">C4</span></span>
- <span data-ttu-id="9c7b1-206">C5</span><span class="sxs-lookup"><span data-stu-id="9c7b1-206">C5</span></span>
- <span data-ttu-id="9c7b1-207">C6</span><span class="sxs-lookup"><span data-stu-id="9c7b1-207">C6</span></span>
- <span data-ttu-id="9c7b1-208">250MB</span><span class="sxs-lookup"><span data-stu-id="9c7b1-208">250MB</span></span>
- <span data-ttu-id="9c7b1-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="9c7b1-209">1GB</span></span>
- <span data-ttu-id="9c7b1-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="9c7b1-210">2.5GB</span></span>
- <span data-ttu-id="9c7b1-211">6GB</span><span class="sxs-lookup"><span data-stu-id="9c7b1-211">6GB</span></span>
- <span data-ttu-id="9c7b1-212">13GB</span><span class="sxs-lookup"><span data-stu-id="9c7b1-212">13GB</span></span>
- <span data-ttu-id="9c7b1-213">26GB</span><span class="sxs-lookup"><span data-stu-id="9c7b1-213">26GB</span></span>
- <span data-ttu-id="9c7b1-214">53GB der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="9c7b1-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="9c7b1-215">-Sku</span></span>
<span data-ttu-id="9c7b1-216">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="9c7b1-217">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9c7b1-217">Valid values are:</span></span> 
- <span data-ttu-id="9c7b1-218">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="9c7b1-218">Basic</span></span>
- <span data-ttu-id="9c7b1-219">Standard</span><span class="sxs-lookup"><span data-stu-id="9c7b1-219">Standard</span></span>
- <span data-ttu-id="9c7b1-220">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="9c7b1-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="9c7b1-221">-StaticIP</span></span>
<span data-ttu-id="9c7b1-222">Gibt eine eindeutige IP-Adresse im Subnetz für den Cache für den "a/a-Cache" an.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="9c7b1-223">Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="9c7b1-224">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="9c7b1-224">-SubnetId</span></span>
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

### <span data-ttu-id="9c7b1-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c7b1-225">-Tag</span></span>
<span data-ttu-id="9c7b1-226">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="9c7b1-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="9c7b1-227">-TenantSettings</span></span>
<span data-ttu-id="9c7b1-228">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="9c7b1-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="9c7b1-229">-Zone</span></span>
<span data-ttu-id="9c7b1-230">Liste der Zonen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-230">List of zones.</span></span>

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

### <span data-ttu-id="9c7b1-231">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c7b1-231">-Confirm</span></span>
<span data-ttu-id="9c7b1-232">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c7b1-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7b1-233">-WhatIf</span></span>
<span data-ttu-id="9c7b1-234">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c7b1-235">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c7b1-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7b1-236">CommonParameters</span></span>
<span data-ttu-id="9c7b1-237">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c7b1-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7b1-238">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c7b1-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7b1-239">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c7b1-239">INPUTS</span></span>

### <span data-ttu-id="9c7b1-240">System. String</span><span class="sxs-lookup"><span data-stu-id="9c7b1-240">System.String</span></span>

### <span data-ttu-id="9c7b1-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c7b1-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9c7b1-242">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9c7b1-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9c7b1-243">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9c7b1-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9c7b1-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="9c7b1-244">System.String[]</span></span>

## <span data-ttu-id="9c7b1-245">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c7b1-245">OUTPUTS</span></span>

### <span data-ttu-id="9c7b1-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9c7b1-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="9c7b1-247">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c7b1-247">NOTES</span></span>

## <span data-ttu-id="9c7b1-248">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c7b1-248">RELATED LINKS</span></span>

[<span data-ttu-id="9c7b1-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c7b1-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="9c7b1-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c7b1-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9c7b1-251">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c7b1-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


