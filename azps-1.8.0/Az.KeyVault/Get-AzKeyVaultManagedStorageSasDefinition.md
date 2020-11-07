---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff384b456d6cbaac3fa0c28f01038a60b211dfca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819620"
---
# <span data-ttu-id="bb045-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="bb045-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="bb045-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb045-102">SYNOPSIS</span></span>
<span data-ttu-id="bb045-103">Ruft Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="bb045-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="bb045-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb045-104">SYNTAX</span></span>

### <span data-ttu-id="bb045-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb045-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb045-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb045-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb045-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb045-107">DESCRIPTION</span></span>
<span data-ttu-id="bb045-108">Ruft eine Key Vault-Definition für verwaltete Speicher SAS ab, wenn der Name der Definition angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bb045-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="bb045-109">Wenn der Definitionsname nicht angegeben ist, werden alle SAS-Definitionen aufgelistet, die dem angegebenen Schlüsseldepot-verwalteten Speicherkonto im Tresor zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bb045-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="bb045-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb045-110">EXAMPLES</span></span>

### <span data-ttu-id="bb045-111">Beispiel 1: Auflisten aller Key Vault-Definitionen für verwaltete Speicher-SAS</span><span class="sxs-lookup"><span data-stu-id="bb045-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="bb045-112">Listet alle SAS-Definitionen auf, die mit dem von Vault "myvault" verwalteten Speicherkonto "mystorageaccount" des Schlüsseldepots verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="bb045-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="bb045-113">Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="bb045-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="bb045-114">Ruft die Details der SAS-Definition "Konten" ab, die mit dem von Vault "myvault" verwalteten Speicherkonto "mystorageaccount" des Schlüsseldepots verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="bb045-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="bb045-115">Beispiel 3: Auflisten aller Schlüsselspeicher-SAS-Definitions Definitionen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="bb045-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="bb045-116">Listet alle SAS-Definitionen auf, die mit dem verwalteten Speicherkonto "mystorageaccount" verknüpft sind, das von Vault "myvault" verwaltet wird, das mit "Konto" beginnt.</span><span class="sxs-lookup"><span data-stu-id="bb045-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="bb045-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb045-117">PARAMETERS</span></span>

### <span data-ttu-id="bb045-118">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="bb045-118">-AccountName</span></span>
<span data-ttu-id="bb045-119">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="bb045-119">Vault name.</span></span>
<span data-ttu-id="bb045-120">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bb045-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb045-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb045-121">-DefaultProfile</span></span>
<span data-ttu-id="bb045-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb045-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb045-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb045-123">-InputObject</span></span>
<span data-ttu-id="bb045-124">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb045-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="bb045-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="bb045-125">-InRemovedState</span></span>
<span data-ttu-id="bb045-126">Gibt an, ob die zuvor gelöschten Speicher-SAS-Definitionen in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bb045-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="bb045-127">-Name</span><span class="sxs-lookup"><span data-stu-id="bb045-127">-Name</span></span>
<span data-ttu-id="bb045-128">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="bb045-128">Storage sas definition name.</span></span>
<span data-ttu-id="bb045-129">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="bb045-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb045-130">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="bb045-130">-VaultName</span></span>
<span data-ttu-id="bb045-131">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="bb045-131">Vault name.</span></span>
<span data-ttu-id="bb045-132">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bb045-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="bb045-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb045-133">CommonParameters</span></span>
<span data-ttu-id="bb045-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb045-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb045-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb045-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb045-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb045-136">INPUTS</span></span>

### <span data-ttu-id="bb045-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bb045-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="bb045-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb045-138">OUTPUTS</span></span>

### <span data-ttu-id="bb045-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bb045-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="bb045-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="bb045-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="bb045-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="bb045-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="bb045-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bb045-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="bb045-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb045-143">NOTES</span></span>

## <span data-ttu-id="bb045-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb045-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

