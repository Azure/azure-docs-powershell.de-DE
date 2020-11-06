---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 317a7f72e68f442608a0b163afd99af6eaac28c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481161"
---
# <span data-ttu-id="75a5a-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="75a5a-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="75a5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="75a5a-103">Regeneriert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="75a5a-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75a5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a5a-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="75a5a-106">Generiert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher neu und legt den Schlüssel als aktiven Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="75a5a-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="75a5a-107">Der schlüsseltresor Proxys Ruft den Azure Resource Manager auf, um den Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="75a5a-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="75a5a-108">Der Aufrufer muss über die Berechtigungen zum erneuten Generieren von Schlüsseln für ein bestimmtes Azure Storage-Konto verfügen.</span><span class="sxs-lookup"><span data-stu-id="75a5a-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="75a5a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75a5a-109">EXAMPLES</span></span>

### <span data-ttu-id="75a5a-110">Beispiel 1: Erneutes Generieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="75a5a-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="75a5a-111">Regeneriert "key1" des Kontos "mystorageaccount" und legt "key1" als aktives des Vault Managed Azure-speicherkontos fest.</span><span class="sxs-lookup"><span data-stu-id="75a5a-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="75a5a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75a5a-112">PARAMETERS</span></span>

### <span data-ttu-id="75a5a-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="75a5a-113">-AccountName</span></span>
<span data-ttu-id="75a5a-114">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="75a5a-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="75a5a-115">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="75a5a-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a5a-116">-DefaultProfile</span></span>
<span data-ttu-id="75a5a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75a5a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75a5a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="75a5a-118">-Force</span></span>
<span data-ttu-id="75a5a-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="75a5a-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="75a5a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="75a5a-120">-KeyName</span></span>
<span data-ttu-id="75a5a-121">Name des Speicherkonto Schlüssels, der neu generiert und aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="75a5a-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a5a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75a5a-122">-PassThru</span></span>
<span data-ttu-id="75a5a-123">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="75a5a-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="75a5a-124">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="75a5a-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="75a5a-125">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="75a5a-125">-VaultName</span></span>
<span data-ttu-id="75a5a-126">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="75a5a-126">Vault name.</span></span>
<span data-ttu-id="75a5a-127">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="75a5a-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="75a5a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75a5a-128">-Confirm</span></span>
<span data-ttu-id="75a5a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75a5a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75a5a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a5a-130">-WhatIf</span></span>
<span data-ttu-id="75a5a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75a5a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a5a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75a5a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75a5a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a5a-133">CommonParameters</span></span>
<span data-ttu-id="75a5a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a5a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a5a-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a5a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a5a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75a5a-136">INPUTS</span></span>

### <span data-ttu-id="75a5a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="75a5a-137">System.String</span></span>

## <span data-ttu-id="75a5a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75a5a-138">OUTPUTS</span></span>

### <span data-ttu-id="75a5a-139">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75a5a-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="75a5a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="75a5a-140">NOTES</span></span>

## <span data-ttu-id="75a5a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75a5a-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

