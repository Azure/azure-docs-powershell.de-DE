---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 9859c6f17f393a5ca691c34e3ee144e24ab59fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663063"
---
# <span data-ttu-id="66533-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="66533-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="66533-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66533-102">SYNOPSIS</span></span>
<span data-ttu-id="66533-103">Entfernt eine Schlüsselspeicher-SAS-Definition für verwalteten Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="66533-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66533-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66533-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66533-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66533-105">DESCRIPTION</span></span>
<span data-ttu-id="66533-106">Entfernt eine Schlüsselspeicher-SAS-Definition für verwalteten Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="66533-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="66533-107">Dadurch wird auch der Schlüssel entfernt, der zum Abrufen des SAS-Tokens pro dieser SAS-Definition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66533-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="66533-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66533-108">EXAMPLES</span></span>

### <span data-ttu-id="66533-109">Beispiel 1: Entfernen einer von Key Vault verwalteten Azure Storage SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="66533-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="66533-110">Entfernt eine Schlüsselspeicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="66533-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="66533-111">Beispiel 2: Entfernen einer von Key Vault verwalteten Azure Storage SAS-Definition ohne Bestätigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="66533-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="66533-112">Entfernt eine Schlüsselspeicher-SAS-Definition "mysasdef", die dem Konto "mystorageaccount" im Tresor "myvault" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="66533-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="66533-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="66533-113">PARAMETERS</span></span>

### <span data-ttu-id="66533-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="66533-114">-AccountName</span></span>
<span data-ttu-id="66533-115">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="66533-115">Storage account name.</span></span>
<span data-ttu-id="66533-116">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und dem Namen des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="66533-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66533-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66533-117">-DefaultProfile</span></span>
<span data-ttu-id="66533-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="66533-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66533-119">-Force</span><span class="sxs-lookup"><span data-stu-id="66533-119">-Force</span></span>
<span data-ttu-id="66533-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="66533-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66533-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66533-121">-Name</span></span>
<span data-ttu-id="66533-122">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="66533-122">Storage sas definition name.</span></span>
<span data-ttu-id="66533-123">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="66533-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66533-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66533-124">-PassThru</span></span>
<span data-ttu-id="66533-125">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="66533-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="66533-126">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="66533-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66533-127">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="66533-127">-VaultName</span></span>
<span data-ttu-id="66533-128">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="66533-128">Vault name.</span></span>
<span data-ttu-id="66533-129">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="66533-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66533-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66533-130">-Confirm</span></span>
<span data-ttu-id="66533-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66533-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66533-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66533-132">-WhatIf</span></span>
<span data-ttu-id="66533-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66533-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66533-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66533-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66533-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66533-135">CommonParameters</span></span>
<span data-ttu-id="66533-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66533-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66533-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66533-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66533-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66533-138">INPUTS</span></span>

### <span data-ttu-id="66533-139">System. String</span><span class="sxs-lookup"><span data-stu-id="66533-139">System.String</span></span>

## <span data-ttu-id="66533-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66533-140">OUTPUTS</span></span>

### <span data-ttu-id="66533-141">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="66533-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="66533-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="66533-142">NOTES</span></span>

## <span data-ttu-id="66533-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66533-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

