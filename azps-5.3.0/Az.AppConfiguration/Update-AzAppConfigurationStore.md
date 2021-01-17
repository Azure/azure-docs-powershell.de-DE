---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 8aea57e0c2bea5dbaa2e3233e886c97bfebe4bd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381434"
---
# <span data-ttu-id="58c72-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="58c72-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="58c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c72-102">SYNOPSIS</span></span>
<span data-ttu-id="58c72-103">Aktualisiert einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="58c72-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="58c72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c72-104">SYNTAX</span></span>

### <span data-ttu-id="58c72-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="58c72-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="58c72-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="58c72-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="58c72-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58c72-107">DESCRIPTION</span></span>
<span data-ttu-id="58c72-108">Aktualisiert einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="58c72-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="58c72-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58c72-109">EXAMPLES</span></span>

### <span data-ttu-id="58c72-110">Beispiel 1: Aktivieren der Datenverschlüsselung des App-Konfigurationsspeichers durch vom System zugewiesene verwaltete Identität</span><span class="sxs-lookup"><span data-stu-id="58c72-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="58c72-111">Dieser Befehl aktiviert die Datenverschlüsselung durch einen Schlüssel, der im Azure Key Vault gespeichert ist, und verwendet dazu eine vom System zugewiesene verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="58c72-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="58c72-112">Der Tresor muss den soft-delete- und purge-protection aktiviert haben, und die verwaltete Identität muss über die folgenden wichtigen Berechtigungen verfügen: "get", "wrapKey", "unwrapKey".</span><span class="sxs-lookup"><span data-stu-id="58c72-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="58c72-113">Beispiel 2: Aktivieren der Datenverschlüsselung des App-Konfigurationsspeichers durch vom Benutzer zugewiesene verwaltete Identität</span><span class="sxs-lookup"><span data-stu-id="58c72-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="58c72-114">Dieser Befehl aktiviert die Datenverschlüsselung durch einen Schlüssel, der im Azure Key Vault gespeichert ist, und verwendet dazu eine vom Benutzer zugewiesene verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="58c72-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="58c72-115">Die vom Benutzer zugewiesene Identität muss mit festgelegt worden `-UserAssignedIdentity` sein.</span><span class="sxs-lookup"><span data-stu-id="58c72-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="58c72-116">Der Tresor muss den soft-delete- und purge-protection aktiviert haben, und die verwaltete Identität muss über die folgenden wichtigen Berechtigungen verfügen: "get", "wrapKey", "unwrapKey".</span><span class="sxs-lookup"><span data-stu-id="58c72-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="58c72-117">Beispiel 3: Deaktivieren der Verschlüsselung eines App-Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="58c72-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="58c72-118">Mit diesem Befehl wird die Verschlüsselung eines App-Konfigurationsspeichers deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="58c72-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="58c72-119">Beispiel 3: Aktualisieren von SKU und Tag eines App-Konfigurationsspeichers nach Pipeline.</span><span class="sxs-lookup"><span data-stu-id="58c72-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="58c72-120">Mit diesem Befehl werden SKU und Tag eines App-Konfigurationsspeichers nach Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="58c72-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="58c72-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58c72-121">PARAMETERS</span></span>

### <span data-ttu-id="58c72-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58c72-122">-AsJob</span></span>
<span data-ttu-id="58c72-123">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="58c72-123">Run the command as a job</span></span>

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

### <span data-ttu-id="58c72-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c72-124">-DefaultProfile</span></span>
<span data-ttu-id="58c72-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58c72-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c72-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="58c72-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="58c72-127">Der URI des Schlüsseltresorschlüssels, der zum Verschlüsseln von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58c72-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="58c72-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="58c72-128">-IdentityType</span></span>
<span data-ttu-id="58c72-129">Der Typ der verwalteten Identität, die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58c72-129">The type of managed identity used.</span></span>
<span data-ttu-id="58c72-130">Der Typ "SystemAssignedAndUserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Reihe von benutzerzuweisungen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="58c72-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="58c72-131">Mit dem Typ "Keine" werden alle Identitäten entfernt.</span><span class="sxs-lookup"><span data-stu-id="58c72-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c72-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58c72-132">-InputObject</span></span>
<span data-ttu-id="58c72-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="58c72-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58c72-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="58c72-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="58c72-135">Die Client-ID der Identität, die für den Zugriff auf den Schlüsseltresor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58c72-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="58c72-136">-Name</span><span class="sxs-lookup"><span data-stu-id="58c72-136">-Name</span></span>
<span data-ttu-id="58c72-137">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="58c72-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="58c72-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="58c72-138">-NoWait</span></span>
<span data-ttu-id="58c72-139">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="58c72-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="58c72-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c72-140">-ResourceGroupName</span></span>
<span data-ttu-id="58c72-141">Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="58c72-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="58c72-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="58c72-142">-Sku</span></span>
<span data-ttu-id="58c72-143">Der Name der SKU des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="58c72-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="58c72-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58c72-144">-SubscriptionId</span></span>
<span data-ttu-id="58c72-145">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="58c72-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="58c72-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="58c72-146">-Tag</span></span>
<span data-ttu-id="58c72-147">Die ARM Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="58c72-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="58c72-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="58c72-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="58c72-149">Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="58c72-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="58c72-150">Die vom Benutzer zugewiesenen Identitätswörterbücher werden ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="58c72-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="58c72-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58c72-151">-Confirm</span></span>
<span data-ttu-id="58c72-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58c72-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c72-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="58c72-153">-WhatIf</span></span>
<span data-ttu-id="58c72-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58c72-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c72-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58c72-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c72-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c72-156">CommonParameters</span></span>
<span data-ttu-id="58c72-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c72-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c72-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58c72-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c72-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58c72-159">INPUTS</span></span>

### <span data-ttu-id="58c72-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="58c72-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="58c72-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58c72-161">OUTPUTS</span></span>

### <span data-ttu-id="58c72-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="58c72-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="58c72-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58c72-163">NOTES</span></span>

<span data-ttu-id="58c72-164">ALIASE</span><span class="sxs-lookup"><span data-stu-id="58c72-164">ALIASES</span></span>

<span data-ttu-id="58c72-165">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="58c72-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="58c72-166">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58c72-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58c72-167">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="58c72-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="58c72-168">INPUTOBJECT <IAppConfigurationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="58c72-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58c72-169">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="58c72-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="58c72-170">`[GroupName <String>]`: Der Name der Ressourcengruppe für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="58c72-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="58c72-171">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="58c72-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58c72-172">`[PrivateEndpointConnectionName <String>]`: Name der Verbindung für den privaten Endpunkt</span><span class="sxs-lookup"><span data-stu-id="58c72-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="58c72-173">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="58c72-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="58c72-174">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="58c72-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="58c72-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58c72-175">RELATED LINKS</span></span>



<span data-ttu-id="58c72-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="58c72-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

