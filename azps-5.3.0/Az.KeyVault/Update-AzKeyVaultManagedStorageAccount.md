---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 72d23725f537df4f3e2244e799437394496bf434
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469512"
---
# <span data-ttu-id="fd76c-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fd76c-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fd76c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd76c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd76c-103">Aktualisieren bearbeitbarer Attribute eines verwalteten Azure Speicherkontos im Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="fd76c-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="fd76c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd76c-104">SYNTAX</span></span>

### <span data-ttu-id="fd76c-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd76c-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd76c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd76c-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd76c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd76c-107">DESCRIPTION</span></span>
<span data-ttu-id="fd76c-108">Aktualisieren Sie die bearbeitbaren Attribute eines verwalteten Azure Storage-Kontos im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="fd76c-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="fd76c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd76c-109">EXAMPLES</span></span>

### <span data-ttu-id="fd76c-110">Beispiel 1: Aktualisieren des aktiven Schlüssels auf "key2" für ein verwaltetes Azure -Speicherkonto im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="fd76c-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="fd76c-111">Aktualisiert den im Schlüsseltresor verwalteten aktiven Schlüssel "Azure Storage Account" auf "key2".</span><span class="sxs-lookup"><span data-stu-id="fd76c-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="fd76c-112">Nach diesem Update wird "key2" zum Generieren von SAS-Token verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd76c-112">'key2' will be used to generate SAS tokens after this update.</span></span>

### <span data-ttu-id="fd76c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd76c-113">Example 2</span></span>

<span data-ttu-id="fd76c-114">Aktualisieren bearbeitbarer Attribute eines verwalteten Azure Speicherkontos im Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="fd76c-114">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="fd76c-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="fd76c-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultManagedStorageAccount -AccountName 'mystorageaccount' -AutoRegenerateKey $false -RegenerationPeriod $regenerationPeriod -VaultName 'myvault'
```

## <span data-ttu-id="fd76c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd76c-116">PARAMETERS</span></span>

### <span data-ttu-id="fd76c-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd76c-117">-AccountName</span></span>
<span data-ttu-id="fd76c-118">Name des verwalteten Speicherkontos im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="fd76c-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="fd76c-119">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontos aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="fd76c-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-120">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="fd76c-120">-ActiveKeyName</span></span>
<span data-ttu-id="fd76c-121">Name des aktiven Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="fd76c-121">Active key name.</span></span>
<span data-ttu-id="fd76c-122">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Aktiven Schlüsselnamens des Verwalteten Speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="fd76c-122">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="fd76c-123">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="fd76c-123">-AutoRegenerateKey</span></span>
<span data-ttu-id="fd76c-124">Schlüssel automatisch neu generiert.</span><span class="sxs-lookup"><span data-stu-id="fd76c-124">Auto regenerate key.</span></span>
<span data-ttu-id="fd76c-125">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert für die automatische Neuintegärung des Verwalteten Speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="fd76c-125">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd76c-126">-DefaultProfile</span></span>
<span data-ttu-id="fd76c-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fd76c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd76c-128">-Enable</span><span class="sxs-lookup"><span data-stu-id="fd76c-128">-Enable</span></span>
<span data-ttu-id="fd76c-129">Wenn vorhanden, kann ein verwalteter Speicherkontoschlüssel für die Sastokengenerierung verwendet werden, wenn der Wert wahr ist.</span><span class="sxs-lookup"><span data-stu-id="fd76c-129">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="fd76c-130">Deaktiviert die Verwendung eines verwalteten Speicherkontoschlüssels für die Sastokengenerierung, wenn der Wert falsch ist.</span><span class="sxs-lookup"><span data-stu-id="fd76c-130">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="fd76c-131">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Status "Aktiviert/Deaktiviert" des Speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="fd76c-131">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd76c-132">-InputObject</span></span>
<span data-ttu-id="fd76c-133">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fd76c-133">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd76c-134">-PassThru</span></span>
<span data-ttu-id="fd76c-135">Das Cmdlet gibt das Objekt standardmäßig nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="fd76c-135">Cmdlet does not return object by default.</span></span> <span data-ttu-id="fd76c-136">Wenn dieser Schalter angegeben ist, geben Sie das Objekt für das verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="fd76c-136">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="fd76c-137">-Destimperiod</span><span class="sxs-lookup"><span data-stu-id="fd76c-137">-RegenerationPeriod</span></span>
<span data-ttu-id="fd76c-138">Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="fd76c-138">Regeneration period.</span></span> <span data-ttu-id="fd76c-139">Wenn die automatische erneut generierte Taste aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der die inaktiven Keygets des verwalteten Speicherkontos automatisch neu generiert und zum aktiven Schlüssel werden.</span><span class="sxs-lookup"><span data-stu-id="fd76c-139">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="fd76c-140">Wenn nichts angegeben wird, bleibt der vorhandene Wert des Zeitraums der Schlüssel eines verwalteten Speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="fd76c-140">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd76c-141">-Tag</span></span>
<span data-ttu-id="fd76c-142">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fd76c-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fd76c-143">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="fd76c-143">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd76c-144">-VaultName</span></span>
<span data-ttu-id="fd76c-145">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="fd76c-145">Vault name.</span></span>
<span data-ttu-id="fd76c-146">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="fd76c-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd76c-147">-Confirm</span></span>
<span data-ttu-id="fd76c-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd76c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd76c-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd76c-149">-WhatIf</span></span>
<span data-ttu-id="fd76c-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd76c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd76c-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd76c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd76c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd76c-152">CommonParameters</span></span>
<span data-ttu-id="fd76c-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd76c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd76c-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd76c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd76c-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd76c-155">INPUTS</span></span>

### <span data-ttu-id="fd76c-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fd76c-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="fd76c-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd76c-157">OUTPUTS</span></span>

### <span data-ttu-id="fd76c-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fd76c-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fd76c-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd76c-159">NOTES</span></span>

## <span data-ttu-id="fd76c-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd76c-160">RELATED LINKS</span></span>

[<span data-ttu-id="fd76c-161">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fd76c-161">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
