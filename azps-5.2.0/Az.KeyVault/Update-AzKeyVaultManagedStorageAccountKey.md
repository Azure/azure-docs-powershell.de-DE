---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295216"
---
# <span data-ttu-id="4f8ea-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4f8ea-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="4f8ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8ea-103">Generiert den angegebenen Schlüssel des verwalteten Azure -Speicherkontos im Schlüsseltresor erneut.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="4f8ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f8ea-104">SYNTAX</span></span>

### <span data-ttu-id="4f8ea-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f8ea-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4f8ea-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f8ea-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f8ea-107">DESCRIPTION</span></span>
<span data-ttu-id="4f8ea-108">Generiert den angegebenen Schlüssel des im Schlüsseltresor verwalteten Azure -Speicherkontos erneut und legt den Schlüssel als aktiven Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="4f8ea-109">Der Schlüsseltresor proxys den Aufruf von Azure Resource Manager, um den Schlüssel erneut zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="4f8ea-110">Der Aufrufer muss Berechtigungen zum erneuten Generieren von Schlüsseln für ein bestimmtes Azure -Speicherkonto besitzen.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="4f8ea-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f8ea-111">EXAMPLES</span></span>

### <span data-ttu-id="4f8ea-112">Beispiel 1: Erneutererieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="4f8ea-112">Example 1: Regenerate a key</span></span>
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

<span data-ttu-id="4f8ea-113">Generiert "key1" des Kontos "mystorageaccount" erneut und legt "key1" als aktives Konto des verwalteten Key Vault Azure Storage Account fest.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="4f8ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f8ea-114">PARAMETERS</span></span>

### <span data-ttu-id="4f8ea-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f8ea-115">-AccountName</span></span>
<span data-ttu-id="4f8ea-116">Name des verwalteten Speicherkontos im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="4f8ea-117">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontos aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="4f8ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8ea-118">-DefaultProfile</span></span>
<span data-ttu-id="4f8ea-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4f8ea-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f8ea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4f8ea-120">-Force</span></span>
<span data-ttu-id="4f8ea-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4f8ea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f8ea-122">-InputObject</span></span>
<span data-ttu-id="4f8ea-123">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="4f8ea-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4f8ea-124">-KeyName</span></span>
<span data-ttu-id="4f8ea-125">Name des Speicherkontoschlüssels zum erneuten Erstellen und Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="4f8ea-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f8ea-126">-PassThru</span></span>
<span data-ttu-id="4f8ea-127">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4f8ea-128">Wenn dieser Schalter angegeben ist, gibt das Cmdlet das konto für verwalteten Speicher zurück, das gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="4f8ea-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4f8ea-129">-VaultName</span></span>
<span data-ttu-id="4f8ea-130">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-130">Vault name.</span></span>
<span data-ttu-id="4f8ea-131">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4f8ea-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f8ea-132">-Confirm</span></span>
<span data-ttu-id="4f8ea-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8ea-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f8ea-134">-WhatIf</span></span>
<span data-ttu-id="4f8ea-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f8ea-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8ea-137">CommonParameters</span></span>
<span data-ttu-id="4f8ea-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8ea-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f8ea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8ea-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8ea-140">INPUTS</span></span>

### <span data-ttu-id="4f8ea-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4f8ea-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="4f8ea-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8ea-142">OUTPUTS</span></span>

### <span data-ttu-id="4f8ea-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f8ea-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4f8ea-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f8ea-144">NOTES</span></span>

## <span data-ttu-id="4f8ea-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f8ea-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

