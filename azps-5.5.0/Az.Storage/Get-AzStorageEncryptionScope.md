---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145433"
---
# <span data-ttu-id="bcde3-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="bcde3-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="bcde3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcde3-102">SYNOPSIS</span></span>
<span data-ttu-id="bcde3-103">Sie können Verschlüsselungsbereiche aus einem Speicherkonto abspeichern oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="bcde3-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="bcde3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcde3-104">SYNTAX</span></span>

### <span data-ttu-id="bcde3-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcde3-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcde3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bcde3-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcde3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcde3-107">DESCRIPTION</span></span>
<span data-ttu-id="bcde3-108">Das **Cmdlet "Get-AzStorageEncryptionScope"** ruft Verschlüsselungsbereiche aus einem Speicherkonto ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="bcde3-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="bcde3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bcde3-109">EXAMPLES</span></span>

### <span data-ttu-id="bcde3-110">Beispiel 1: Einen einzelnen Verschlüsselungsbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="bcde3-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="bcde3-111">Dieser Befehl ruft einen einzelnen Verschlüsselungsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="bcde3-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="bcde3-112">Beispiel 2: Auflisten aller Verschlüsselungsbereich eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bcde3-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="bcde3-113">Dieser Befehl listet alle Verschlüsselungsbereich eines Speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="bcde3-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="bcde3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcde3-114">PARAMETERS</span></span>

### <span data-ttu-id="bcde3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcde3-115">-DefaultProfile</span></span>
<span data-ttu-id="bcde3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcde3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcde3-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="bcde3-117">-EncryptionScopeName</span></span>
<span data-ttu-id="bcde3-118">Azure Storage EncryptionScope-Name</span><span class="sxs-lookup"><span data-stu-id="bcde3-118">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="bcde3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcde3-119">-ResourceGroupName</span></span>
<span data-ttu-id="bcde3-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="bcde3-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="bcde3-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcde3-121">-StorageAccount</span></span>
<span data-ttu-id="bcde3-122">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="bcde3-122">Storage account object</span></span>

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

### <span data-ttu-id="bcde3-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bcde3-123">-StorageAccountName</span></span>
<span data-ttu-id="bcde3-124">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="bcde3-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="bcde3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcde3-125">CommonParameters</span></span>
<span data-ttu-id="bcde3-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcde3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcde3-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcde3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcde3-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bcde3-128">INPUTS</span></span>

### <span data-ttu-id="bcde3-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcde3-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bcde3-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bcde3-130">OUTPUTS</span></span>

### <span data-ttu-id="bcde3-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="bcde3-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="bcde3-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bcde3-132">NOTES</span></span>

## <span data-ttu-id="bcde3-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bcde3-133">RELATED LINKS</span></span>
