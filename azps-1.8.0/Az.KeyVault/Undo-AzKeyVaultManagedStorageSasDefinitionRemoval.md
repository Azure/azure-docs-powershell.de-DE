---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: 7b56e7d251aee8887fe408237d17d275cb87034e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819504"
---
# <span data-ttu-id="1bc09-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="1bc09-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="1bc09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bc09-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc09-103">Stellt eine zuvor gelöschte keyvault-verwaltete Speicher-SAS-Definition fest.</span><span class="sxs-lookup"><span data-stu-id="1bc09-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="1bc09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bc09-104">SYNTAX</span></span>

### <span data-ttu-id="1bc09-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="1bc09-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bc09-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1bc09-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bc09-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bc09-107">DESCRIPTION</span></span>
<span data-ttu-id="1bc09-108">Mit dem Befehl **"Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** " wird eine zuvor gelöschte verwaltete Speicher-SAS-Definition wiederhergestellt, vorausgesetzt, dass Soft Delete für diesen Tresor aktiviert ist und der Wiederherstellungsversuch während des Wiederherstellungsintervalls erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1bc09-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="1bc09-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bc09-109">EXAMPLES</span></span>

### <span data-ttu-id="1bc09-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1bc09-110">Example 1</span></span>
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

<span data-ttu-id="1bc09-111">Diese Abfolge von Befehlen bestimmt, ob die angegebene Speicher SAS-Definition im Tresor in einem gelöschten Zustand vorhanden ist. mit dem folgenden Befehl wird die gelöschte SAS-Definition wiederhergestellt, sodass Sie wieder in einen aktiven Zustand versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1bc09-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="1bc09-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bc09-112">PARAMETERS</span></span>

### <span data-ttu-id="1bc09-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="1bc09-113">-AccountName</span></span>
<span data-ttu-id="1bc09-114">Keyvault – Name des verwalteten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1bc09-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="1bc09-115">Cmdlet erstellt den FQDN einer Definition des verwalteten Speichers SAS aus Vault Name, aktuell ausgewählter Umgebung und Name des verwalteten speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="1bc09-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="1bc09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc09-116">-DefaultProfile</span></span>
<span data-ttu-id="1bc09-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bc09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bc09-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1bc09-118">-InputObject</span></span>
<span data-ttu-id="1bc09-119">SAS-Definitionsobjekt für verwalteten Speicher gelöscht</span><span class="sxs-lookup"><span data-stu-id="1bc09-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="1bc09-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1bc09-120">-Name</span></span>
<span data-ttu-id="1bc09-121">Der Name der von keyvault verwalteten Speicher-SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="1bc09-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="1bc09-122">Cmdlet erstellt den FQDN des Ziels aus Vault-Name, aktuell ausgewählter Umgebung, dem Namen des verwalteten speicherkontos und dem Namen der SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="1bc09-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="1bc09-123">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="1bc09-123">-VaultName</span></span>
<span data-ttu-id="1bc09-124">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="1bc09-124">Vault name.</span></span>
<span data-ttu-id="1bc09-125">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="1bc09-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1bc09-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bc09-126">-Confirm</span></span>
<span data-ttu-id="1bc09-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bc09-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bc09-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bc09-128">-WhatIf</span></span>
<span data-ttu-id="1bc09-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bc09-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bc09-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bc09-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bc09-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc09-131">CommonParameters</span></span>
<span data-ttu-id="1bc09-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bc09-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc09-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc09-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc09-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bc09-134">INPUTS</span></span>

### <span data-ttu-id="1bc09-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1bc09-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="1bc09-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bc09-136">OUTPUTS</span></span>

### <span data-ttu-id="1bc09-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="1bc09-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="1bc09-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bc09-138">NOTES</span></span>

## <span data-ttu-id="1bc09-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bc09-139">RELATED LINKS</span></span>
