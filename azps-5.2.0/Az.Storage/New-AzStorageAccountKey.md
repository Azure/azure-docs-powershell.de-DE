---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304115"
---
# <span data-ttu-id="6e171-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6e171-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="6e171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e171-102">SYNOPSIS</span></span>
<span data-ttu-id="6e171-103">Generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="6e171-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="6e171-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e171-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e171-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e171-105">DESCRIPTION</span></span>
<span data-ttu-id="6e171-106">Das **Cmdlet "New-AzStorageAccountKey"** generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="6e171-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="6e171-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e171-107">EXAMPLES</span></span>

### <span data-ttu-id="6e171-108">Beispiel 1: Erneutererieren eines Speicherschlüssels</span><span class="sxs-lookup"><span data-stu-id="6e171-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="6e171-109">Mit diesem Befehl wird ein Speicherschlüssel für das angegebene Speicherkonto erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="6e171-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="6e171-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e171-110">PARAMETERS</span></span>

### <span data-ttu-id="6e171-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e171-111">-DefaultProfile</span></span>
<span data-ttu-id="6e171-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e171-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e171-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6e171-113">-KeyName</span></span>
<span data-ttu-id="6e171-114">Gibt an, welcher Schlüssel erneut generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e171-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="6e171-115">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6e171-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e171-116">key1</span><span class="sxs-lookup"><span data-stu-id="6e171-116">key1</span></span>
- <span data-ttu-id="6e171-117">key2</span><span class="sxs-lookup"><span data-stu-id="6e171-117">key2</span></span>
- <span data-ttu-id="6e171-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="6e171-118">kerb1</span></span>
- <span data-ttu-id="6e171-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="6e171-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e171-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6e171-120">-Name</span></span>
<span data-ttu-id="6e171-121">Gibt den Namen des Speicherkontos an, für das ein Speicherschlüssel erneut generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e171-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e171-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e171-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e171-123">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="6e171-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="6e171-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e171-124">CommonParameters</span></span>
<span data-ttu-id="6e171-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e171-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e171-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e171-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e171-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e171-127">INPUTS</span></span>

### <span data-ttu-id="6e171-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6e171-128">System.String</span></span>

## <span data-ttu-id="6e171-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e171-129">OUTPUTS</span></span>

### <span data-ttu-id="6e171-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="6e171-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="6e171-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6e171-131">NOTES</span></span>

## <span data-ttu-id="6e171-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6e171-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e171-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6e171-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
