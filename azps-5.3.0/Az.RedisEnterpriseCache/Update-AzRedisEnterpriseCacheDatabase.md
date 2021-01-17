---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378158"
---
# <span data-ttu-id="fd8a5-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="fd8a5-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="fd8a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8a5-103">Aktualisiert eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="fd8a5-103">Updates a database</span></span>

## <span data-ttu-id="fd8a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd8a5-104">SYNTAX</span></span>

### <span data-ttu-id="fd8a5-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd8a5-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fd8a5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fd8a5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fd8a5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd8a5-107">DESCRIPTION</span></span>
<span data-ttu-id="fd8a5-108">Aktualisiert eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="fd8a5-108">Updates a database</span></span>

## <span data-ttu-id="fd8a5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd8a5-109">EXAMPLES</span></span>

### <span data-ttu-id="fd8a5-110">Beispiel 1: Aktualisieren des Clientprotokolls</span><span class="sxs-lookup"><span data-stu-id="fd8a5-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="fd8a5-111">Mit diesem Befehl wird das Clientprotokoll der Datenbank für den Redis Enterprise-Cache namens "MyCache" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="fd8a5-112">Beispiel 2: Aktualisieren des Clientprotokolls und der Entfernungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fd8a5-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="fd8a5-113">Mit diesem Befehl werden das Clientprotokoll und die Entfernungsrichtlinie der Datenbank für den Redis Enterprise-Cache namens "MyCache" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="fd8a5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd8a5-114">PARAMETERS</span></span>

### <span data-ttu-id="fd8a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd8a5-115">-AsJob</span></span>
<span data-ttu-id="fd8a5-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd8a5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fd8a5-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="fd8a5-117">-ClientProtocol</span></span>
<span data-ttu-id="fd8a5-118">Gibt an, ob Redis Clients eine Verbindung mit TLS-verschlüsselten oder Nur-Text-Redis-Protokollen herstellen können.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="fd8a5-119">Der Standardwert ist TLS-verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="fd8a5-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="fd8a5-120">-ClusteringPolicy</span></span>
<span data-ttu-id="fd8a5-121">Clusteringrichtlinie – Standard ist OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="fd8a5-122">Wird zum Zeitpunkt der Erstellung angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-122">Specified at create time.</span></span>

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

### <span data-ttu-id="fd8a5-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fd8a5-123">-ClusterName</span></span>
<span data-ttu-id="fd8a5-124">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="fd8a5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8a5-125">-DefaultProfile</span></span>
<span data-ttu-id="fd8a5-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd8a5-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd8a5-127">-EvictionPolicy</span></span>
<span data-ttu-id="fd8a5-128">Richtlinie für die Entfernung von Redis – Standard ist "FlüchtigeLRU"</span><span class="sxs-lookup"><span data-stu-id="fd8a5-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="fd8a5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd8a5-129">-InputObject</span></span>
<span data-ttu-id="fd8a5-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd8a5-131">-Module</span><span class="sxs-lookup"><span data-stu-id="fd8a5-131">-Module</span></span>
<span data-ttu-id="fd8a5-132">Optionale Gruppe von Redis-Modulen, die in dieser Datenbank aktiviert werden sollen – Module können nur zur Erstellungszeit hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="fd8a5-133">Informationen zum Erstellen von #A0 finden Sie im Abschnitt "NOTES", und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd8a5-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fd8a5-134">-NoWait</span></span>
<span data-ttu-id="fd8a5-135">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fd8a5-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fd8a5-136">-Port</span><span class="sxs-lookup"><span data-stu-id="fd8a5-136">-Port</span></span>
<span data-ttu-id="fd8a5-137">Der TCP-Port des Datenbankendpunkts.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="fd8a5-138">Wird zur Erstellungszeit angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-138">Specified at create time.</span></span>
<span data-ttu-id="fd8a5-139">Standardmäßig wird ein verfügbarer Port verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="fd8a5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8a5-140">-ResourceGroupName</span></span>
<span data-ttu-id="fd8a5-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd8a5-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd8a5-142">-SubscriptionId</span></span>
<span data-ttu-id="fd8a5-143">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd8a5-144">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd8a5-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd8a5-145">-Confirm</span></span>
<span data-ttu-id="fd8a5-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8a5-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd8a5-147">-WhatIf</span></span>
<span data-ttu-id="fd8a5-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8a5-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8a5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8a5-150">CommonParameters</span></span>
<span data-ttu-id="fd8a5-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8a5-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd8a5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8a5-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd8a5-153">INPUTS</span></span>

### <span data-ttu-id="fd8a5-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="fd8a5-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="fd8a5-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd8a5-155">OUTPUTS</span></span>

### <span data-ttu-id="fd8a5-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="fd8a5-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="fd8a5-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd8a5-157">NOTES</span></span>

<span data-ttu-id="fd8a5-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fd8a5-158">ALIASES</span></span>

<span data-ttu-id="fd8a5-159">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="fd8a5-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd8a5-160">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd8a5-161">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd8a5-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fd8a5-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd8a5-163">`[ClusterName <String>]`: Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="fd8a5-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fd8a5-165">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="fd8a5-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd8a5-166">`[Location <String>]`: Der Bereich, in dem sich der Vorgang befindet.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="fd8a5-167">`[OperationId <String>]`: Der eindeutige Bezeichner des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="fd8a5-168">`[PrivateEndpointConnectionName <String>]`: Der Name der privaten Endpunktverbindung, die der Azure-Ressource zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="fd8a5-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="fd8a5-169">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="fd8a5-170">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="fd8a5-171">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="fd8a5-172">MODULE <IModule[]>: Optionale Gruppe von Redis-Modulen, die in dieser Datenbank aktiviert werden sollen – Module können nur zur Erstellungszeit hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="fd8a5-173">`Name <String>`: Der Name des Moduls, z. B. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="fd8a5-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="fd8a5-174">`[Arg <String>]`: Konfigurationsoptionen für das Modul, z. B. 'ERROR_RATE 0,00 INITIAL_SIZE 400'.</span><span class="sxs-lookup"><span data-stu-id="fd8a5-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="fd8a5-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd8a5-175">RELATED LINKS</span></span>

