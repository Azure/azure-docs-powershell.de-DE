---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 552a696a31b8c5fb26a1c6a17434ef53380d0491
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944141"
---
# <span data-ttu-id="7a8de-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7a8de-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7a8de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8de-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8de-103">Ruft verwaltete Azure -Speicherkonten für den Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="7a8de-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="7a8de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a8de-104">SYNTAX</span></span>

### <span data-ttu-id="7a8de-105">ByAccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a8de-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a8de-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a8de-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a8de-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a8de-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a8de-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a8de-108">DESCRIPTION</span></span>
<span data-ttu-id="7a8de-109">Ruft ein vom Schlüsseltresor verwaltetes Azure Storage-Konto ab, wenn der Name des Kontos angegeben ist und die Kontoschlüssel vom angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7a8de-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="7a8de-110">Wenn der Kontoname nicht angegeben ist, werden alle Konten aufgelistet, deren Schlüssel von einem angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7a8de-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="7a8de-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a8de-111">EXAMPLES</span></span>

### <span data-ttu-id="7a8de-112">Beispiel 1: Auflisten aller verwalteten Speicherkonten im Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="7a8de-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="7a8de-113">Listet alle Konten auf, deren Schlüssel vom Tresor "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7a8de-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="7a8de-114">Beispiel 2: Erhalten eines verwalteten Speicherkontos für den Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="7a8de-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="7a8de-115">Ruft die Details des verwalteten Speicherkontos für den Schlüsseltresor von "mystorageaccount" ab, wenn die Schlüssel vom Tresor "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7a8de-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="7a8de-116">Beispiel 3: Auflisten aller verwalteten Speicherkonten im Schlüsseltresor mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="7a8de-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="7a8de-117">Listet alle Konten auf, deren Schlüssel vom Tresor "myvault" verwaltet werden, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="7a8de-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="7a8de-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7a8de-118">PARAMETERS</span></span>

### <span data-ttu-id="7a8de-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a8de-119">-AccountName</span></span>
<span data-ttu-id="7a8de-120">Name des verwalteten Speicherkontos für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7a8de-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="7a8de-121">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="7a8de-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7a8de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8de-122">-DefaultProfile</span></span>
<span data-ttu-id="7a8de-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7a8de-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a8de-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a8de-124">-InputObject</span></span>
<span data-ttu-id="7a8de-125">Vault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7a8de-125">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8de-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7a8de-126">-InRemovedState</span></span>
<span data-ttu-id="7a8de-127">Gibt an, ob die zuvor gelöschten Speicherkonten in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a8de-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="7a8de-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a8de-128">-ResourceId</span></span>
<span data-ttu-id="7a8de-129">Tresorressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7a8de-129">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8de-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7a8de-130">-VaultName</span></span>
<span data-ttu-id="7a8de-131">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="7a8de-131">Vault name.</span></span>
<span data-ttu-id="7a8de-132">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="7a8de-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8de-133">CommonParameters</span></span>
<span data-ttu-id="7a8de-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8de-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a8de-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8de-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a8de-136">INPUTS</span></span>

### <span data-ttu-id="7a8de-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a8de-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="7a8de-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7a8de-138">System.String</span></span>

## <span data-ttu-id="7a8de-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a8de-139">OUTPUTS</span></span>

### <span data-ttu-id="7a8de-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7a8de-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="7a8de-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7a8de-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="7a8de-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7a8de-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="7a8de-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7a8de-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7a8de-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7a8de-144">NOTES</span></span>

## <span data-ttu-id="7a8de-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7a8de-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

