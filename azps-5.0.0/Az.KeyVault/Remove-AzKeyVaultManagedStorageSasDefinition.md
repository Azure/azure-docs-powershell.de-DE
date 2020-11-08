---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180413"
---
# <span data-ttu-id="8f666-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8f666-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8f666-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f666-102">SYNOPSIS</span></span>
<span data-ttu-id="8f666-103">Entfernt eine Schlüsselspeicher-SAS-Definition für verwalteten Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8f666-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="8f666-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f666-104">SYNTAX</span></span>

### <span data-ttu-id="8f666-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f666-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f666-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f666-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f666-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f666-107">DESCRIPTION</span></span>
<span data-ttu-id="8f666-108">Entfernt eine Schlüsselspeicher-SAS-Definition für verwalteten Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8f666-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="8f666-109">Dadurch wird auch der Schlüssel entfernt, der zum Abrufen des SAS-Tokens pro dieser SAS-Definition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f666-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="8f666-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f666-110">EXAMPLES</span></span>

### <span data-ttu-id="8f666-111">Beispiel 1: Entfernen einer von Key Vault verwalteten Azure Storage SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="8f666-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="8f666-112">Entfernt eine Schlüsselspeicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8f666-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="8f666-113">Beispiel 2: Entfernen einer von Key Vault verwalteten Azure Storage SAS-Definition ohne Bestätigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8f666-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="8f666-114">Entfernt eine Schlüsselspeicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8f666-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="8f666-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f666-115">PARAMETERS</span></span>

### <span data-ttu-id="8f666-116">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="8f666-116">-AccountName</span></span>
<span data-ttu-id="8f666-117">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8f666-117">Storage account name.</span></span>
<span data-ttu-id="8f666-118">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und dem Namen des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="8f666-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="8f666-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f666-119">-DefaultProfile</span></span>
<span data-ttu-id="8f666-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f666-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f666-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8f666-121">-Force</span></span>
<span data-ttu-id="8f666-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8f666-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8f666-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8f666-123">-InputObject</span></span>
<span data-ttu-id="8f666-124">ManagedStorageSasDefinition-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f666-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="8f666-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8f666-125">-Name</span></span>
<span data-ttu-id="8f666-126">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="8f666-126">Storage sas definition name.</span></span>
<span data-ttu-id="8f666-127">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="8f666-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="8f666-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f666-128">-PassThru</span></span>
<span data-ttu-id="8f666-129">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8f666-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8f666-130">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="8f666-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="8f666-131">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="8f666-131">-VaultName</span></span>
<span data-ttu-id="8f666-132">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="8f666-132">Vault name.</span></span>
<span data-ttu-id="8f666-133">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8f666-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8f666-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f666-134">-Confirm</span></span>
<span data-ttu-id="8f666-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f666-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f666-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f666-136">-WhatIf</span></span>
<span data-ttu-id="8f666-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f666-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f666-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f666-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f666-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f666-139">CommonParameters</span></span>
<span data-ttu-id="8f666-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f666-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f666-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f666-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f666-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f666-142">INPUTS</span></span>

### <span data-ttu-id="8f666-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8f666-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="8f666-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f666-144">OUTPUTS</span></span>

### <span data-ttu-id="8f666-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8f666-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8f666-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f666-146">NOTES</span></span>

## <span data-ttu-id="8f666-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f666-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

