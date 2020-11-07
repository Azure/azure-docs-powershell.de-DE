---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 642c5ff36fb0647907cf72218bd626bcdafe19ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819508"
---
# <span data-ttu-id="90b91-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="90b91-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="90b91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90b91-102">SYNOPSIS</span></span>
<span data-ttu-id="90b91-103">Stellt ein zuvor gelöschtes, von keyvault verwaltetes Speicherkonto ein.</span><span class="sxs-lookup"><span data-stu-id="90b91-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="90b91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90b91-104">SYNTAX</span></span>

### <span data-ttu-id="90b91-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="90b91-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90b91-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="90b91-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b91-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90b91-107">DESCRIPTION</span></span>
<span data-ttu-id="90b91-108">Mit dem Befehl **"Undo-AzKeyVaultManagedStorageAccountRemoval** " wird ein zuvor gelöschtes verwaltetes Speicherkonto wiederhergestellt, vorausgesetzt, dass Soft Delete für diesen Tresor aktiviert ist und der Wiederherstellungsversuch während des Wiederherstellungsintervalls erfolgt.</span><span class="sxs-lookup"><span data-stu-id="90b91-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="90b91-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90b91-109">EXAMPLES</span></span>

### <span data-ttu-id="90b91-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90b91-110">Example 1</span></span>
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

<span data-ttu-id="90b91-111">Diese Abfolge von Befehlen bestimmt, ob das angegebene Speicherkonto im Tresor in einem gelöschten Zustand vorhanden ist. mit dem nachfolgenden Befehl wird das gelöschte Speicherkonto wiederhergestellt, wodurch es wieder in einen aktiven Zustand versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="90b91-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="90b91-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="90b91-112">PARAMETERS</span></span>

### <span data-ttu-id="90b91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b91-113">-DefaultProfile</span></span>
<span data-ttu-id="90b91-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90b91-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90b91-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90b91-115">-InputObject</span></span>
<span data-ttu-id="90b91-116">Kontoobjekt für verwalteten Speicher gelöscht</span><span class="sxs-lookup"><span data-stu-id="90b91-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="90b91-117">-Name</span><span class="sxs-lookup"><span data-stu-id="90b91-117">-Name</span></span>
<span data-ttu-id="90b91-118">Name des verwalteten speicherkontos für keyvault</span><span class="sxs-lookup"><span data-stu-id="90b91-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="90b91-119">Cmdlet erstellt den FQDN des Ziels aus Vault-Name, aktuell ausgewählter Umgebung und dem Namen des verwalteten speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="90b91-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="90b91-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="90b91-120">-VaultName</span></span>
<span data-ttu-id="90b91-121">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="90b91-121">Vault name.</span></span>
<span data-ttu-id="90b91-122">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="90b91-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="90b91-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90b91-123">-Confirm</span></span>
<span data-ttu-id="90b91-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90b91-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b91-125">-WhatIf</span></span>
<span data-ttu-id="90b91-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90b91-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b91-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90b91-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b91-128">CommonParameters</span></span>
<span data-ttu-id="90b91-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b91-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b91-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b91-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90b91-131">INPUTS</span></span>

### <span data-ttu-id="90b91-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="90b91-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="90b91-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90b91-133">OUTPUTS</span></span>

### <span data-ttu-id="90b91-134">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90b91-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="90b91-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="90b91-135">NOTES</span></span>

## <span data-ttu-id="90b91-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90b91-136">RELATED LINKS</span></span>
