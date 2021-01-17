---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459656"
---
# <span data-ttu-id="5080e-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5080e-101">New-AzRedisCache</span></span>

## <span data-ttu-id="5080e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5080e-102">SYNOPSIS</span></span>
<span data-ttu-id="5080e-103">Erstellt einen Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="5080e-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="5080e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5080e-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5080e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5080e-105">DESCRIPTION</span></span>
<span data-ttu-id="5080e-106">Das **Cmdlet "New-AzRedisCache"** erstellt einen Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="5080e-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="5080e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5080e-107">EXAMPLES</span></span>

### <span data-ttu-id="5080e-108">Beispiel 1: Erstellen eines Caches für Redis</span><span class="sxs-lookup"><span data-stu-id="5080e-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="5080e-109">Dieser Befehl erstellt einen Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="5080e-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="5080e-110">Beispiel 2: Erstellen eines Redis-Caches für Standard-SKU</span><span class="sxs-lookup"><span data-stu-id="5080e-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="5080e-111">Dieser Befehl erstellt einen Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="5080e-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="5080e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5080e-112">PARAMETERS</span></span>

### <span data-ttu-id="5080e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5080e-113">-DefaultProfile</span></span>
<span data-ttu-id="5080e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5080e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5080e-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="5080e-115">-EnableNonSslPort</span></span>
<span data-ttu-id="5080e-116">Gibt an, ob der Nicht-SSL-Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5080e-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="5080e-117">Der Standardwert ist $False (der Nicht-SSL-Port ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="5080e-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="5080e-118">-Location</span><span class="sxs-lookup"><span data-stu-id="5080e-118">-Location</span></span>
<span data-ttu-id="5080e-119">Gibt den Speicherort an, an dem ein Cache für Redis erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5080e-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="5080e-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5080e-120">Valid values are:</span></span> 
- <span data-ttu-id="5080e-121">USA, Mitte,Norden</span><span class="sxs-lookup"><span data-stu-id="5080e-121">North Central US</span></span>
- <span data-ttu-id="5080e-122">USA, Süden, Mitte</span><span class="sxs-lookup"><span data-stu-id="5080e-122">South Central US</span></span>
- <span data-ttu-id="5080e-123">USA, Mitte</span><span class="sxs-lookup"><span data-stu-id="5080e-123">Central US</span></span>
- <span data-ttu-id="5080e-124">Europa, Westen</span><span class="sxs-lookup"><span data-stu-id="5080e-124">West Europe</span></span>
- <span data-ttu-id="5080e-125">Europa, Norden</span><span class="sxs-lookup"><span data-stu-id="5080e-125">North Europe</span></span>
- <span data-ttu-id="5080e-126">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="5080e-126">West US</span></span>
- <span data-ttu-id="5080e-127">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="5080e-127">East US</span></span>
- <span data-ttu-id="5080e-128">USA, Osten 2</span><span class="sxs-lookup"><span data-stu-id="5080e-128">East US 2</span></span>
- <span data-ttu-id="5080e-129">Japan, Osten</span><span class="sxs-lookup"><span data-stu-id="5080e-129">Japan East</span></span>
- <span data-ttu-id="5080e-130">Japan, Westen</span><span class="sxs-lookup"><span data-stu-id="5080e-130">Japan West</span></span>
- <span data-ttu-id="5080e-131">Brasilien, Süden</span><span class="sxs-lookup"><span data-stu-id="5080e-131">Brazil South</span></span>
- <span data-ttu-id="5080e-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="5080e-132">Southeast Asia</span></span>
- <span data-ttu-id="5080e-133">Ostasien</span><span class="sxs-lookup"><span data-stu-id="5080e-133">East Asia</span></span>
- <span data-ttu-id="5080e-134">Australien, Osten</span><span class="sxs-lookup"><span data-stu-id="5080e-134">Australia East</span></span>
- <span data-ttu-id="5080e-135">Australien, Südosten</span><span class="sxs-lookup"><span data-stu-id="5080e-135">Australia Southeast</span></span>

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

### <span data-ttu-id="5080e-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5080e-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="5080e-137">Geben Sie die TLS-Version an, die von Clients zum Herstellen einer Verbindung mit dem Cache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5080e-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="5080e-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5080e-138">-Name</span></span>
<span data-ttu-id="5080e-139">Gibt den Namen des zu erstellenden Caches für Redis an.</span><span class="sxs-lookup"><span data-stu-id="5080e-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="5080e-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="5080e-140">-RedisConfiguration</span></span>
<span data-ttu-id="5080e-141">Gibt die Konfigurationseinstellungen von Redis an.</span><span class="sxs-lookup"><span data-stu-id="5080e-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="5080e-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5080e-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5080e-143">rdb-backup-enabled.</span><span class="sxs-lookup"><span data-stu-id="5080e-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="5080e-144">Gibt an, dass die Daten persistenz von Redis aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5080e-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="5080e-145">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="5080e-145">Premium tier only.</span></span>
- <span data-ttu-id="5080e-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="5080e-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="5080e-147">Gibt die Verbindungszeichenfolge zum Speicherkonto für die Daten persistenz von Redis an.</span><span class="sxs-lookup"><span data-stu-id="5080e-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="5080e-148">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="5080e-148">Premium tier only.</span></span>
- <span data-ttu-id="5080e-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="5080e-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="5080e-150">Gibt die Sicherungshäufigkeit für die Daten persistenz von Redis an.</span><span class="sxs-lookup"><span data-stu-id="5080e-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="5080e-151">Nur Premium-Stufe.</span><span class="sxs-lookup"><span data-stu-id="5080e-151">Premium tier only.</span></span> 
- <span data-ttu-id="5080e-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="5080e-152">maxmemory-reserved.</span></span>
<span data-ttu-id="5080e-153">Konfiguriert den Speicher, der für Prozesse ohne Cache reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="5080e-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="5080e-154">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5080e-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="5080e-155">maxmemory-policy.</span></span>
<span data-ttu-id="5080e-156">Konfiguriert die Entfernungsrichtlinie für den Cache.</span><span class="sxs-lookup"><span data-stu-id="5080e-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="5080e-157">Alle Preisstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-157">All pricing tiers.</span></span> 
- <span data-ttu-id="5080e-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="5080e-158">notify-keyspace-events.</span></span>
<span data-ttu-id="5080e-159">Konfiguriert Keyspacebenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="5080e-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="5080e-160">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="5080e-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="5080e-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="5080e-162">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="5080e-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5080e-163">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5080e-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="5080e-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="5080e-165">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="5080e-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5080e-166">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5080e-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="5080e-167">set-max-intset-entries.</span></span>
<span data-ttu-id="5080e-168">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="5080e-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5080e-169">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5080e-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="5080e-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="5080e-171">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="5080e-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5080e-172">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5080e-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="5080e-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="5080e-174">Konfiguriert die Speicheroptimierung für kleine aggregierte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="5080e-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5080e-175">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5080e-176">datenbanken.</span><span class="sxs-lookup"><span data-stu-id="5080e-176">databases.</span></span>
<span data-ttu-id="5080e-177">Konfiguriert die Anzahl der Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="5080e-177">Configures the number of databases.</span></span>
<span data-ttu-id="5080e-178">Diese Eigenschaft kann nur beim Erstellen des Caches konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5080e-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="5080e-179">Standard- und Premiumstufen.</span><span class="sxs-lookup"><span data-stu-id="5080e-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="5080e-180">Weitere Informationen finden Sie unter Verwalten des Azure Redis Cache mit Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="5080e-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="5080e-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5080e-181">-ResourceGroupName</span></span>
<span data-ttu-id="5080e-182">Gibt den Namen der Ressourcengruppe an, in der der Cache für Redis erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5080e-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="5080e-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="5080e-183">-ShardCount</span></span>
<span data-ttu-id="5080e-184">Gibt die Anzahl der in einem Premium-Clustercache zu erstellenden Shards an.</span><span class="sxs-lookup"><span data-stu-id="5080e-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="5080e-185">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5080e-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5080e-186">1</span><span class="sxs-lookup"><span data-stu-id="5080e-186">1</span></span>
- <span data-ttu-id="5080e-187">2</span><span class="sxs-lookup"><span data-stu-id="5080e-187">2</span></span>
- <span data-ttu-id="5080e-188">3</span><span class="sxs-lookup"><span data-stu-id="5080e-188">3</span></span>
- <span data-ttu-id="5080e-189">4</span><span class="sxs-lookup"><span data-stu-id="5080e-189">4</span></span>
- <span data-ttu-id="5080e-190">5</span><span class="sxs-lookup"><span data-stu-id="5080e-190">5</span></span>
- <span data-ttu-id="5080e-191">6</span><span class="sxs-lookup"><span data-stu-id="5080e-191">6</span></span>
- <span data-ttu-id="5080e-192">7</span><span class="sxs-lookup"><span data-stu-id="5080e-192">7</span></span>
- <span data-ttu-id="5080e-193">8</span><span class="sxs-lookup"><span data-stu-id="5080e-193">8</span></span>
- <span data-ttu-id="5080e-194">9</span><span class="sxs-lookup"><span data-stu-id="5080e-194">9</span></span> 
- <span data-ttu-id="5080e-195">10</span><span class="sxs-lookup"><span data-stu-id="5080e-195">10</span></span>

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

### <span data-ttu-id="5080e-196">-Size</span><span class="sxs-lookup"><span data-stu-id="5080e-196">-Size</span></span>
<span data-ttu-id="5080e-197">Gibt die Größe des Caches von Redis an.</span><span class="sxs-lookup"><span data-stu-id="5080e-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="5080e-198">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5080e-198">Valid values are:</span></span> 
- <span data-ttu-id="5080e-199">P1</span><span class="sxs-lookup"><span data-stu-id="5080e-199">P1</span></span>
- <span data-ttu-id="5080e-200">P2</span><span class="sxs-lookup"><span data-stu-id="5080e-200">P2</span></span>
- <span data-ttu-id="5080e-201">P3</span><span class="sxs-lookup"><span data-stu-id="5080e-201">P3</span></span>
- <span data-ttu-id="5080e-202">P4</span><span class="sxs-lookup"><span data-stu-id="5080e-202">P4</span></span>
- <span data-ttu-id="5080e-203">P5</span><span class="sxs-lookup"><span data-stu-id="5080e-203">P5</span></span>
- <span data-ttu-id="5080e-204">C0</span><span class="sxs-lookup"><span data-stu-id="5080e-204">C0</span></span>
- <span data-ttu-id="5080e-205">C1</span><span class="sxs-lookup"><span data-stu-id="5080e-205">C1</span></span>
- <span data-ttu-id="5080e-206">C2</span><span class="sxs-lookup"><span data-stu-id="5080e-206">C2</span></span>
- <span data-ttu-id="5080e-207">C3</span><span class="sxs-lookup"><span data-stu-id="5080e-207">C3</span></span>
- <span data-ttu-id="5080e-208">C4</span><span class="sxs-lookup"><span data-stu-id="5080e-208">C4</span></span>
- <span data-ttu-id="5080e-209">C5</span><span class="sxs-lookup"><span data-stu-id="5080e-209">C5</span></span>
- <span data-ttu-id="5080e-210">C6</span><span class="sxs-lookup"><span data-stu-id="5080e-210">C6</span></span>
- <span data-ttu-id="5080e-211">250 MB</span><span class="sxs-lookup"><span data-stu-id="5080e-211">250MB</span></span>
- <span data-ttu-id="5080e-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="5080e-212">1GB</span></span>
- <span data-ttu-id="5080e-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="5080e-213">2.5GB</span></span>
- <span data-ttu-id="5080e-214">6 GB</span><span class="sxs-lookup"><span data-stu-id="5080e-214">6GB</span></span>
- <span data-ttu-id="5080e-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="5080e-215">13GB</span></span>
- <span data-ttu-id="5080e-216">26 GB</span><span class="sxs-lookup"><span data-stu-id="5080e-216">26GB</span></span>
- <span data-ttu-id="5080e-217">53 GB Der Standardwert ist 1 GB oder C1.</span><span class="sxs-lookup"><span data-stu-id="5080e-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="5080e-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="5080e-218">-Sku</span></span>
<span data-ttu-id="5080e-219">Gibt die SKU des zu erstellenden Caches für Redis an.</span><span class="sxs-lookup"><span data-stu-id="5080e-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="5080e-220">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5080e-220">Valid values are:</span></span> 
- <span data-ttu-id="5080e-221">Standard</span><span class="sxs-lookup"><span data-stu-id="5080e-221">Basic</span></span>
- <span data-ttu-id="5080e-222">Standard</span><span class="sxs-lookup"><span data-stu-id="5080e-222">Standard</span></span>
- <span data-ttu-id="5080e-223">Premium Der Standardwert ist "Standard".</span><span class="sxs-lookup"><span data-stu-id="5080e-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="5080e-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="5080e-224">-StaticIP</span></span>
<span data-ttu-id="5080e-225">Gibt eine eindeutige IP-Adresse im Subnetz für den Redis Cache an.</span><span class="sxs-lookup"><span data-stu-id="5080e-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="5080e-226">Wenn Sie keinen Wert für diesen Parameter angeben, wählt dieses Cmdlet eine IP-Adresse aus dem Subnetz aus.</span><span class="sxs-lookup"><span data-stu-id="5080e-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="5080e-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5080e-227">-SubnetId</span></span>
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

### <span data-ttu-id="5080e-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="5080e-228">-Tag</span></span>
<span data-ttu-id="5080e-229">Eine Hashtabelle, die Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="5080e-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="5080e-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="5080e-230">-TenantSettings</span></span>
<span data-ttu-id="5080e-231">Dieser Parameter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="5080e-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="5080e-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="5080e-232">-Zone</span></span>
<span data-ttu-id="5080e-233">Liste der Zonen.</span><span class="sxs-lookup"><span data-stu-id="5080e-233">List of zones.</span></span>

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

### <span data-ttu-id="5080e-234">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5080e-234">-Confirm</span></span>
<span data-ttu-id="5080e-235">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5080e-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5080e-236">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5080e-236">-WhatIf</span></span>
<span data-ttu-id="5080e-237">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5080e-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5080e-238">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5080e-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5080e-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5080e-239">CommonParameters</span></span>
<span data-ttu-id="5080e-240">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5080e-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5080e-241">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5080e-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5080e-242">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5080e-242">INPUTS</span></span>

### <span data-ttu-id="5080e-243">System.String</span><span class="sxs-lookup"><span data-stu-id="5080e-243">System.String</span></span>

### <span data-ttu-id="5080e-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5080e-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5080e-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5080e-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5080e-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5080e-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5080e-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5080e-247">System.String[]</span></span>

## <span data-ttu-id="5080e-248">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5080e-248">OUTPUTS</span></span>

### <span data-ttu-id="5080e-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5080e-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="5080e-250">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5080e-250">NOTES</span></span>

## <span data-ttu-id="5080e-251">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5080e-251">RELATED LINKS</span></span>

[<span data-ttu-id="5080e-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5080e-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5080e-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5080e-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5080e-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5080e-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


