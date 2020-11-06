---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: f3a1e4d1e938b84a434c07451f3d2294e203f440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502097"
---
# <span data-ttu-id="622d1-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="622d1-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="622d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="622d1-102">SYNOPSIS</span></span>
<span data-ttu-id="622d1-103">Ruft wichtige Vault Managed Azure-Speicherkonten ab.</span><span class="sxs-lookup"><span data-stu-id="622d1-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="622d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="622d1-104">SYNTAX</span></span>

### <span data-ttu-id="622d1-105">ByAccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="622d1-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="622d1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="622d1-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="622d1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="622d1-107">ByResourceId</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622d1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="622d1-108">DESCRIPTION</span></span>
<span data-ttu-id="622d1-109">Ruft ein zentrales Vault Managed Azure-Speicherkonto ab, wenn der Name des Kontos angegeben ist und die Kontoschlüssel vom angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="622d1-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="622d1-110">Wenn der Kontoname nicht angegeben ist, werden alle Konten aufgelistet, deren Schlüssel durch den angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="622d1-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="622d1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="622d1-111">EXAMPLES</span></span>

### <span data-ttu-id="622d1-112">Beispiel 1: Auflisten aller wichtigen Vault-verwalteten Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="622d1-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="622d1-113">Listet alle Konten auf, deren Schlüssel durch Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="622d1-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="622d1-114">Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="622d1-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

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

<span data-ttu-id="622d1-115">Ruft die Details des verwalteten speicherkontos von Key Vault für "mystorageaccount" ab, wenn die Schlüssel von Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="622d1-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="622d1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="622d1-116">PARAMETERS</span></span>

### <span data-ttu-id="622d1-117">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="622d1-117">-AccountName</span></span>
<span data-ttu-id="622d1-118">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="622d1-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="622d1-119">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="622d1-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622d1-120">-DefaultProfile</span></span>
<span data-ttu-id="622d1-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="622d1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="622d1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="622d1-122">-InputObject</span></span>
<span data-ttu-id="622d1-123">Vault-Objekt</span><span class="sxs-lookup"><span data-stu-id="622d1-123">Vault object.</span></span>

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

### <span data-ttu-id="622d1-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="622d1-124">-InRemovedState</span></span>
<span data-ttu-id="622d1-125">Gibt an, ob die zuvor gelöschten Speicherkonten in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="622d1-125">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="622d1-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="622d1-126">-ResourceId</span></span>
<span data-ttu-id="622d1-127">Vault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="622d1-127">Vault resource id.</span></span>

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

### <span data-ttu-id="622d1-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="622d1-128">-VaultName</span></span>
<span data-ttu-id="622d1-129">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="622d1-129">Vault name.</span></span>
<span data-ttu-id="622d1-130">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="622d1-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="622d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622d1-131">CommonParameters</span></span>
<span data-ttu-id="622d1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622d1-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622d1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622d1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="622d1-134">INPUTS</span></span>

### <span data-ttu-id="622d1-135">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="622d1-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="622d1-136">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="622d1-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="622d1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="622d1-137">System.String</span></span>

## <span data-ttu-id="622d1-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="622d1-138">OUTPUTS</span></span>

### <span data-ttu-id="622d1-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="622d1-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="622d1-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="622d1-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="622d1-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="622d1-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="622d1-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="622d1-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="622d1-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="622d1-143">NOTES</span></span>

## <span data-ttu-id="622d1-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="622d1-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

