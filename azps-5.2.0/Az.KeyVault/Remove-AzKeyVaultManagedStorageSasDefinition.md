---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291917"
---
# <span data-ttu-id="cae11-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="cae11-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cae11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae11-102">SYNOPSIS</span></span>
<span data-ttu-id="cae11-103">Entfernt eine im Schlüsseltresor verwaltete Azure Storage-SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="cae11-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="cae11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cae11-104">SYNTAX</span></span>

### <span data-ttu-id="cae11-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cae11-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae11-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cae11-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae11-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cae11-107">DESCRIPTION</span></span>
<span data-ttu-id="cae11-108">Entfernt eine im Schlüsseltresor verwaltete Azure Storage-SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="cae11-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="cae11-109">Dadurch wird auch der geheime Schlüssel entfernt, der zum Erhalten des SAS-Tokens nach dieser SAS-Definition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cae11-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="cae11-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cae11-110">EXAMPLES</span></span>

### <span data-ttu-id="cae11-111">Beispiel 1: Entfernen einer im Schlüsseltresor verwalteten Azure Storage-SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="cae11-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
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

<span data-ttu-id="cae11-112">Entfernt eine im Schlüsseltresor verwaltete Speicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cae11-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="cae11-113">Beispiel 2: Entfernen einer im Schlüsseltresor verwalteten Azure Storage-SAS-Definition ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="cae11-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
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

<span data-ttu-id="cae11-114">Entfernt eine im Schlüsseltresor verwaltete Speicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cae11-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="cae11-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cae11-115">PARAMETERS</span></span>

### <span data-ttu-id="cae11-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cae11-116">-AccountName</span></span>
<span data-ttu-id="cae11-117">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="cae11-117">Storage account name.</span></span>
<span data-ttu-id="cae11-118">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Namen des Tresors, der aktuell für die Umgebung und den Namen des Speicherkontos ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="cae11-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="cae11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae11-119">-DefaultProfile</span></span>
<span data-ttu-id="cae11-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cae11-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cae11-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cae11-121">-Force</span></span>
<span data-ttu-id="cae11-122">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="cae11-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cae11-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cae11-123">-InputObject</span></span>
<span data-ttu-id="cae11-124">ManagedStorageSasDefinition-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cae11-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="cae11-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cae11-125">-Name</span></span>
<span data-ttu-id="cae11-126">Name der Speicher-SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="cae11-126">Storage sas definition name.</span></span>
<span data-ttu-id="cae11-127">Das Cmdlet erstellt den FQDN einer Speicher-SAS-Definition aus dem Namen des Tresors, der aktuell ausgewählten Umgebung, dem Namen des Speicherkontos und dem Namen der Sasdefinition.</span><span class="sxs-lookup"><span data-stu-id="cae11-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="cae11-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cae11-128">-PassThru</span></span>
<span data-ttu-id="cae11-129">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cae11-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cae11-130">Wenn dieser Schalter angegeben ist, gibt das Cmdlet das konto für verwalteten Speicher zurück, das gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="cae11-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="cae11-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cae11-131">-VaultName</span></span>
<span data-ttu-id="cae11-132">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="cae11-132">Vault name.</span></span>
<span data-ttu-id="cae11-133">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="cae11-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="cae11-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cae11-134">-Confirm</span></span>
<span data-ttu-id="cae11-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cae11-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae11-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cae11-136">-WhatIf</span></span>
<span data-ttu-id="cae11-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cae11-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae11-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cae11-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae11-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae11-139">CommonParameters</span></span>
<span data-ttu-id="cae11-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae11-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae11-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cae11-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae11-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cae11-142">INPUTS</span></span>

### <span data-ttu-id="cae11-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cae11-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="cae11-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cae11-144">OUTPUTS</span></span>

### <span data-ttu-id="cae11-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="cae11-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cae11-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cae11-146">NOTES</span></span>

## <span data-ttu-id="cae11-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cae11-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

