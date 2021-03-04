---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: d6b030cfbc6233d917d252f2d271eb7d4bfe65bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943864"
---
# <span data-ttu-id="339c5-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="339c5-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="339c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339c5-102">SYNOPSIS</span></span>
<span data-ttu-id="339c5-103">Löscht einen RedisEnterprise-Cachecluster.</span><span class="sxs-lookup"><span data-stu-id="339c5-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="339c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="339c5-104">SYNTAX</span></span>

### <span data-ttu-id="339c5-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="339c5-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="339c5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="339c5-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="339c5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="339c5-107">DESCRIPTION</span></span>
<span data-ttu-id="339c5-108">Löscht einen RedisEnterprise-Cachecluster.</span><span class="sxs-lookup"><span data-stu-id="339c5-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="339c5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="339c5-109">EXAMPLES</span></span>

### <span data-ttu-id="339c5-110">Beispiel 1: Entfernen eines Redis Enterprise-Caches und Zurückgeben des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="339c5-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="339c5-111">Mit diesem Befehl wird ein Redis Enterprise Cache entfernt und angezeigt, ob der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="339c5-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="339c5-112">Beispiel 2: Entfernen eines Redis Enterprise-Caches und Nichtanzeige des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="339c5-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="339c5-113">Mit diesem Befehl wird ein Redis Enterprise Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="339c5-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="339c5-114">Da der Parameter PassThru nicht angegeben ist, wird das Ergebnis des Vorgangs nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="339c5-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="339c5-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="339c5-115">PARAMETERS</span></span>

### <span data-ttu-id="339c5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="339c5-116">-AsJob</span></span>
<span data-ttu-id="339c5-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="339c5-117">Run the command as a job</span></span>

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

### <span data-ttu-id="339c5-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="339c5-118">-ClusterName</span></span>
<span data-ttu-id="339c5-119">Der Name des RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="339c5-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339c5-120">-DefaultProfile</span></span>
<span data-ttu-id="339c5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="339c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339c5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="339c5-122">-InputObject</span></span>
<span data-ttu-id="339c5-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="339c5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="339c5-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="339c5-124">-NoWait</span></span>
<span data-ttu-id="339c5-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="339c5-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="339c5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="339c5-126">-PassThru</span></span>
<span data-ttu-id="339c5-127">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="339c5-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="339c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="339c5-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="339c5-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339c5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="339c5-130">-SubscriptionId</span></span>
<span data-ttu-id="339c5-131">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="339c5-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="339c5-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="339c5-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339c5-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="339c5-133">-Confirm</span></span>
<span data-ttu-id="339c5-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="339c5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339c5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339c5-135">-WhatIf</span></span>
<span data-ttu-id="339c5-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="339c5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339c5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="339c5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339c5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339c5-138">CommonParameters</span></span>
<span data-ttu-id="339c5-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339c5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339c5-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="339c5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339c5-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="339c5-141">INPUTS</span></span>

### <span data-ttu-id="339c5-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="339c5-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="339c5-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="339c5-143">OUTPUTS</span></span>

### <span data-ttu-id="339c5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="339c5-144">System.Boolean</span></span>

## <span data-ttu-id="339c5-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="339c5-145">NOTES</span></span>

<span data-ttu-id="339c5-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="339c5-146">ALIASES</span></span>

<span data-ttu-id="339c5-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="339c5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="339c5-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="339c5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="339c5-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="339c5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="339c5-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="339c5-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="339c5-151">`[ClusterName <String>]`: Der Name des RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="339c5-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="339c5-152">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="339c5-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="339c5-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="339c5-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="339c5-154">`[Location <String>]`: Der Bereich, in dem sich der Vorgang befindet.</span><span class="sxs-lookup"><span data-stu-id="339c5-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="339c5-155">`[OperationId <String>]`: Der eindeutige Bezeichner des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="339c5-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="339c5-156">`[PrivateEndpointConnectionName <String>]`: Der Name der privaten Endpunktverbindung, die der Azure-Ressource zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="339c5-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="339c5-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="339c5-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="339c5-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="339c5-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="339c5-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="339c5-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="339c5-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="339c5-160">RELATED LINKS</span></span>

