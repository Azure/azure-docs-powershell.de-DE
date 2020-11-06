---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a5176dea9ca1cff125d615e4f2d8cd5447ea28e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496062"
---
# <span data-ttu-id="63e9d-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="63e9d-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="63e9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="63e9d-103">Entfernt eine Schlüsselspeicher-SAS-Definition für verwalteten Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="63e9d-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63e9d-104">SYNTAX</span></span>

### <span data-ttu-id="63e9d-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="63e9d-105">ByDefinitionName (Default)</span></span>
```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e9d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="63e9d-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultManagedStorageSasDefinition
 [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e9d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63e9d-107">DESCRIPTION</span></span>
<span data-ttu-id="63e9d-108">Entfernt eine Schlüsselspeicher-SAS-Definition für verwalteten Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="63e9d-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="63e9d-109">Dadurch wird auch der Schlüssel entfernt, der zum Abrufen des SAS-Tokens pro dieser SAS-Definition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63e9d-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="63e9d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63e9d-110">EXAMPLES</span></span>

### <span data-ttu-id="63e9d-111">Beispiel 1: Entfernen einer von Key Vault verwalteten Azure Storage SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="63e9d-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="63e9d-112">Entfernt eine Schlüsselspeicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="63e9d-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="63e9d-113">Beispiel 2: Entfernen einer von Key Vault verwalteten Azure Storage SAS-Definition ohne Bestätigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="63e9d-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="63e9d-114">Entfernt eine Schlüsselspeicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="63e9d-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="63e9d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="63e9d-115">PARAMETERS</span></span>

### <span data-ttu-id="63e9d-116">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="63e9d-116">-AccountName</span></span>
<span data-ttu-id="63e9d-117">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="63e9d-117">Storage account name.</span></span>
<span data-ttu-id="63e9d-118">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und dem Namen des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="63e9d-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e9d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e9d-119">-DefaultProfile</span></span>
<span data-ttu-id="63e9d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="63e9d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e9d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="63e9d-121">-Force</span></span>
<span data-ttu-id="63e9d-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="63e9d-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="63e9d-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="63e9d-123">-InputObject</span></span>
<span data-ttu-id="63e9d-124">ManagedStorageSasDefinition-Objekt.</span><span class="sxs-lookup"><span data-stu-id="63e9d-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63e9d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="63e9d-125">-Name</span></span>
<span data-ttu-id="63e9d-126">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="63e9d-126">Storage sas definition name.</span></span>
<span data-ttu-id="63e9d-127">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="63e9d-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e9d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63e9d-128">-PassThru</span></span>
<span data-ttu-id="63e9d-129">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="63e9d-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="63e9d-130">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="63e9d-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="63e9d-131">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="63e9d-131">-VaultName</span></span>
<span data-ttu-id="63e9d-132">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="63e9d-132">Vault name.</span></span>
<span data-ttu-id="63e9d-133">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="63e9d-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="63e9d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63e9d-134">-Confirm</span></span>
<span data-ttu-id="63e9d-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63e9d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e9d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e9d-136">-WhatIf</span></span>
<span data-ttu-id="63e9d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63e9d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e9d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63e9d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e9d-139">CommonParameters</span></span>
<span data-ttu-id="63e9d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e9d-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e9d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e9d-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63e9d-142">INPUTS</span></span>

### <span data-ttu-id="63e9d-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="63e9d-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>
<span data-ttu-id="63e9d-144">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63e9d-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="63e9d-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63e9d-145">OUTPUTS</span></span>

### <span data-ttu-id="63e9d-146">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="63e9d-146">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="63e9d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="63e9d-147">NOTES</span></span>

## <span data-ttu-id="63e9d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63e9d-148">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

