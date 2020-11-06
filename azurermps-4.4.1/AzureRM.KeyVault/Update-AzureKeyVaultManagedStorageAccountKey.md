---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 94e1b297879e31ff42f9c12c0e4ad4a601e5e163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501809"
---
# <span data-ttu-id="6707b-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6707b-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="6707b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6707b-102">SYNOPSIS</span></span>
<span data-ttu-id="6707b-103">Regeneriert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="6707b-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6707b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6707b-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6707b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6707b-105">DESCRIPTION</span></span>
<span data-ttu-id="6707b-106">Generiert den angegebenen Schlüssel des verwalteten Azure-speicherkontos für Schlüsselspeicher neu und legt den Schlüssel als aktiven Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="6707b-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="6707b-107">Der schlüsseltresor Proxys Ruft den Azure Resource Manager auf, um den Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6707b-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="6707b-108">Der Aufrufer muss über die Berechtigungen zum erneuten Generieren von Schlüsseln für ein bestimmtes Azure Storage-Konto verfügen.</span><span class="sxs-lookup"><span data-stu-id="6707b-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="6707b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6707b-109">EXAMPLES</span></span>

### <span data-ttu-id="6707b-110">Beispiel 1: Erneutes Generieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="6707b-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="6707b-111">Regeneriert "key1" des Kontos "mystorageaccount" und legt "key1" als aktives des Vault Managed Azure-speicherkontos fest.</span><span class="sxs-lookup"><span data-stu-id="6707b-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="6707b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6707b-112">PARAMETERS</span></span>

### <span data-ttu-id="6707b-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6707b-113">-AccountName</span></span>
<span data-ttu-id="6707b-114">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="6707b-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="6707b-115">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="6707b-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6707b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6707b-116">-Force</span></span>
<span data-ttu-id="6707b-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="6707b-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6707b-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6707b-118">-KeyName</span></span>
<span data-ttu-id="6707b-119">Name des Speicherkonto Schlüssels, der neu generiert und aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6707b-119">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="6707b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6707b-120">-PassThru</span></span>
<span data-ttu-id="6707b-121">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6707b-121">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6707b-122">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="6707b-122">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="6707b-123">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="6707b-123">-VaultName</span></span>
<span data-ttu-id="6707b-124">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="6707b-124">Vault name.</span></span>
<span data-ttu-id="6707b-125">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6707b-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6707b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6707b-126">-Confirm</span></span>
<span data-ttu-id="6707b-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6707b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6707b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6707b-128">-WhatIf</span></span>
<span data-ttu-id="6707b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6707b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6707b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6707b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6707b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6707b-131">-DefaultProfile</span></span>
<span data-ttu-id="6707b-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6707b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6707b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6707b-133">CommonParameters</span></span>
<span data-ttu-id="6707b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6707b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6707b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6707b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6707b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6707b-136">INPUTS</span></span>

### <span data-ttu-id="6707b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6707b-137">System.String</span></span>

## <span data-ttu-id="6707b-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6707b-138">OUTPUTS</span></span>

### <span data-ttu-id="6707b-139">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6707b-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="6707b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="6707b-140">NOTES</span></span>

## <span data-ttu-id="6707b-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6707b-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

