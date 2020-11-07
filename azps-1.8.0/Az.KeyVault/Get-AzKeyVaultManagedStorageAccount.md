---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 165419eb13376becedf72b4e44ee17f0c3655ec4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819627"
---
# <span data-ttu-id="5e66d-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e66d-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="5e66d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e66d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e66d-103">Ruft wichtige Vault Managed Azure-Speicherkonten ab.</span><span class="sxs-lookup"><span data-stu-id="5e66d-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="5e66d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e66d-104">SYNTAX</span></span>

### <span data-ttu-id="5e66d-105">ByAccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e66d-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e66d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5e66d-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e66d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e66d-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e66d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e66d-108">DESCRIPTION</span></span>
<span data-ttu-id="5e66d-109">Ruft ein zentrales Vault Managed Azure-Speicherkonto ab, wenn der Name des Kontos angegeben ist und die Kontoschlüssel vom angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="5e66d-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="5e66d-110">Wenn der Kontoname nicht angegeben ist, werden alle Konten aufgelistet, deren Schlüssel durch den angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="5e66d-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="5e66d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e66d-111">EXAMPLES</span></span>

### <span data-ttu-id="5e66d-112">Beispiel 1: Auflisten aller wichtigen Vault-verwalteten Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="5e66d-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="5e66d-113">Listet alle Konten auf, deren Schlüssel durch Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="5e66d-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="5e66d-114">Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="5e66d-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="5e66d-115">Ruft die Details des verwalteten speicherkontos von Key Vault für "mystorageaccount" ab, wenn die Schlüssel von Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="5e66d-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="5e66d-116">Beispiel 3: Auflisten aller wichtigen Vault-verwalteten Speicherkonten mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="5e66d-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="5e66d-117">Listet alle Konten auf, deren Schlüssel durch Vault "myvault" verwaltet werden, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="5e66d-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="5e66d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e66d-118">PARAMETERS</span></span>

### <span data-ttu-id="5e66d-119">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5e66d-119">-AccountName</span></span>
<span data-ttu-id="5e66d-120">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="5e66d-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="5e66d-121">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="5e66d-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="5e66d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e66d-122">-DefaultProfile</span></span>
<span data-ttu-id="5e66d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5e66d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e66d-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e66d-124">-InputObject</span></span>
<span data-ttu-id="5e66d-125">Vault-Objekt</span><span class="sxs-lookup"><span data-stu-id="5e66d-125">Vault object.</span></span>

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

### <span data-ttu-id="5e66d-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5e66d-126">-InRemovedState</span></span>
<span data-ttu-id="5e66d-127">Gibt an, ob die zuvor gelöschten Speicherkonten in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e66d-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="5e66d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e66d-128">-ResourceId</span></span>
<span data-ttu-id="5e66d-129">Vault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5e66d-129">Vault resource id.</span></span>

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

### <span data-ttu-id="5e66d-130">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="5e66d-130">-VaultName</span></span>
<span data-ttu-id="5e66d-131">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="5e66d-131">Vault name.</span></span>
<span data-ttu-id="5e66d-132">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5e66d-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="5e66d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e66d-133">CommonParameters</span></span>
<span data-ttu-id="5e66d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e66d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e66d-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e66d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e66d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e66d-136">INPUTS</span></span>

### <span data-ttu-id="5e66d-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5e66d-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5e66d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5e66d-138">System.String</span></span>

## <span data-ttu-id="5e66d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e66d-139">OUTPUTS</span></span>

### <span data-ttu-id="5e66d-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5e66d-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="5e66d-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e66d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="5e66d-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5e66d-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="5e66d-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e66d-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="5e66d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e66d-144">NOTES</span></span>

## <span data-ttu-id="5e66d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e66d-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

