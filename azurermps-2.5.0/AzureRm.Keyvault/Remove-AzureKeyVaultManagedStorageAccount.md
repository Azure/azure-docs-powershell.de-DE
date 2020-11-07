---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 438d36a5c9081da3124c0ef5ee03c7eb9ad8f634
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848219"
---
# <span data-ttu-id="57334-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57334-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="57334-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57334-102">SYNOPSIS</span></span>
<span data-ttu-id="57334-103">Entfernt ein zentrales Vault Managed Azure-Speicherkonto und alle zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="57334-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57334-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57334-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57334-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57334-105">DESCRIPTION</span></span>
<span data-ttu-id="57334-106">Trennt ein Azure Storage-Konto von Key Vault.</span><span class="sxs-lookup"><span data-stu-id="57334-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="57334-107">Dadurch wird kein Azure-Speicherkonto entfernt, aber die Kontoschlüssel werden vom Azure Key Vault verwaltet.</span><span class="sxs-lookup"><span data-stu-id="57334-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="57334-108">Alle zugehörigen Schlüsselspeicher-SAS-Definitionen für den Speicher werden ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="57334-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="57334-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57334-109">EXAMPLES</span></span>

### <span data-ttu-id="57334-110">Beispiel 1: Entfernen eines zentralen Vault Managed Azure-speicherkontos und aller zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="57334-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="57334-111">Trennt das Azure-Speicherkonto "mystorageaccount" vom schlüsseltresor "myvault" ab und verhindert, dass die Schlüssel von Key Vault verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="57334-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="57334-112">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="57334-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="57334-113">Alle mit diesem Konto verknüpften Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="57334-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="57334-114">Beispiel 2: Entfernen eines zentralen Vault Managed Azure-speicherkontos und aller zugehörigen SAS-Definitionen ohne Bestätigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="57334-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="57334-115">Trennt das Azure-Speicherkonto "mystorageaccount" vom schlüsseltresor "myvault" ab und verhindert, dass die Schlüssel von Key Vault verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="57334-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="57334-116">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="57334-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="57334-117">Alle mit diesem Konto verknüpften Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="57334-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="57334-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="57334-118">PARAMETERS</span></span>

### <span data-ttu-id="57334-119">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="57334-119">-AccountName</span></span>
<span data-ttu-id="57334-120">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="57334-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="57334-121">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="57334-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="57334-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57334-122">-DefaultProfile</span></span>
<span data-ttu-id="57334-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="57334-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57334-124">-Force</span><span class="sxs-lookup"><span data-stu-id="57334-124">-Force</span></span>
<span data-ttu-id="57334-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="57334-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="57334-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57334-126">-PassThru</span></span>
<span data-ttu-id="57334-127">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="57334-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="57334-128">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="57334-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="57334-129">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="57334-129">-VaultName</span></span>
<span data-ttu-id="57334-130">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="57334-130">Vault name.</span></span>
<span data-ttu-id="57334-131">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="57334-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="57334-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57334-132">-Confirm</span></span>
<span data-ttu-id="57334-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57334-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57334-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57334-134">-WhatIf</span></span>
<span data-ttu-id="57334-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57334-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57334-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57334-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57334-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57334-137">CommonParameters</span></span>
<span data-ttu-id="57334-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57334-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57334-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57334-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57334-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57334-140">INPUTS</span></span>

### <span data-ttu-id="57334-141">System. String</span><span class="sxs-lookup"><span data-stu-id="57334-141">System.String</span></span>

## <span data-ttu-id="57334-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57334-142">OUTPUTS</span></span>

### <span data-ttu-id="57334-143">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57334-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="57334-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="57334-144">NOTES</span></span>

## <span data-ttu-id="57334-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57334-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

