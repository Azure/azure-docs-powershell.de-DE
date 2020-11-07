---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: a8e8bb9a4a006c30275f1de959181ad640a04f88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664855"
---
# <span data-ttu-id="03115-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="03115-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="03115-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03115-102">SYNOPSIS</span></span>
<span data-ttu-id="03115-103">Stellt ein zuvor gelöschtes, von keyvault verwaltetes Speicherkonto ein.</span><span class="sxs-lookup"><span data-stu-id="03115-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03115-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03115-104">SYNTAX</span></span>

### <span data-ttu-id="03115-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="03115-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03115-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="03115-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval
 [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03115-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03115-107">DESCRIPTION</span></span>
<span data-ttu-id="03115-108">Mit dem Befehl **"Undo-AzureKeyVaultManagedStorageAccountRemoval** " wird ein zuvor gelöschtes verwaltetes Speicherkonto wiederhergestellt, vorausgesetzt, dass Soft Delete für diesen Tresor aktiviert ist und der Wiederherstellungsversuch während des Wiederherstellungsintervalls erfolgt.</span><span class="sxs-lookup"><span data-stu-id="03115-108">The **Undo-AzureKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="03115-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03115-109">EXAMPLES</span></span>

### <span data-ttu-id="03115-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03115-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

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

<span data-ttu-id="03115-111">Diese Abfolge von Befehlen bestimmt, ob das angegebene Speicherkonto im Tresor in einem gelöschten Zustand vorhanden ist. mit dem nachfolgenden Befehl wird das gelöschte Speicherkonto wiederhergestellt, wodurch es wieder in einen aktiven Zustand versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="03115-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="03115-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="03115-112">PARAMETERS</span></span>

### <span data-ttu-id="03115-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03115-113">-DefaultProfile</span></span>
<span data-ttu-id="03115-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03115-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03115-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03115-115">-InputObject</span></span>
<span data-ttu-id="03115-116">Kontoobjekt für verwalteten Speicher gelöscht</span><span class="sxs-lookup"><span data-stu-id="03115-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="03115-117">-Name</span><span class="sxs-lookup"><span data-stu-id="03115-117">-Name</span></span>
<span data-ttu-id="03115-118">Name des verwalteten speicherkontos für keyvault</span><span class="sxs-lookup"><span data-stu-id="03115-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="03115-119">Cmdlet erstellt den FQDN des Ziels aus Vault-Name, aktuell ausgewählter Umgebung und dem Namen des verwalteten speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="03115-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="03115-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="03115-120">-VaultName</span></span>
<span data-ttu-id="03115-121">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="03115-121">Vault name.</span></span>
<span data-ttu-id="03115-122">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="03115-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="03115-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03115-123">-Confirm</span></span>
<span data-ttu-id="03115-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03115-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03115-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03115-125">-WhatIf</span></span>
<span data-ttu-id="03115-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03115-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03115-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03115-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03115-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03115-128">CommonParameters</span></span>
<span data-ttu-id="03115-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03115-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03115-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03115-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03115-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03115-131">INPUTS</span></span>

### <span data-ttu-id="03115-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="03115-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="03115-133">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03115-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="03115-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03115-134">OUTPUTS</span></span>

### <span data-ttu-id="03115-135">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03115-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="03115-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="03115-136">NOTES</span></span>

## <span data-ttu-id="03115-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03115-137">RELATED LINKS</span></span>
