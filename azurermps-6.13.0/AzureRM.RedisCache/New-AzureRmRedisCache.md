---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 6b2239e09a35ada6b756e58cf2c3a09ed891e730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663647"
---
# <span data-ttu-id="d2740-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2740-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="d2740-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2740-102">SYNOPSIS</span></span>
<span data-ttu-id="d2740-103">Erstellt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="d2740-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2740-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2740-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>]
 [-Sku <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2740-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2740-105">DESCRIPTION</span></span>
<span data-ttu-id="d2740-106">Mit dem Cmdlet " **New-AzureRmRedisCache** " wird ein Azure-Teiler-Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2740-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="d2740-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2740-107">EXAMPLES</span></span>

### <span data-ttu-id="d2740-108">Beispiel 1: Erstellen eines Zeichenfolgen-Caches</span><span class="sxs-lookup"><span data-stu-id="d2740-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="d2740-109">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2740-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="d2740-110">Beispiel 2: Erstellen eines Standard mäßigen SKUs-Caches</span><span class="sxs-lookup"><span data-stu-id="d2740-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="d2740-111">Mit diesem Befehl wird ein Zwischenspeicher mit einem anderen Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2740-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="d2740-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2740-112">PARAMETERS</span></span>

### <span data-ttu-id="d2740-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2740-113">-DefaultProfile</span></span>
<span data-ttu-id="d2740-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2740-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2740-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="d2740-115">-EnableNonSslPort</span></span>
<span data-ttu-id="d2740-116">Gibt an, ob der nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d2740-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="d2740-117">Der Standardwert ist $false (der nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="d2740-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="d2740-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="d2740-118">-Location</span></span>
<span data-ttu-id="d2740-119">Gibt den Speicherort an, an dem ein a-a/a-Cache erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2740-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="d2740-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d2740-120">Valid values are:</span></span> 
- <span data-ttu-id="d2740-121">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="d2740-121">North Central US</span></span>
- <span data-ttu-id="d2740-122">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="d2740-122">South Central US</span></span>
- <span data-ttu-id="d2740-123">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="d2740-123">Central US</span></span>
- <span data-ttu-id="d2740-124">West Europa</span><span class="sxs-lookup"><span data-stu-id="d2740-124">West Europe</span></span>
- <span data-ttu-id="d2740-125">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="d2740-125">North Europe</span></span>
- <span data-ttu-id="d2740-126">West-US</span><span class="sxs-lookup"><span data-stu-id="d2740-126">West US</span></span>
- <span data-ttu-id="d2740-127">East US</span><span class="sxs-lookup"><span data-stu-id="d2740-127">East US</span></span>
- <span data-ttu-id="d2740-128">East US 2</span><span class="sxs-lookup"><span data-stu-id="d2740-128">East US 2</span></span>
- <span data-ttu-id="d2740-129">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="d2740-129">Japan East</span></span>
- <span data-ttu-id="d2740-130">Japan West</span><span class="sxs-lookup"><span data-stu-id="d2740-130">Japan West</span></span>
- <span data-ttu-id="d2740-131">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="d2740-131">Brazil South</span></span>
- <span data-ttu-id="d2740-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="d2740-132">Southeast Asia</span></span>
- <span data-ttu-id="d2740-133">Ostasien</span><span class="sxs-lookup"><span data-stu-id="d2740-133">East Asia</span></span>
- <span data-ttu-id="d2740-134">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="d2740-134">Australia East</span></span>
- <span data-ttu-id="d2740-135">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="d2740-135">Australia Southeast</span></span>

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

### <span data-ttu-id="d2740-136">-Name</span><span class="sxs-lookup"><span data-stu-id="d2740-136">-Name</span></span>
<span data-ttu-id="d2740-137">Gibt den Namen des zu erstellbaren zu erstellbaren zu erstellbaren zu.</span><span class="sxs-lookup"><span data-stu-id="d2740-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="d2740-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2740-138">-RedisConfiguration</span></span>
<span data-ttu-id="d2740-139">Gibt die Einstellungen für die Einstellungen für die Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d2740-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="d2740-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d2740-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2740-141">RDB – Backup-aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d2740-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="d2740-142">Gibt an, dass die Dauerhaftigkeit der Datenpersistenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d2740-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="d2740-143">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="d2740-143">Premium tier only.</span></span>
- <span data-ttu-id="d2740-144">RDB-Speicher-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d2740-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="d2740-145">Gibt die Verbindungszeichenfolge für das Speicherkonto für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="d2740-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="d2740-146">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="d2740-146">Premium tier only.</span></span>
- <span data-ttu-id="d2740-147">RDB-Backup-Frequency.</span><span class="sxs-lookup"><span data-stu-id="d2740-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="d2740-148">Gibt die Sicherungshäufigkeit für die Dauerhaftigkeit von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="d2740-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="d2740-149">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="d2740-149">Premium tier only.</span></span> 
- <span data-ttu-id="d2740-150">maxmemory-reserviert.</span><span class="sxs-lookup"><span data-stu-id="d2740-150">maxmemory-reserved.</span></span>
<span data-ttu-id="d2740-151">Konfiguriert den für nicht-Cache-Prozesse reservierten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d2740-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="d2740-152">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d2740-153">maxmemory-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d2740-153">maxmemory-policy.</span></span>
<span data-ttu-id="d2740-154">Konfiguriert die vertreibungs Richtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="d2740-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="d2740-155">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-155">All pricing tiers.</span></span> 
- <span data-ttu-id="d2740-156">Notify-Keyspace-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d2740-156">notify-keyspace-events.</span></span>
<span data-ttu-id="d2740-157">Konfiguriert die Keyspace-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="d2740-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="d2740-158">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="d2740-159">Hash-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="d2740-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="d2740-160">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d2740-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d2740-161">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d2740-162">Hash-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="d2740-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="d2740-163">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d2740-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d2740-164">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d2740-165">Satz-Max-intset-Einträge.</span><span class="sxs-lookup"><span data-stu-id="d2740-165">set-max-intset-entries.</span></span>
<span data-ttu-id="d2740-166">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d2740-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d2740-167">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d2740-168">zset-Max-ziplist-Einträge.</span><span class="sxs-lookup"><span data-stu-id="d2740-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="d2740-169">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d2740-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d2740-170">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d2740-171">zset-Max-ziplist-Wert.</span><span class="sxs-lookup"><span data-stu-id="d2740-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="d2740-172">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="d2740-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d2740-173">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d2740-174">Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="d2740-174">databases.</span></span>
<span data-ttu-id="d2740-175">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="d2740-175">Configures the number of databases.</span></span>
<span data-ttu-id="d2740-176">Diese Eigenschaft kann nur bei der Cache Erstellung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d2740-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="d2740-177">Standard-und Premium-Stufen.</span><span class="sxs-lookup"><span data-stu-id="d2740-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="d2740-178">Weitere Informationen finden Sie unter Verwalten von Azure-c-a/a-Cache mit Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="d2740-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="d2740-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2740-179">-ResourceGroupName</span></span>
<span data-ttu-id="d2740-180">Gibt den Namen der Ressourcengruppe an, in der der "a/a-Cache" erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2740-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="d2740-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="d2740-181">-ShardCount</span></span>
<span data-ttu-id="d2740-182">Gibt die Anzahl der zu erstellende Scherben in einem Premium-Cluster-Cache an.</span><span class="sxs-lookup"><span data-stu-id="d2740-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="d2740-183">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d2740-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2740-184">1</span><span class="sxs-lookup"><span data-stu-id="d2740-184">1</span></span>
- <span data-ttu-id="d2740-185">2</span><span class="sxs-lookup"><span data-stu-id="d2740-185">2</span></span>
- <span data-ttu-id="d2740-186">3</span><span class="sxs-lookup"><span data-stu-id="d2740-186">3</span></span>
- <span data-ttu-id="d2740-187">4</span><span class="sxs-lookup"><span data-stu-id="d2740-187">4</span></span>
- <span data-ttu-id="d2740-188">5</span><span class="sxs-lookup"><span data-stu-id="d2740-188">5</span></span>
- <span data-ttu-id="d2740-189">6</span><span class="sxs-lookup"><span data-stu-id="d2740-189">6</span></span>
- <span data-ttu-id="d2740-190">7</span><span class="sxs-lookup"><span data-stu-id="d2740-190">7</span></span>
- <span data-ttu-id="d2740-191">8</span><span class="sxs-lookup"><span data-stu-id="d2740-191">8</span></span>
- <span data-ttu-id="d2740-192">9</span><span class="sxs-lookup"><span data-stu-id="d2740-192">9</span></span> 
- <span data-ttu-id="d2740-193">10</span><span class="sxs-lookup"><span data-stu-id="d2740-193">10</span></span>

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

### <span data-ttu-id="d2740-194">-Size</span><span class="sxs-lookup"><span data-stu-id="d2740-194">-Size</span></span>
<span data-ttu-id="d2740-195">Gibt die Größe des Zwischenspeichers für "a. a" an.</span><span class="sxs-lookup"><span data-stu-id="d2740-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="d2740-196">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d2740-196">Valid values are:</span></span> 
- <span data-ttu-id="d2740-197">P1</span><span class="sxs-lookup"><span data-stu-id="d2740-197">P1</span></span>
- <span data-ttu-id="d2740-198">P2</span><span class="sxs-lookup"><span data-stu-id="d2740-198">P2</span></span>
- <span data-ttu-id="d2740-199">P3</span><span class="sxs-lookup"><span data-stu-id="d2740-199">P3</span></span>
- <span data-ttu-id="d2740-200">P4</span><span class="sxs-lookup"><span data-stu-id="d2740-200">P4</span></span>
- <span data-ttu-id="d2740-201">C0</span><span class="sxs-lookup"><span data-stu-id="d2740-201">C0</span></span>
- <span data-ttu-id="d2740-202">C1</span><span class="sxs-lookup"><span data-stu-id="d2740-202">C1</span></span>
- <span data-ttu-id="d2740-203">C2</span><span class="sxs-lookup"><span data-stu-id="d2740-203">C2</span></span>
- <span data-ttu-id="d2740-204">C3</span><span class="sxs-lookup"><span data-stu-id="d2740-204">C3</span></span>
- <span data-ttu-id="d2740-205">C4</span><span class="sxs-lookup"><span data-stu-id="d2740-205">C4</span></span>
- <span data-ttu-id="d2740-206">C5</span><span class="sxs-lookup"><span data-stu-id="d2740-206">C5</span></span>
- <span data-ttu-id="d2740-207">C6</span><span class="sxs-lookup"><span data-stu-id="d2740-207">C6</span></span>
- <span data-ttu-id="d2740-208">250MB</span><span class="sxs-lookup"><span data-stu-id="d2740-208">250MB</span></span>
- <span data-ttu-id="d2740-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="d2740-209">1GB</span></span>
- <span data-ttu-id="d2740-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="d2740-210">2.5GB</span></span>
- <span data-ttu-id="d2740-211">6GB</span><span class="sxs-lookup"><span data-stu-id="d2740-211">6GB</span></span>
- <span data-ttu-id="d2740-212">13GB</span><span class="sxs-lookup"><span data-stu-id="d2740-212">13GB</span></span>
- <span data-ttu-id="d2740-213">26GB</span><span class="sxs-lookup"><span data-stu-id="d2740-213">26GB</span></span>
- <span data-ttu-id="d2740-214">53GB der Standardwert ist 1GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="d2740-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="d2740-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="d2740-215">-Sku</span></span>
<span data-ttu-id="d2740-216">Gibt die SKU des zu erstellbaren zu erstellbaren zu erstellendes zu.</span><span class="sxs-lookup"><span data-stu-id="d2740-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="d2740-217">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d2740-217">Valid values are:</span></span> 
- <span data-ttu-id="d2740-218">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="d2740-218">Basic</span></span>
- <span data-ttu-id="d2740-219">Standard</span><span class="sxs-lookup"><span data-stu-id="d2740-219">Standard</span></span>
- <span data-ttu-id="d2740-220">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="d2740-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="d2740-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="d2740-221">-StaticIP</span></span>
<span data-ttu-id="d2740-222">Gibt eine eindeutige IP-Adresse im Subnetz für den Cache für den "a/a-Cache" an.</span><span class="sxs-lookup"><span data-stu-id="d2740-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="d2740-223">Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.</span><span class="sxs-lookup"><span data-stu-id="d2740-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="d2740-224">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="d2740-224">-SubnetId</span></span>
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

### <span data-ttu-id="d2740-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2740-225">-Tag</span></span>
<span data-ttu-id="d2740-226">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2740-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="d2740-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="d2740-227">-TenantSettings</span></span>
<span data-ttu-id="d2740-228">Dieser Parameter wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="d2740-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="d2740-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="d2740-229">-Zone</span></span>
<span data-ttu-id="d2740-230">Liste der Zonen.</span><span class="sxs-lookup"><span data-stu-id="d2740-230">List of zones.</span></span>

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

### <span data-ttu-id="d2740-231">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2740-231">-Confirm</span></span>
<span data-ttu-id="d2740-232">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2740-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2740-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2740-233">-WhatIf</span></span>
<span data-ttu-id="d2740-234">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2740-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2740-235">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2740-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2740-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2740-236">CommonParameters</span></span>
<span data-ttu-id="d2740-237">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2740-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2740-238">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2740-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2740-239">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2740-239">INPUTS</span></span>

### <span data-ttu-id="d2740-240">System. String</span><span class="sxs-lookup"><span data-stu-id="d2740-240">System.String</span></span>

### <span data-ttu-id="d2740-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2740-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d2740-242">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d2740-242">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d2740-243">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d2740-243">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d2740-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="d2740-244">System.String[]</span></span>

## <span data-ttu-id="d2740-245">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2740-245">OUTPUTS</span></span>

### <span data-ttu-id="d2740-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d2740-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="d2740-247">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2740-247">NOTES</span></span>

## <span data-ttu-id="d2740-248">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2740-248">RELATED LINKS</span></span>

[<span data-ttu-id="d2740-249">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2740-249">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d2740-250">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2740-250">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="d2740-251">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2740-251">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


