---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 7bf6539aaf849177d6e9da1fd74bcbedc28c8763
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501817"
---
# <span data-ttu-id="fa013-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa013-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fa013-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa013-102">SYNOPSIS</span></span>
<span data-ttu-id="fa013-103">Ruft wichtige Vault Managed Azure-Speicherkonten ab.</span><span class="sxs-lookup"><span data-stu-id="fa013-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa013-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa013-104">SYNTAX</span></span>

### <span data-ttu-id="fa013-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa013-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa013-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="fa013-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa013-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa013-107">DESCRIPTION</span></span>
<span data-ttu-id="fa013-108">Ruft ein zentrales Vault Managed Azure-Speicherkonto ab, wenn der Name des Kontos angegeben ist und die Kontoschlüssel vom angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fa013-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="fa013-109">Wenn der Kontoname nicht angegeben ist, werden alle Konten aufgelistet, deren Schlüssel durch den angegebenen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fa013-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="fa013-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa013-110">EXAMPLES</span></span>

### <span data-ttu-id="fa013-111">Beispiel 1: Auflisten aller wichtigen Vault-verwalteten Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="fa013-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="fa013-112">Listet alle Konten auf, deren Schlüssel durch Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fa013-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="fa013-113">Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="fa013-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="fa013-114">Ruft die Details des verwalteten speicherkontos von Key Vault für "mystorageaccount" ab, wenn die Schlüssel von Vault "myvault" verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fa013-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="fa013-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa013-115">PARAMETERS</span></span>

### <span data-ttu-id="fa013-116">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="fa013-116">-AccountName</span></span>
<span data-ttu-id="fa013-117">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="fa013-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="fa013-118">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="fa013-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa013-119">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="fa013-119">-VaultName</span></span>
<span data-ttu-id="fa013-120">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="fa013-120">Vault name.</span></span>
<span data-ttu-id="fa013-121">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="fa013-121">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa013-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa013-122">-DefaultProfile</span></span>
<span data-ttu-id="fa013-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa013-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa013-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa013-124">CommonParameters</span></span>
<span data-ttu-id="fa013-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa013-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa013-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa013-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa013-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa013-127">INPUTS</span></span>

### <span data-ttu-id="fa013-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fa013-128">System.String</span></span>

## <span data-ttu-id="fa013-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa013-129">OUTPUTS</span></span>

### <span data-ttu-id="fa013-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fa013-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fa013-131">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa013-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="fa013-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa013-132">NOTES</span></span>

## <span data-ttu-id="fa013-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa013-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

