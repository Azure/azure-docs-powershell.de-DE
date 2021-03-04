---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: 1b16f30b068eb41bf0202c65e95f55f94769ba2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943846"
---
# <span data-ttu-id="f1240-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="f1240-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="f1240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1240-102">SYNOPSIS</span></span>
<span data-ttu-id="f1240-103">Aktualisiert einen vorhandenen RedisEnterprise-Cluster</span><span class="sxs-lookup"><span data-stu-id="f1240-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="f1240-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1240-104">SYNTAX</span></span>

### <span data-ttu-id="f1240-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1240-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1240-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f1240-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1240-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1240-107">DESCRIPTION</span></span>
<span data-ttu-id="f1240-108">Aktualisiert einen vorhandenen RedisEnterprise-Cluster</span><span class="sxs-lookup"><span data-stu-id="f1240-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="f1240-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1240-109">EXAMPLES</span></span>

### <span data-ttu-id="f1240-110">Beispiel 1: Aktualisieren des Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="f1240-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="f1240-111">Mit diesem Befehl wird die minimale TLS-Version aktualisiert und dem Redis Enterprise Cache mit dem Namen MyCache ein Tag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f1240-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="f1240-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1240-112">PARAMETERS</span></span>

### <span data-ttu-id="f1240-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1240-113">-AsJob</span></span>
<span data-ttu-id="f1240-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1240-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f1240-115">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="f1240-115">-Capacity</span></span>
<span data-ttu-id="f1240-116">Die Größe des RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f1240-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="f1240-117">Je nach SKU ist standardmäßig 2 oder 3 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f1240-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="f1240-118">Gültige Werte sind (2, 4, 6, ...) für Enterprise SKUs und (3, 9, 15, ...) für Flash-SKUs.</span><span class="sxs-lookup"><span data-stu-id="f1240-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="f1240-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f1240-119">-ClusterName</span></span>
<span data-ttu-id="f1240-120">Der Name des RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f1240-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="f1240-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1240-121">-DefaultProfile</span></span>
<span data-ttu-id="f1240-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1240-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1240-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1240-123">-InputObject</span></span>
<span data-ttu-id="f1240-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f1240-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1240-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f1240-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="f1240-126">Die mindestens für den Cluster zu unterstützende TLS-Version, z. B. "1.2".</span><span class="sxs-lookup"><span data-stu-id="f1240-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="f1240-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1240-127">-NoWait</span></span>
<span data-ttu-id="f1240-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f1240-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1240-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1240-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1240-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1240-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1240-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="f1240-131">-Sku</span></span>
<span data-ttu-id="f1240-132">Der Typ des zu bereitstellenden RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f1240-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="f1240-133">Mögliche Werte: (Enterprise_E10, EnterpriseFlash_F300 usw.)</span><span class="sxs-lookup"><span data-stu-id="f1240-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="f1240-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1240-134">-SubscriptionId</span></span>
<span data-ttu-id="f1240-135">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1240-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1240-136">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="f1240-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f1240-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1240-137">-Tag</span></span>
<span data-ttu-id="f1240-138">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="f1240-138">Resource tags.</span></span>

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

### <span data-ttu-id="f1240-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1240-139">-Confirm</span></span>
<span data-ttu-id="f1240-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1240-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1240-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1240-141">-WhatIf</span></span>
<span data-ttu-id="f1240-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1240-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1240-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1240-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1240-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1240-144">CommonParameters</span></span>
<span data-ttu-id="f1240-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1240-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1240-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1240-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1240-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1240-147">INPUTS</span></span>

### <span data-ttu-id="f1240-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="f1240-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="f1240-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1240-149">OUTPUTS</span></span>

### <span data-ttu-id="f1240-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="f1240-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="f1240-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1240-151">NOTES</span></span>

<span data-ttu-id="f1240-152">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f1240-152">ALIASES</span></span>

<span data-ttu-id="f1240-153">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f1240-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1240-154">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f1240-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1240-155">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1240-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1240-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="f1240-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1240-157">`[ClusterName <String>]`: Der Name des RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f1240-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="f1240-158">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f1240-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f1240-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f1240-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1240-160">`[Location <String>]`: Der Bereich, in dem sich der Vorgang befindet.</span><span class="sxs-lookup"><span data-stu-id="f1240-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="f1240-161">`[OperationId <String>]`: Der eindeutige Bezeichner des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f1240-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="f1240-162">`[PrivateEndpointConnectionName <String>]`: Der Name der privaten Endpunktverbindung, die der Azure-Ressource zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="f1240-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="f1240-163">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1240-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f1240-164">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1240-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f1240-165">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="f1240-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f1240-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1240-166">RELATED LINKS</span></span>

