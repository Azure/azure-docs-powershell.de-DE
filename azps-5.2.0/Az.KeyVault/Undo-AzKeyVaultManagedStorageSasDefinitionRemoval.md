---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295270"
---
# <span data-ttu-id="531bf-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="531bf-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="531bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531bf-102">SYNOPSIS</span></span>
<span data-ttu-id="531bf-103">Stellt eine zuvor gelöschte SAS-Definition für verwalteten KeyVault-Speicher wiederher.</span><span class="sxs-lookup"><span data-stu-id="531bf-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="531bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="531bf-104">SYNTAX</span></span>

### <span data-ttu-id="531bf-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="531bf-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="531bf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="531bf-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="531bf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="531bf-107">DESCRIPTION</span></span>
<span data-ttu-id="531bf-108">Mit dem Befehl **"Undo-AzKeyVaultManagedStorageSasDefinitionRemoval"** wird eine zuvor gelöschte SAS-Definition für verwalteten Speicher wiederhergestellt, sofern für diesen Tresor das weiche Löschen aktiviert ist und der Wiederherstellungsversuch während des Wiederherstellungsintervalls erfolgt.</span><span class="sxs-lookup"><span data-stu-id="531bf-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="531bf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="531bf-109">EXAMPLES</span></span>

### <span data-ttu-id="531bf-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="531bf-110">Example 1</span></span>
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

<span data-ttu-id="531bf-111">Diese Abfolge von Befehlen bestimmt, ob die angegebene Speicher-SAS-Definition im Tresor in einem gelöschten Zustand vorhanden ist. Mit dem nachfolgenden Befehl wird die gelöschte Sasdefinition wiederhergestellt, und der aktive Zustand wird wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="531bf-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="531bf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="531bf-112">PARAMETERS</span></span>

### <span data-ttu-id="531bf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="531bf-113">-AccountName</span></span>
<span data-ttu-id="531bf-114">Name des von KeyVault verwalteten Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="531bf-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="531bf-115">Das Cmdlet erstellt den FQDN einer SAS-Definition für verwalteten Speicher aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem Namen des verwalteten Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="531bf-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="531bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531bf-116">-DefaultProfile</span></span>
<span data-ttu-id="531bf-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="531bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="531bf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="531bf-118">-InputObject</span></span>
<span data-ttu-id="531bf-119">Deleted managed storage SAS definition object</span><span class="sxs-lookup"><span data-stu-id="531bf-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="531bf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="531bf-120">-Name</span></span>
<span data-ttu-id="531bf-121">Name der SAS-Definition für verwalteten KeyVault-Speicher.</span><span class="sxs-lookup"><span data-stu-id="531bf-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="531bf-122">Das Cmdlet erstellt den FQDN des Ziels aus dem Namen des Tresors, der aktuell ausgewählten Umgebung, dem Namen des verwalteten Speicherkontos und dem Namen der SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="531bf-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="531bf-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="531bf-123">-VaultName</span></span>
<span data-ttu-id="531bf-124">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="531bf-124">Vault name.</span></span>
<span data-ttu-id="531bf-125">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="531bf-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="531bf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="531bf-126">-Confirm</span></span>
<span data-ttu-id="531bf-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="531bf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="531bf-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="531bf-128">-WhatIf</span></span>
<span data-ttu-id="531bf-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="531bf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="531bf-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="531bf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="531bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531bf-131">CommonParameters</span></span>
<span data-ttu-id="531bf-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531bf-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="531bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531bf-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="531bf-134">INPUTS</span></span>

### <span data-ttu-id="531bf-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="531bf-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="531bf-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="531bf-136">OUTPUTS</span></span>

### <span data-ttu-id="531bf-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="531bf-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="531bf-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="531bf-138">NOTES</span></span>

## <span data-ttu-id="531bf-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="531bf-139">RELATED LINKS</span></span>
