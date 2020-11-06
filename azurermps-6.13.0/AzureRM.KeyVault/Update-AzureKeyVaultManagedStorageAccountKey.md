---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 2e096b04830d50840d6298e7aa8085b0090a347e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502082"
---
# <span data-ttu-id="ff80f-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff80f-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="ff80f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff80f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff80f-103">Regeneriert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="ff80f-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff80f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff80f-104">SYNTAX</span></span>

### <span data-ttu-id="ff80f-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff80f-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff80f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff80f-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff80f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff80f-107">DESCRIPTION</span></span>
<span data-ttu-id="ff80f-108">Generiert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher neu und legt den Schlüssel als aktiven Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="ff80f-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="ff80f-109">Der schlüsseltresor Proxys Ruft den Azure Resource Manager auf, um den Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ff80f-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="ff80f-110">Der Aufrufer muss über die Berechtigungen zum erneuten Generieren von Schlüsseln für ein bestimmtes Azure Storage-Konto verfügen.</span><span class="sxs-lookup"><span data-stu-id="ff80f-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="ff80f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff80f-111">EXAMPLES</span></span>

### <span data-ttu-id="ff80f-112">Beispiel 1: Erneutes Generieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ff80f-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="ff80f-113">Regeneriert "key1" des Kontos "mystorageaccount" und legt "key1" als aktives des Vault Managed Azure-speicherkontos fest.</span><span class="sxs-lookup"><span data-stu-id="ff80f-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ff80f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff80f-114">PARAMETERS</span></span>

### <span data-ttu-id="ff80f-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ff80f-115">-AccountName</span></span>
<span data-ttu-id="ff80f-116">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="ff80f-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="ff80f-117">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="ff80f-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="ff80f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff80f-118">-DefaultProfile</span></span>
<span data-ttu-id="ff80f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ff80f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff80f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ff80f-120">-Force</span></span>
<span data-ttu-id="ff80f-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="ff80f-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ff80f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ff80f-122">-InputObject</span></span>
<span data-ttu-id="ff80f-123">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff80f-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="ff80f-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ff80f-124">-KeyName</span></span>
<span data-ttu-id="ff80f-125">Name des Speicherkonto Schlüssels, der neu generiert und aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff80f-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff80f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff80f-126">-PassThru</span></span>
<span data-ttu-id="ff80f-127">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ff80f-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ff80f-128">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="ff80f-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="ff80f-129">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="ff80f-129">-VaultName</span></span>
<span data-ttu-id="ff80f-130">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="ff80f-130">Vault name.</span></span>
<span data-ttu-id="ff80f-131">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ff80f-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ff80f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff80f-132">-Confirm</span></span>
<span data-ttu-id="ff80f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff80f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff80f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff80f-134">-WhatIf</span></span>
<span data-ttu-id="ff80f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff80f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff80f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff80f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff80f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff80f-137">CommonParameters</span></span>
<span data-ttu-id="ff80f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff80f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff80f-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff80f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff80f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff80f-140">INPUTS</span></span>

### <span data-ttu-id="ff80f-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ff80f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="ff80f-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff80f-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ff80f-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff80f-143">OUTPUTS</span></span>

### <span data-ttu-id="ff80f-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff80f-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ff80f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff80f-145">NOTES</span></span>

## <span data-ttu-id="ff80f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff80f-146">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

