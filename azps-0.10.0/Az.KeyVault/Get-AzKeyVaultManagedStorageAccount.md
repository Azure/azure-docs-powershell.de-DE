---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843891"
---
# <span data-ttu-id="a6f4c-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6f4c-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a6f4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f4c-103">Ruft wichtige Vault Managed Azure-Speicherkonten ab.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="a6f4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6f4c-104">SYNTAX</span></span>

### <span data-ttu-id="a6f4c-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6f4c-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6f4c-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="a6f4c-106">ByAccountName</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6f4c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="a6f4c-108">Ruft ein zentrales Vault Managed Azure-Speicherkonto ab, wenn der Name des Kontos angegeben ist und die Kontoschlüssel vom angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="a6f4c-109">Wenn der Kontoname nicht angegeben ist, werden alle Konten aufgelistet, deren Schlüssel durch den angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="a6f4c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6f4c-110">EXAMPLES</span></span>

### <span data-ttu-id="a6f4c-111">Beispiel 1: Auflisten aller wichtigen Vault-verwalteten Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="a6f4c-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="a6f4c-112">Listet alle Konten auf, deren Schlüssel durch Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="a6f4c-113">Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="a6f4c-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="a6f4c-114">Ruft die Details des verwalteten speicherkontos von Key Vault für "mystorageaccount" ab, wenn die Schlüssel von Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="a6f4c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6f4c-115">PARAMETERS</span></span>

### <span data-ttu-id="a6f4c-116">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a6f4c-116">-AccountName</span></span>
<span data-ttu-id="a6f4c-117">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="a6f4c-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="a6f4c-118">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f4c-119">-DefaultProfile</span></span>
<span data-ttu-id="a6f4c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a6f4c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f4c-121">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="a6f4c-121">-VaultName</span></span>
<span data-ttu-id="a6f4c-122">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-122">Vault name.</span></span>
<span data-ttu-id="a6f4c-123">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f4c-124">CommonParameters</span></span>
<span data-ttu-id="a6f4c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f4c-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f4c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f4c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6f4c-127">INPUTS</span></span>

### <span data-ttu-id="a6f4c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a6f4c-128">System.String</span></span>

## <span data-ttu-id="a6f4c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6f4c-129">OUTPUTS</span></span>

### <span data-ttu-id="a6f4c-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a6f4c-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a6f4c-131">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6f4c-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="a6f4c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6f4c-132">NOTES</span></span>

## <span data-ttu-id="a6f4c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6f4c-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

