---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 80ff79e71498cc76479592b65207da09fabed6a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931083"
---
# <span data-ttu-id="2d90d-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2d90d-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="2d90d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d90d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d90d-103">Regeneriert den angegebenen Schlüssel des verwalteten Azure -Speicherkontos für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="2d90d-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2d90d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d90d-104">SYNTAX</span></span>

### <span data-ttu-id="2d90d-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d90d-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d90d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2d90d-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d90d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d90d-107">DESCRIPTION</span></span>
<span data-ttu-id="2d90d-108">Regeneriert den angegebenen Schlüssel des verwalteten Azure -Speicherkontos für den Schlüsseltresor und legt den Schlüssel als aktiven Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="2d90d-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="2d90d-109">Der Schlüsseltresor proxiert den Aufruf von Azure Resource Manager, um den Schlüssel zu regenerieren.</span><span class="sxs-lookup"><span data-stu-id="2d90d-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="2d90d-110">Der Aufrufer muss Berechtigungen zum Erneuten generieren von Schlüsseln für ein bestimmtes Azure Storage-Konto bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2d90d-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="2d90d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d90d-111">EXAMPLES</span></span>

### <span data-ttu-id="2d90d-112">Beispiel 1: Neuerieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="2d90d-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

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

<span data-ttu-id="2d90d-113">Regeneriert "key1" des Kontos "mystorageaccount" und legt "key1" als aktiv des verwalteten Azure -Speicherkontos für den Schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="2d90d-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2d90d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d90d-114">PARAMETERS</span></span>

### <span data-ttu-id="2d90d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d90d-115">-AccountName</span></span>
<span data-ttu-id="2d90d-116">Name des verwalteten Speicherkontos für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="2d90d-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="2d90d-117">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="2d90d-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="2d90d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d90d-118">-DefaultProfile</span></span>
<span data-ttu-id="2d90d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2d90d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d90d-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2d90d-120">-Force</span></span>
<span data-ttu-id="2d90d-121">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="2d90d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2d90d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d90d-122">-InputObject</span></span>
<span data-ttu-id="2d90d-123">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d90d-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="2d90d-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2d90d-124">-KeyName</span></span>
<span data-ttu-id="2d90d-125">Name des Speicherkontoschlüssels zum Regenerieren und Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2d90d-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="2d90d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d90d-126">-PassThru</span></span>
<span data-ttu-id="2d90d-127">Das Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2d90d-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2d90d-128">Wenn dieser Schalter angegeben ist, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="2d90d-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="2d90d-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2d90d-129">-VaultName</span></span>
<span data-ttu-id="2d90d-130">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="2d90d-130">Vault name.</span></span>
<span data-ttu-id="2d90d-131">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2d90d-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2d90d-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d90d-132">-Confirm</span></span>
<span data-ttu-id="2d90d-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d90d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d90d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d90d-134">-WhatIf</span></span>
<span data-ttu-id="2d90d-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d90d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d90d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d90d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d90d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d90d-137">CommonParameters</span></span>
<span data-ttu-id="2d90d-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d90d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d90d-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d90d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d90d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d90d-140">INPUTS</span></span>

### <span data-ttu-id="2d90d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2d90d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="2d90d-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d90d-142">OUTPUTS</span></span>

### <span data-ttu-id="2d90d-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d90d-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2d90d-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d90d-144">NOTES</span></span>

## <span data-ttu-id="2d90d-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d90d-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

