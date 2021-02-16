---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158465"
---
# <span data-ttu-id="502b9-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="502b9-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="502b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="502b9-102">SYNOPSIS</span></span>
<span data-ttu-id="502b9-103">Aktualisiert einen vorhandenen RedisEnterprise-Cluster</span><span class="sxs-lookup"><span data-stu-id="502b9-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="502b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="502b9-104">SYNTAX</span></span>

### <span data-ttu-id="502b9-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="502b9-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="502b9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="502b9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="502b9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="502b9-107">DESCRIPTION</span></span>
<span data-ttu-id="502b9-108">Aktualisiert einen vorhandenen RedisEnterprise-Cluster</span><span class="sxs-lookup"><span data-stu-id="502b9-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="502b9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="502b9-109">EXAMPLES</span></span>

### <span data-ttu-id="502b9-110">Beispiel 1: Aktualisieren des Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="502b9-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="502b9-111">Dieser Befehl aktualisiert die minimale TLS-Version und fügt dem Redis Enterprise-Cache mit dem Namen "MyCache" ein Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="502b9-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="502b9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="502b9-112">PARAMETERS</span></span>

### <span data-ttu-id="502b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="502b9-113">-AsJob</span></span>
<span data-ttu-id="502b9-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="502b9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="502b9-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="502b9-115">-Capacity</span></span>
<span data-ttu-id="502b9-116">Die Größe des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="502b9-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="502b9-117">Je nach SKU wird standardmäßig "2" oder "3" verwendet.</span><span class="sxs-lookup"><span data-stu-id="502b9-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="502b9-118">Gültige Werte sind (2, 4, 6, ...) für Enterprise-SKUs und (3, 9, 15, ...) für Flash-SKUs.</span><span class="sxs-lookup"><span data-stu-id="502b9-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="502b9-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="502b9-119">-ClusterName</span></span>
<span data-ttu-id="502b9-120">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="502b9-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="502b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502b9-121">-DefaultProfile</span></span>
<span data-ttu-id="502b9-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="502b9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="502b9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="502b9-123">-InputObject</span></span>
<span data-ttu-id="502b9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="502b9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="502b9-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="502b9-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="502b9-126">Die minimale zu unterstützende TLS-Version für den Cluster, z. B. '1.2'</span><span class="sxs-lookup"><span data-stu-id="502b9-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="502b9-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="502b9-127">-NoWait</span></span>
<span data-ttu-id="502b9-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="502b9-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="502b9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502b9-129">-ResourceGroupName</span></span>
<span data-ttu-id="502b9-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="502b9-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="502b9-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="502b9-131">-Sku</span></span>
<span data-ttu-id="502b9-132">Der Typ des zu implementierenden RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="502b9-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="502b9-133">Mögliche Werte: (Enterprise_E10, EnterpriseFlash_F300 usw.)</span><span class="sxs-lookup"><span data-stu-id="502b9-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="502b9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="502b9-134">-SubscriptionId</span></span>
<span data-ttu-id="502b9-135">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="502b9-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="502b9-136">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="502b9-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="502b9-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="502b9-137">-Tag</span></span>
<span data-ttu-id="502b9-138">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="502b9-138">Resource tags.</span></span>

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

### <span data-ttu-id="502b9-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="502b9-139">-Confirm</span></span>
<span data-ttu-id="502b9-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="502b9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="502b9-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="502b9-141">-WhatIf</span></span>
<span data-ttu-id="502b9-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="502b9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="502b9-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="502b9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="502b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502b9-144">CommonParameters</span></span>
<span data-ttu-id="502b9-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502b9-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="502b9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502b9-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="502b9-147">INPUTS</span></span>

### <span data-ttu-id="502b9-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="502b9-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="502b9-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="502b9-149">OUTPUTS</span></span>

### <span data-ttu-id="502b9-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="502b9-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="502b9-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="502b9-151">NOTES</span></span>

<span data-ttu-id="502b9-152">ALIASE</span><span class="sxs-lookup"><span data-stu-id="502b9-152">ALIASES</span></span>

<span data-ttu-id="502b9-153">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="502b9-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="502b9-154">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="502b9-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="502b9-155">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="502b9-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="502b9-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="502b9-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="502b9-157">`[ClusterName <String>]`: Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="502b9-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="502b9-158">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="502b9-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="502b9-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="502b9-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="502b9-160">`[Location <String>]`: Der Bereich, in dem sich der Vorgang befindet.</span><span class="sxs-lookup"><span data-stu-id="502b9-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="502b9-161">`[OperationId <String>]`: Der eindeutige Bezeichner des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="502b9-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="502b9-162">`[PrivateEndpointConnectionName <String>]`: Der Name der privaten Endpunktverbindung, die der Azure-Ressource zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="502b9-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="502b9-163">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="502b9-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="502b9-164">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="502b9-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="502b9-165">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="502b9-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="502b9-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="502b9-166">RELATED LINKS</span></span>

