---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: b8297580f088678f1fdd61b8bff670adb03d2bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925267"
---
# <span data-ttu-id="12e88-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="12e88-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="12e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e88-102">SYNOPSIS</span></span>
<span data-ttu-id="12e88-103">Aktualisiert einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="12e88-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="12e88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e88-104">SYNTAX</span></span>

### <span data-ttu-id="12e88-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="12e88-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12e88-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="12e88-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="12e88-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e88-107">DESCRIPTION</span></span>
<span data-ttu-id="12e88-108">Aktualisiert einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="12e88-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="12e88-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12e88-109">EXAMPLES</span></span>

### <span data-ttu-id="12e88-110">Beispiel 1: Aktivieren der Datenverschlüsselung des App-Konfigurationsspeichers nach vom System zugewiesener verwalteter Identität</span><span class="sxs-lookup"><span data-stu-id="12e88-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="12e88-111">Dieser Befehl aktiviert die Datenverschlüsselung durch einen Schlüssel, der im Azure Key Vault gespeichert ist, und verwendet eine vom System zugewiesene verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="12e88-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="12e88-112">Der Tresor muss soft-delete und purge-protection aktiviert haben, und die verwaltete Identität muss über die folgenden Schlüsselberechtigungen verfügen: "Get", "wrapKey", "entwrapKey".</span><span class="sxs-lookup"><span data-stu-id="12e88-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="12e88-113">Beispiel 2: Aktivieren der Datenverschlüsselung des App-Konfigurationsspeichers nach vom Benutzer zugewiesener verwalteter Identität</span><span class="sxs-lookup"><span data-stu-id="12e88-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="12e88-114">Dieser Befehl aktiviert die Datenverschlüsselung durch einen Schlüssel, der im Azure Key Vault gespeichert ist, und verwendet eine vom Benutzer zugewiesene verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="12e88-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="12e88-115">Die vom Benutzer zugewiesene Identität muss mit festgelegt worden `-UserAssignedIdentity` sein.</span><span class="sxs-lookup"><span data-stu-id="12e88-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="12e88-116">Der Tresor muss soft-delete und purge-protection aktiviert haben, und die verwaltete Identität muss über die folgenden Schlüsselberechtigungen verfügen: "Get", "wrapKey", "entwrapKey".</span><span class="sxs-lookup"><span data-stu-id="12e88-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="12e88-117">Beispiel 3: Deaktivieren der Verschlüsselung eines App-Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="12e88-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="12e88-118">Mit diesem Befehl wird die Verschlüsselung eines App-Konfigurationsspeichers deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="12e88-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="12e88-119">Beispiel 3: Aktualisieren von Sku und Tag eines App-Konfigurationsspeichers per Pipeline.</span><span class="sxs-lookup"><span data-stu-id="12e88-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="12e88-120">Mit diesem Befehl werden Sku und Tag eines App-Konfigurationsspeichers per Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="12e88-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="12e88-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12e88-121">PARAMETERS</span></span>

### <span data-ttu-id="12e88-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12e88-122">-AsJob</span></span>
<span data-ttu-id="12e88-123">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="12e88-123">Run the command as a job</span></span>

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

### <span data-ttu-id="12e88-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e88-124">-DefaultProfile</span></span>
<span data-ttu-id="12e88-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12e88-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e88-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="12e88-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="12e88-127">Der URI des Schlüsseltresorschlüssels, der zum Verschlüsseln von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12e88-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="12e88-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="12e88-128">-IdentityType</span></span>
<span data-ttu-id="12e88-129">Der Typ der verwendeten verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="12e88-129">The type of managed identity used.</span></span>
<span data-ttu-id="12e88-130">Der Typ "SystemAssignedAndUserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Gruppe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="12e88-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="12e88-131">Der Typ "Keine" entfernt alle Identitäten.</span><span class="sxs-lookup"><span data-stu-id="12e88-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="12e88-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12e88-132">-InputObject</span></span>
<span data-ttu-id="12e88-133">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="12e88-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12e88-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="12e88-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="12e88-135">Die Client-ID der Identität, die für den Zugriff auf den Schlüsseltresor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12e88-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="12e88-136">-Name</span><span class="sxs-lookup"><span data-stu-id="12e88-136">-Name</span></span>
<span data-ttu-id="12e88-137">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="12e88-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="12e88-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12e88-138">-NoWait</span></span>
<span data-ttu-id="12e88-139">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="12e88-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12e88-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e88-140">-ResourceGroupName</span></span>
<span data-ttu-id="12e88-141">Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="12e88-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="12e88-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="12e88-142">-Sku</span></span>
<span data-ttu-id="12e88-143">Der SKU-Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="12e88-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="12e88-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e88-144">-SubscriptionId</span></span>
<span data-ttu-id="12e88-145">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="12e88-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="12e88-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="12e88-146">-Tag</span></span>
<span data-ttu-id="12e88-147">Die ARM Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="12e88-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="12e88-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="12e88-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="12e88-149">Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="12e88-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="12e88-150">Die vom Benutzer zugewiesenen Identitätswörterbuchschlüssel werden ARM Ressourcen-IDs im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12e88-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="12e88-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12e88-151">-Confirm</span></span>
<span data-ttu-id="12e88-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12e88-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e88-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e88-153">-WhatIf</span></span>
<span data-ttu-id="12e88-154">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12e88-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e88-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12e88-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e88-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e88-156">CommonParameters</span></span>
<span data-ttu-id="12e88-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e88-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e88-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12e88-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e88-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12e88-159">INPUTS</span></span>

### <span data-ttu-id="12e88-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="12e88-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="12e88-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12e88-161">OUTPUTS</span></span>

### <span data-ttu-id="12e88-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="12e88-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="12e88-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12e88-163">NOTES</span></span>

<span data-ttu-id="12e88-164">ALIASE</span><span class="sxs-lookup"><span data-stu-id="12e88-164">ALIASES</span></span>

<span data-ttu-id="12e88-165">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="12e88-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12e88-166">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="12e88-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12e88-167">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12e88-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12e88-168">INPUTOBJECT <IAppConfigurationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="12e88-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12e88-169">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="12e88-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="12e88-170">`[GroupName <String>]`: Der Name der Ressourcengruppe für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="12e88-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="12e88-171">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="12e88-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12e88-172">`[PrivateEndpointConnectionName <String>]`: Name der Privaten Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="12e88-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="12e88-173">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="12e88-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="12e88-174">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="12e88-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="12e88-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12e88-175">RELATED LINKS</span></span>



<span data-ttu-id="12e88-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="12e88-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

