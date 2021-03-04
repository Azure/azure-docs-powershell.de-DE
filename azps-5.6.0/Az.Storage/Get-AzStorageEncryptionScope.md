---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: 02d91338063a1c06654fa30cbbf584a6f62ea34a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933376"
---
# <span data-ttu-id="6d8f5-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6d8f5-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="6d8f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8f5-103">Sie können Verschlüsselungsbereiche aus einem Speicherkonto erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="6d8f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d8f5-104">SYNTAX</span></span>

### <span data-ttu-id="6d8f5-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d8f5-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d8f5-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6d8f5-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d8f5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d8f5-107">DESCRIPTION</span></span>
<span data-ttu-id="6d8f5-108">Das **Get-AzStorageEncryptionScope-Cmdlet** ruft Verschlüsselungsbereiche aus einem Speicherkonto ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="6d8f5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d8f5-109">EXAMPLES</span></span>

### <span data-ttu-id="6d8f5-110">Beispiel 1: Einen einzelnen Verschlüsselungsbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="6d8f5-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="6d8f5-111">Dieser Befehl ruft einen einzelnen Verschlüsselungsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="6d8f5-112">Beispiel 2: Auflisten aller Verschlüsselungsbereiche eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="6d8f5-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="6d8f5-113">Mit diesem Befehl werden alle Verschlüsselungsbereiche eines Speicherkontos aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="6d8f5-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6d8f5-114">PARAMETERS</span></span>

### <span data-ttu-id="6d8f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8f5-115">-DefaultProfile</span></span>
<span data-ttu-id="6d8f5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d8f5-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="6d8f5-117">-EncryptionScopeName</span></span>
<span data-ttu-id="6d8f5-118">Azure Storage EncryptionScope Name</span><span class="sxs-lookup"><span data-stu-id="6d8f5-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d8f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d8f5-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d8f5-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d8f5-121">-StorageAccount</span></span>
<span data-ttu-id="6d8f5-122">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="6d8f5-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8f5-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6d8f5-123">-StorageAccountName</span></span>
<span data-ttu-id="6d8f5-124">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d8f5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8f5-125">CommonParameters</span></span>
<span data-ttu-id="6d8f5-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d8f5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8f5-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8f5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8f5-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d8f5-128">INPUTS</span></span>

### <span data-ttu-id="6d8f5-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d8f5-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6d8f5-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d8f5-130">OUTPUTS</span></span>

### <span data-ttu-id="6d8f5-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6d8f5-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="6d8f5-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6d8f5-132">NOTES</span></span>

## <span data-ttu-id="6d8f5-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6d8f5-133">RELATED LINKS</span></span>
