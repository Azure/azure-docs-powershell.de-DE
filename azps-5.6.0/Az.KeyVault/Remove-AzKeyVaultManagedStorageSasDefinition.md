---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 844802c01b9b3bff7f59b795d5ba7712b9a7f4c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950216"
---
# <span data-ttu-id="70947-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="70947-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="70947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70947-102">SYNOPSIS</span></span>
<span data-ttu-id="70947-103">Entfernt eine verwaltete Azure Storage -SAS-Definition für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="70947-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="70947-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70947-104">SYNTAX</span></span>

### <span data-ttu-id="70947-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="70947-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70947-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="70947-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70947-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70947-107">DESCRIPTION</span></span>
<span data-ttu-id="70947-108">Entfernt eine verwaltete Azure Storage -SAS-Definition für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="70947-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="70947-109">Dadurch wird auch der Geheimtipp entfernt, der zum Abzurufen des SAS-Tokens nach dieser SAS-Definition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70947-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="70947-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70947-110">EXAMPLES</span></span>

### <span data-ttu-id="70947-111">Beispiel 1: Entfernen einer verwalteten Azure Storage SAS-Definition für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="70947-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
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

<span data-ttu-id="70947-112">Entfernt eine im Schlüsseltresor verwaltete Speicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="70947-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="70947-113">Beispiel 2: Entfernen einer verwalteten Azure Storage -SAS-Definition für den Schlüsseltresor ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="70947-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
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

<span data-ttu-id="70947-114">Entfernt eine im Schlüsseltresor verwaltete Speicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="70947-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="70947-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="70947-115">PARAMETERS</span></span>

### <span data-ttu-id="70947-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70947-116">-AccountName</span></span>
<span data-ttu-id="70947-117">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="70947-117">Storage account name.</span></span>
<span data-ttu-id="70947-118">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem Namen des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="70947-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="70947-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70947-119">-DefaultProfile</span></span>
<span data-ttu-id="70947-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="70947-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70947-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="70947-121">-Force</span></span>
<span data-ttu-id="70947-122">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="70947-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="70947-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70947-123">-InputObject</span></span>
<span data-ttu-id="70947-124">ManagedStorageSasDefinition-Objekt.</span><span class="sxs-lookup"><span data-stu-id="70947-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="70947-125">-Name</span><span class="sxs-lookup"><span data-stu-id="70947-125">-Name</span></span>
<span data-ttu-id="70947-126">Name der Speicher-SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="70947-126">Storage sas definition name.</span></span>
<span data-ttu-id="70947-127">Das Cmdlet erstellt den FQDN einer Speicher-SAS-Definition aus dem Tresornamen, der aktuell ausgewählten Umgebung, dem Namen des Speicherkontos und dem Sas-Definitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="70947-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="70947-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70947-128">-PassThru</span></span>
<span data-ttu-id="70947-129">Das Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="70947-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="70947-130">Wenn dieser Schalter angegeben ist, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="70947-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="70947-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70947-131">-VaultName</span></span>
<span data-ttu-id="70947-132">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="70947-132">Vault name.</span></span>
<span data-ttu-id="70947-133">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="70947-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="70947-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70947-134">-Confirm</span></span>
<span data-ttu-id="70947-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70947-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70947-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70947-136">-WhatIf</span></span>
<span data-ttu-id="70947-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70947-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70947-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70947-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70947-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70947-139">CommonParameters</span></span>
<span data-ttu-id="70947-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70947-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70947-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70947-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70947-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70947-142">INPUTS</span></span>

### <span data-ttu-id="70947-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="70947-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="70947-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70947-144">OUTPUTS</span></span>

### <span data-ttu-id="70947-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="70947-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="70947-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="70947-146">NOTES</span></span>

## <span data-ttu-id="70947-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="70947-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

