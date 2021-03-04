---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: a8f90c2314ad645a8de3a72abc92928759e3b828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922976"
---
# <span data-ttu-id="57a15-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="57a15-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="57a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57a15-102">SYNOPSIS</span></span>
<span data-ttu-id="57a15-103">Stellt eine zuvor gelöschte SAS-Definition für verwalteten KeyVault-Speicher wiederher.</span><span class="sxs-lookup"><span data-stu-id="57a15-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="57a15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57a15-104">SYNTAX</span></span>

### <span data-ttu-id="57a15-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="57a15-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57a15-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="57a15-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57a15-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57a15-107">DESCRIPTION</span></span>
<span data-ttu-id="57a15-108">Mit **dem Befehl Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** wird eine zuvor gelöschte SAS-Definition für verwalteten Speicher wiederhergestellt, sofern für diesen Tresor die soft delete aktiviert ist und der Wiederherstellungsversuch während des Wiederherstellungsintervalls erfolgt.</span><span class="sxs-lookup"><span data-stu-id="57a15-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="57a15-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57a15-109">EXAMPLES</span></span>

### <span data-ttu-id="57a15-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57a15-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="57a15-111">Diese Reihenfolge von Befehlen bestimmt, ob die angegebene #A0 im Tresor in einem gelöschten Zustand vorhanden ist. Mit dem nachfolgenden Befehl wird die gelöschte Sas-Definition wiederhergestellt, und sie wird wieder in einen aktiven Zustand wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="57a15-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="57a15-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="57a15-112">PARAMETERS</span></span>

### <span data-ttu-id="57a15-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57a15-113">-AccountName</span></span>
<span data-ttu-id="57a15-114">Name des keyVault-verwalteten Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="57a15-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="57a15-115">Das Cmdlet erstellt den FQDN einer SAS-Definition für verwalteten Speicher aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem Namen des verwalteten Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="57a15-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a15-116">-DefaultProfile</span></span>
<span data-ttu-id="57a15-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57a15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a15-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57a15-118">-InputObject</span></span>
<span data-ttu-id="57a15-119">Gelöschtes SAS-Definitionsobjekt für verwalteten Speicher</span><span class="sxs-lookup"><span data-stu-id="57a15-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57a15-120">-Name</span><span class="sxs-lookup"><span data-stu-id="57a15-120">-Name</span></span>
<span data-ttu-id="57a15-121">Name der SAS-Definition für verwalteten KeyVault-Speicher.</span><span class="sxs-lookup"><span data-stu-id="57a15-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="57a15-122">Das Cmdlet erstellt den FQDN des Ziels aus dem Tresornamen, der aktuell ausgewählten Umgebung, dem Namen des verwalteten Speicherkontos und dem Namen der SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="57a15-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a15-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="57a15-123">-VaultName</span></span>
<span data-ttu-id="57a15-124">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="57a15-124">Vault name.</span></span>
<span data-ttu-id="57a15-125">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="57a15-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a15-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57a15-126">-Confirm</span></span>
<span data-ttu-id="57a15-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57a15-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a15-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a15-128">-WhatIf</span></span>
<span data-ttu-id="57a15-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57a15-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a15-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57a15-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a15-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a15-131">CommonParameters</span></span>
<span data-ttu-id="57a15-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a15-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a15-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57a15-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a15-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57a15-134">INPUTS</span></span>

### <span data-ttu-id="57a15-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57a15-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="57a15-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57a15-136">OUTPUTS</span></span>

### <span data-ttu-id="57a15-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="57a15-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="57a15-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="57a15-138">NOTES</span></span>

## <span data-ttu-id="57a15-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="57a15-139">RELATED LINKS</span></span>
