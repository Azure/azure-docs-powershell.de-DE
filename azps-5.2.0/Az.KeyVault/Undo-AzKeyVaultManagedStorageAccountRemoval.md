---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 3d854d6b820f6c2e23d99e3397173ec45d5b7697
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295271"
---
# <span data-ttu-id="afaf5-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="afaf5-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="afaf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="afaf5-103">Stellt ein zuvor gelöschtes, von KeyVault verwaltetes Speicherkonto wiederher.</span><span class="sxs-lookup"><span data-stu-id="afaf5-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="afaf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afaf5-104">SYNTAX</span></span>

### <span data-ttu-id="afaf5-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="afaf5-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afaf5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="afaf5-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afaf5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afaf5-107">DESCRIPTION</span></span>
<span data-ttu-id="afaf5-108">Mit dem Befehl **"Undo-AzKeyVaultManagedStorageAccountRemoval"** wird ein zuvor gelöschtes verwaltetes Speicherkonto wiederhergestellt, sofern für diesen Tresor das weiche Löschen aktiviert ist und der Wiederherstellungsversuch während des Wiederherstellungsintervalls erfolgt.</span><span class="sxs-lookup"><span data-stu-id="afaf5-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="afaf5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afaf5-109">EXAMPLES</span></span>

### <span data-ttu-id="afaf5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afaf5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="afaf5-111">Diese Befehlssequenz bestimmt, ob das angegebene Speicherkonto im Tresor in einem gelöschten Zustand vorhanden ist. Mit dem nachfolgenden Befehl wird das gelöschte Speicherkonto wiederhergestellt und wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="afaf5-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="afaf5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afaf5-112">PARAMETERS</span></span>

### <span data-ttu-id="afaf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afaf5-113">-DefaultProfile</span></span>
<span data-ttu-id="afaf5-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afaf5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afaf5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afaf5-115">-InputObject</span></span>
<span data-ttu-id="afaf5-116">Objekt "Gelöschter verwalteter Speicherkonto"</span><span class="sxs-lookup"><span data-stu-id="afaf5-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afaf5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="afaf5-117">-Name</span></span>
<span data-ttu-id="afaf5-118">Name des verwalteten Speicherkontos von KeyVault.</span><span class="sxs-lookup"><span data-stu-id="afaf5-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="afaf5-119">Das Cmdlet erstellt den FQDN des Ziels aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem Namen des verwalteten Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="afaf5-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaf5-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="afaf5-120">-VaultName</span></span>
<span data-ttu-id="afaf5-121">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="afaf5-121">Vault name.</span></span>
<span data-ttu-id="afaf5-122">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="afaf5-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="afaf5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afaf5-123">-Confirm</span></span>
<span data-ttu-id="afaf5-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afaf5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afaf5-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="afaf5-125">-WhatIf</span></span>
<span data-ttu-id="afaf5-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afaf5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afaf5-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afaf5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afaf5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afaf5-128">CommonParameters</span></span>
<span data-ttu-id="afaf5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afaf5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afaf5-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afaf5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afaf5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afaf5-131">INPUTS</span></span>

### <span data-ttu-id="afaf5-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="afaf5-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="afaf5-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afaf5-133">OUTPUTS</span></span>

### <span data-ttu-id="afaf5-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="afaf5-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="afaf5-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="afaf5-135">NOTES</span></span>

## <span data-ttu-id="afaf5-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="afaf5-136">RELATED LINKS</span></span>
