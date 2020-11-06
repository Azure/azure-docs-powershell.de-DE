---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 63187859a4296f37e5af28880f42a487c018288f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479210"
---
# <span data-ttu-id="6da82-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="6da82-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="6da82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6da82-102">SYNOPSIS</span></span>
<span data-ttu-id="6da82-103">Ruft Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="6da82-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6da82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6da82-104">SYNTAX</span></span>

### <span data-ttu-id="6da82-105">ByAccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6da82-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6da82-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6da82-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6da82-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6da82-107">DESCRIPTION</span></span>
<span data-ttu-id="6da82-108">Ruft eine Key Vault-Definition für verwaltete Speicher SAS ab, wenn der Name der Definition angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6da82-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="6da82-109">Wenn der Definitionsname nicht angegeben ist, werden alle SAS-Definitionen aufgelistet, die dem angegebenen Schlüsseldepot-verwalteten Speicherkonto im Tresor zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6da82-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="6da82-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6da82-110">EXAMPLES</span></span>

### <span data-ttu-id="6da82-111">Beispiel 1: Auflisten aller Key Vault-Definitionen für verwaltete Speicher-SAS</span><span class="sxs-lookup"><span data-stu-id="6da82-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="6da82-112">Listet alle SAS-Definitionen auf, die mit dem von Vault "myvault" verwalteten Speicherkonto "mystorageaccount" des Schlüsseldepots verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="6da82-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="6da82-113">Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="6da82-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="6da82-114">Ruft die Details der SAS-Definition "mysasDef" ab, die mit dem von Vault "myvault" verwalteten Schlüsseldepot-verwalteten Speicherkonto "mystorageaccount" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6da82-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="6da82-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6da82-115">PARAMETERS</span></span>

### <span data-ttu-id="6da82-116">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6da82-116">-AccountName</span></span>
<span data-ttu-id="6da82-117">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="6da82-117">Vault name.</span></span>
<span data-ttu-id="6da82-118">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6da82-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da82-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6da82-119">-Name</span></span>
<span data-ttu-id="6da82-120">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="6da82-120">Storage sas definition name.</span></span>
<span data-ttu-id="6da82-121">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="6da82-121">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da82-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="6da82-122">-VaultName</span></span>
<span data-ttu-id="6da82-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="6da82-123">Vault name.</span></span>
<span data-ttu-id="6da82-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6da82-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6da82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da82-125">-DefaultProfile</span></span>
<span data-ttu-id="6da82-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6da82-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da82-127">CommonParameters</span></span>
<span data-ttu-id="6da82-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da82-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da82-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da82-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6da82-130">INPUTS</span></span>

### <span data-ttu-id="6da82-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6da82-131">System.String</span></span>

## <span data-ttu-id="6da82-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6da82-132">OUTPUTS</span></span>

### <span data-ttu-id="6da82-133">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6da82-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="6da82-134">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="6da82-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="6da82-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6da82-135">NOTES</span></span>

## <span data-ttu-id="6da82-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6da82-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

