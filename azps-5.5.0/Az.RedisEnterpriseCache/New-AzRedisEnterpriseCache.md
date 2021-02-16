---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169196"
---
# <span data-ttu-id="53705-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="53705-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="53705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53705-102">SYNOPSIS</span></span>
<span data-ttu-id="53705-103">Erstellt einen Redis Enterpise-Cachecluster und eine zugeordnete Datenbank.</span><span class="sxs-lookup"><span data-stu-id="53705-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="53705-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53705-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53705-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53705-105">DESCRIPTION</span></span>
<span data-ttu-id="53705-106">Erstellt oder aktualisiert einen vorhandenen Cachecluster (überschreiben/neu erstellen, mit potenziellen Ausfallzeiten) und eine zugeordnete Datenbank mit dem Namen "default".</span><span class="sxs-lookup"><span data-stu-id="53705-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="53705-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53705-107">EXAMPLES</span></span>

### <span data-ttu-id="53705-108">Beispiel 1: Erstellen eines Redis Enterprise-Caches</span><span class="sxs-lookup"><span data-stu-id="53705-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="53705-109">Mit diesem Befehl wird ein Redis Enterprise-Cache namens "MyCache" erstellt.</span><span class="sxs-lookup"><span data-stu-id="53705-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="53705-110">Beispiel 2: Erstellen eines Redis Enterprise Caches mit einigen optionalen Parametern</span><span class="sxs-lookup"><span data-stu-id="53705-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="53705-111">Mit diesem Befehl wird mit einigen optionalen Parametern ein Redis Enterprise-Cache namens "MyCache" erstellt.</span><span class="sxs-lookup"><span data-stu-id="53705-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="53705-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53705-112">PARAMETERS</span></span>

### <span data-ttu-id="53705-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53705-113">-AsJob</span></span>
<span data-ttu-id="53705-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="53705-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="53705-115">-Capacity</span></span>
<span data-ttu-id="53705-116">Die Größe des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="53705-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="53705-117">Je nach SKU wird standardmäßig "2" oder "3" verwendet.</span><span class="sxs-lookup"><span data-stu-id="53705-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="53705-118">Gültige Werte sind (2, 4, 6, ...) für Enterprise-SKUs und (3, 9, 15, ...) für Flash-SKUs.</span><span class="sxs-lookup"><span data-stu-id="53705-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="53705-119">-ClientProtocol</span></span>
<span data-ttu-id="53705-120">Gibt an, ob Redis Clients eine Verbindung mit TLS-verschlüsselten oder Nur-Text-Redis-Protokollen herstellen können.</span><span class="sxs-lookup"><span data-stu-id="53705-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="53705-121">Der Standardwert ist TLS-verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="53705-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="53705-122">-ClusteringPolicy</span></span>
<span data-ttu-id="53705-123">Clusteringrichtlinie – Standard ist OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="53705-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="53705-124">Wird zum Zeitpunkt der Erstellung angegeben.</span><span class="sxs-lookup"><span data-stu-id="53705-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="53705-125">-ClusterName</span></span>
<span data-ttu-id="53705-126">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="53705-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53705-127">-DefaultProfile</span></span>
<span data-ttu-id="53705-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53705-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="53705-129">-EvictionPolicy</span></span>
<span data-ttu-id="53705-130">Richtlinie für die Entfernung von Redis – Der Standardwert ist "VolatileLRU".</span><span class="sxs-lookup"><span data-stu-id="53705-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-131">-Location</span><span class="sxs-lookup"><span data-stu-id="53705-131">-Location</span></span>
<span data-ttu-id="53705-132">Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="53705-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="53705-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="53705-134">Die minimale zu unterstützende TLS-Version für den Cluster, z. B. 1.2</span><span class="sxs-lookup"><span data-stu-id="53705-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-135">-Module</span><span class="sxs-lookup"><span data-stu-id="53705-135">-Module</span></span>
<span data-ttu-id="53705-136">Optionale Gruppe von Redis-Modulen, die in dieser Datenbank aktiviert werden sollen – Module können nur zur Erstellungszeit hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="53705-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="53705-137">Informationen zum Erstellen von #A0 finden Sie im Abschnitt "NOTES", und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="53705-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="53705-138">-NoWait</span></span>
<span data-ttu-id="53705-139">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="53705-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-140">-Port</span><span class="sxs-lookup"><span data-stu-id="53705-140">-Port</span></span>
<span data-ttu-id="53705-141">Der TCP-Port des Datenbankendpunkts.</span><span class="sxs-lookup"><span data-stu-id="53705-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="53705-142">Wird zum Zeitpunkt der Erstellung angegeben.</span><span class="sxs-lookup"><span data-stu-id="53705-142">Specified at create time.</span></span>
<span data-ttu-id="53705-143">Standardmäßig wird ein verfügbarer Port verwendet.</span><span class="sxs-lookup"><span data-stu-id="53705-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53705-144">-ResourceGroupName</span></span>
<span data-ttu-id="53705-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="53705-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="53705-146">-Sku</span></span>
<span data-ttu-id="53705-147">Der Typ des zu implementierenden RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="53705-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="53705-148">Mögliche Werte: (Enterprise_E10, EnterpriseFlash_F300 usw.)</span><span class="sxs-lookup"><span data-stu-id="53705-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53705-149">-SubscriptionId</span></span>
<span data-ttu-id="53705-150">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="53705-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="53705-151">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="53705-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="53705-152">-Tag</span></span>
<span data-ttu-id="53705-153">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="53705-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="53705-154">-Zone</span></span>
<span data-ttu-id="53705-155">Die Zonen, in denen dieser Cluster bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="53705-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53705-156">-Confirm</span></span>
<span data-ttu-id="53705-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53705-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53705-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="53705-158">-WhatIf</span></span>
<span data-ttu-id="53705-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53705-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53705-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53705-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53705-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53705-161">CommonParameters</span></span>
<span data-ttu-id="53705-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53705-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53705-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53705-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53705-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53705-164">INPUTS</span></span>

## <span data-ttu-id="53705-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53705-165">OUTPUTS</span></span>

### <span data-ttu-id="53705-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="53705-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="53705-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53705-167">NOTES</span></span>

<span data-ttu-id="53705-168">ALIASE</span><span class="sxs-lookup"><span data-stu-id="53705-168">ALIASES</span></span>

<span data-ttu-id="53705-169">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="53705-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53705-170">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="53705-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53705-171">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53705-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53705-172">MODULE <IModule[]>: Optionale Gruppe von Redis-Modulen, die in dieser Datenbank aktiviert werden sollen – Module können nur zur Erstellungszeit hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="53705-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="53705-173">`Name <String>`: Der Name des Moduls, z. B. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="53705-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="53705-174">`[Arg <String>]`: Konfigurationsoptionen für das Modul, z. B. 'ERROR_RATE 0,00 INITIAL_SIZE 400'.</span><span class="sxs-lookup"><span data-stu-id="53705-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="53705-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53705-175">RELATED LINKS</span></span>

