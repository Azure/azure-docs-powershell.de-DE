---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176647"
---
# <span data-ttu-id="3b83b-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="3b83b-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="3b83b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b83b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b83b-103">Aktualisiert einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="3b83b-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="3b83b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b83b-104">SYNTAX</span></span>

### <span data-ttu-id="3b83b-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b83b-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b83b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3b83b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3b83b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b83b-107">DESCRIPTION</span></span>
<span data-ttu-id="3b83b-108">Aktualisiert einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="3b83b-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="3b83b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b83b-109">EXAMPLES</span></span>

### <span data-ttu-id="3b83b-110">Beispiel 1: Aktivieren der Datenverschlüsselung des App-conifguration-Speichers durch vom System zugewiesene verwaltete Identität</span><span class="sxs-lookup"><span data-stu-id="3b83b-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3b83b-111">Dieser Befehl ermöglicht die Datenverschlüsselung durch einen Schlüssel, der im Azure Key Vault mit einer vom System zugewiesenen verwalteten Identität gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3b83b-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="3b83b-112">Der Tresor muss den Soft-Delete-und Purge-Schutz aktiviert haben, und die verwaltete Identität muss über diese Schlüssel Berechtigungen verfügen: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="3b83b-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="3b83b-113">Beispiel 2: Aktivieren der Datenverschlüsselung des App-conifguration-Speichers nach vom Benutzer zugewiesene verwaltete Identität</span><span class="sxs-lookup"><span data-stu-id="3b83b-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="3b83b-114">Dieser Befehl ermöglicht die Datenverschlüsselung durch einen Schlüssel, der im Azure Key Vault mit einer vom Benutzer zugewiesenen verwalteten Identität gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3b83b-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="3b83b-115">Die vom Benutzer zugewiesene Identität muss mit gesetzt worden sein `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="3b83b-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="3b83b-116">Der Tresor muss den Soft-Delete-und Purge-Schutz aktiviert haben, und die verwaltete Identität muss über diese Schlüssel Berechtigungen verfügen: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="3b83b-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="3b83b-117">Beispiel 3: Deaktivieren der Verschlüsselung eines App-conifguration-Speichers</span><span class="sxs-lookup"><span data-stu-id="3b83b-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3b83b-118">Mit diesem Befehl wird die Verschlüsselung eines App-conifguration-Speichers deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b83b-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="3b83b-119">Beispiel 3: Aktualisieren von SKU und Tag eines App-conifguration-Speichers nach Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b83b-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3b83b-120">Dieser Befehl aktualisiert SKU und Tag eines App-conifguration-Speichers nach Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b83b-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="3b83b-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b83b-121">PARAMETERS</span></span>

### <span data-ttu-id="3b83b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b83b-122">-AsJob</span></span>
<span data-ttu-id="3b83b-123">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3b83b-123">Run the command as a job</span></span>

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

### <span data-ttu-id="3b83b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b83b-124">-DefaultProfile</span></span>
<span data-ttu-id="3b83b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b83b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b83b-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="3b83b-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="3b83b-127">Der URI des schlüsseltresor Schlüssels, der zum Verschlüsseln von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b83b-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="3b83b-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3b83b-128">-IdentityType</span></span>
<span data-ttu-id="3b83b-129">Der Typ der verwendeten verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="3b83b-129">The type of managed identity used.</span></span>
<span data-ttu-id="3b83b-130">Der Typ "SystemAssignedAndUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Reihe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="3b83b-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="3b83b-131">Der Typ "None" entfernt alle Identitäten.</span><span class="sxs-lookup"><span data-stu-id="3b83b-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="3b83b-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b83b-132">-InputObject</span></span>
<span data-ttu-id="3b83b-133">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3b83b-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b83b-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="3b83b-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="3b83b-135">Die Client-ID der Identität, die für den Zugriff auf Key Vault verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b83b-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="3b83b-136">-Name</span><span class="sxs-lookup"><span data-stu-id="3b83b-136">-Name</span></span>
<span data-ttu-id="3b83b-137">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="3b83b-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="3b83b-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3b83b-138">-NoWait</span></span>
<span data-ttu-id="3b83b-139">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3b83b-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b83b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b83b-140">-ResourceGroupName</span></span>
<span data-ttu-id="3b83b-141">Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="3b83b-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="3b83b-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="3b83b-142">-Sku</span></span>
<span data-ttu-id="3b83b-143">Der SKU-Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="3b83b-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="3b83b-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3b83b-144">-SubscriptionId</span></span>
<span data-ttu-id="3b83b-145">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3b83b-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="3b83b-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b83b-146">-Tag</span></span>
<span data-ttu-id="3b83b-147">Die Arm-Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="3b83b-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="3b83b-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3b83b-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="3b83b-149">Die Liste der Benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b83b-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="3b83b-150">Die vom Benutzer zugewiesenen ID-Wörterbuchschlüssel sind arm-Ressourcen-IDs in der Form: "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="3b83b-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="3b83b-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b83b-151">-Confirm</span></span>
<span data-ttu-id="3b83b-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b83b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b83b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b83b-153">-WhatIf</span></span>
<span data-ttu-id="3b83b-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b83b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b83b-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b83b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b83b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b83b-156">CommonParameters</span></span>
<span data-ttu-id="3b83b-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b83b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b83b-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b83b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b83b-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b83b-159">INPUTS</span></span>

### <span data-ttu-id="3b83b-160">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="3b83b-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="3b83b-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b83b-161">OUTPUTS</span></span>

### <span data-ttu-id="3b83b-162">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="3b83b-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="3b83b-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b83b-163">NOTES</span></span>

<span data-ttu-id="3b83b-164">Aliase</span><span class="sxs-lookup"><span data-stu-id="3b83b-164">ALIASES</span></span>

<span data-ttu-id="3b83b-165">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b83b-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b83b-166">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3b83b-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b83b-167">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3b83b-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b83b-168">Inputobject <IAppConfigurationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3b83b-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b83b-169">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="3b83b-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="3b83b-170">`[GroupName <String>]`: Der Name der privaten Link Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b83b-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="3b83b-171">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3b83b-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b83b-172">`[PrivateEndpointConnectionName <String>]`: Privater Endpunkt-Verbindungsname</span><span class="sxs-lookup"><span data-stu-id="3b83b-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="3b83b-173">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="3b83b-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="3b83b-174">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3b83b-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="3b83b-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b83b-175">RELATED LINKS</span></span>



<span data-ttu-id="3b83b-176">[Satz-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [Neu – AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="3b83b-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

