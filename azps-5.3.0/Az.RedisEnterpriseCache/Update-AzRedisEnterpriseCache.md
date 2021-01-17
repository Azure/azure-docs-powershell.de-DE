---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378172"
---
# <span data-ttu-id="2eb37-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="2eb37-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="2eb37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb37-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb37-103">Aktualisiert einen vorhandenen RedisEnterprise-Cluster</span><span class="sxs-lookup"><span data-stu-id="2eb37-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="2eb37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2eb37-104">SYNTAX</span></span>

### <span data-ttu-id="2eb37-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2eb37-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2eb37-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2eb37-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2eb37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2eb37-107">DESCRIPTION</span></span>
<span data-ttu-id="2eb37-108">Aktualisiert einen vorhandenen RedisEnterprise-Cluster</span><span class="sxs-lookup"><span data-stu-id="2eb37-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="2eb37-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2eb37-109">EXAMPLES</span></span>

### <span data-ttu-id="2eb37-110">Beispiel 1: Aktualisieren des Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="2eb37-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="2eb37-111">Dieser Befehl aktualisiert die minimale TLS-Version und fügt dem Redis Enterprise-Cache mit dem Namen "MyCache" ein Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="2eb37-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="2eb37-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eb37-112">PARAMETERS</span></span>

### <span data-ttu-id="2eb37-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2eb37-113">-AsJob</span></span>
<span data-ttu-id="2eb37-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2eb37-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2eb37-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="2eb37-115">-Capacity</span></span>
<span data-ttu-id="2eb37-116">Die Größe des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2eb37-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="2eb37-117">Je nach SKU wird standardmäßig "2" oder "3" verwendet.</span><span class="sxs-lookup"><span data-stu-id="2eb37-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="2eb37-118">Gültige Werte sind (2, 4, 6, ...) für Enterprise-SKUs und (3, 9, 15, ...) für Flash-SKUs.</span><span class="sxs-lookup"><span data-stu-id="2eb37-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="2eb37-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2eb37-119">-ClusterName</span></span>
<span data-ttu-id="2eb37-120">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2eb37-120">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb37-121">-DefaultProfile</span></span>
<span data-ttu-id="2eb37-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2eb37-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb37-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eb37-123">-InputObject</span></span>
<span data-ttu-id="2eb37-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2eb37-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb37-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2eb37-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="2eb37-126">Die minimale zu unterstützende TLS-Version für den Cluster, z. B. '1.2'</span><span class="sxs-lookup"><span data-stu-id="2eb37-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="2eb37-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2eb37-127">-NoWait</span></span>
<span data-ttu-id="2eb37-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2eb37-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2eb37-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb37-129">-ResourceGroupName</span></span>
<span data-ttu-id="2eb37-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2eb37-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb37-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="2eb37-131">-Sku</span></span>
<span data-ttu-id="2eb37-132">Der Typ des zu implementierenden RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2eb37-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="2eb37-133">Mögliche Werte: (Enterprise_E10, EnterpriseFlash_F300 usw.)</span><span class="sxs-lookup"><span data-stu-id="2eb37-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb37-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2eb37-134">-SubscriptionId</span></span>
<span data-ttu-id="2eb37-135">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2eb37-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2eb37-136">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="2eb37-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb37-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="2eb37-137">-Tag</span></span>
<span data-ttu-id="2eb37-138">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="2eb37-138">Resource tags.</span></span>

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

### <span data-ttu-id="2eb37-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eb37-139">-Confirm</span></span>
<span data-ttu-id="2eb37-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2eb37-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb37-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2eb37-141">-WhatIf</span></span>
<span data-ttu-id="2eb37-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2eb37-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb37-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2eb37-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb37-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb37-144">CommonParameters</span></span>
<span data-ttu-id="2eb37-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb37-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb37-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eb37-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb37-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2eb37-147">INPUTS</span></span>

### <span data-ttu-id="2eb37-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="2eb37-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="2eb37-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2eb37-149">OUTPUTS</span></span>

### <span data-ttu-id="2eb37-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="2eb37-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="2eb37-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2eb37-151">NOTES</span></span>

<span data-ttu-id="2eb37-152">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2eb37-152">ALIASES</span></span>

<span data-ttu-id="2eb37-153">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2eb37-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2eb37-154">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2eb37-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2eb37-155">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2eb37-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2eb37-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2eb37-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2eb37-157">`[ClusterName <String>]`: Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2eb37-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="2eb37-158">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2eb37-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2eb37-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2eb37-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2eb37-160">`[Location <String>]`: Der Bereich, in dem sich der Vorgang befindet.</span><span class="sxs-lookup"><span data-stu-id="2eb37-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="2eb37-161">`[OperationId <String>]`: Der eindeutige Bezeichner des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="2eb37-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="2eb37-162">`[PrivateEndpointConnectionName <String>]`: Der Name der privaten Endpunktverbindung, die der Azure-Ressource zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="2eb37-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="2eb37-163">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2eb37-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2eb37-164">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2eb37-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2eb37-165">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="2eb37-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2eb37-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2eb37-166">RELATED LINKS</span></span>

