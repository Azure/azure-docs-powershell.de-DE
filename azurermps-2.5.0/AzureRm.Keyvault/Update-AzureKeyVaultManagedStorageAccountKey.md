---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: d7bd1e776cc0593f57a17e8d83ecde3f6981973b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849280"
---
# <span data-ttu-id="dccc4-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dccc4-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="dccc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dccc4-102">SYNOPSIS</span></span>
<span data-ttu-id="dccc4-103">Regeneriert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="dccc4-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dccc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dccc4-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dccc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccc4-105">DESCRIPTION</span></span>
<span data-ttu-id="dccc4-106">Generiert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher neu und legt den Schlüssel als aktiven Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="dccc4-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="dccc4-107">Der schlüsseltresor Proxys Ruft den Azure Resource Manager auf, um den Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="dccc4-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="dccc4-108">Der Aufrufer muss über die Berechtigungen zum erneuten Generieren von Schlüsseln für ein bestimmtes Azure Storage-Konto verfügen.</span><span class="sxs-lookup"><span data-stu-id="dccc4-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="dccc4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dccc4-109">EXAMPLES</span></span>

### <span data-ttu-id="dccc4-110">Beispiel 1: Erneutes Generieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="dccc4-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="dccc4-111">Regeneriert "key1" des Kontos "mystorageaccount" und legt "key1" als aktives des Vault Managed Azure-speicherkontos fest.</span><span class="sxs-lookup"><span data-stu-id="dccc4-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="dccc4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccc4-112">PARAMETERS</span></span>

### <span data-ttu-id="dccc4-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="dccc4-113">-AccountName</span></span>
<span data-ttu-id="dccc4-114">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="dccc4-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="dccc4-115">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="dccc4-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="dccc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccc4-116">-DefaultProfile</span></span>
<span data-ttu-id="dccc4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dccc4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dccc4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dccc4-118">-Force</span></span>
<span data-ttu-id="dccc4-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="dccc4-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dccc4-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dccc4-120">-KeyName</span></span>
<span data-ttu-id="dccc4-121">Name des Speicherkonto Schlüssels, der neu generiert und aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dccc4-121">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="dccc4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dccc4-122">-PassThru</span></span>
<span data-ttu-id="dccc4-123">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="dccc4-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dccc4-124">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="dccc4-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="dccc4-125">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="dccc4-125">-VaultName</span></span>
<span data-ttu-id="dccc4-126">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="dccc4-126">Vault name.</span></span>
<span data-ttu-id="dccc4-127">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="dccc4-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="dccc4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dccc4-128">-Confirm</span></span>
<span data-ttu-id="dccc4-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dccc4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dccc4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dccc4-130">-WhatIf</span></span>
<span data-ttu-id="dccc4-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dccc4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dccc4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dccc4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dccc4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccc4-133">CommonParameters</span></span>
<span data-ttu-id="dccc4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccc4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccc4-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dccc4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccc4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dccc4-136">INPUTS</span></span>

### <span data-ttu-id="dccc4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dccc4-137">System.String</span></span>

## <span data-ttu-id="dccc4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dccc4-138">OUTPUTS</span></span>

### <span data-ttu-id="dccc4-139">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dccc4-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="dccc4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="dccc4-140">NOTES</span></span>

## <span data-ttu-id="dccc4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dccc4-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

