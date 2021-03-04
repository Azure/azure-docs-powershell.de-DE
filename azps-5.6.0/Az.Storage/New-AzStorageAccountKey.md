---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 254d9a012bd3539242e560511e23975acb68b4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944584"
---
# <span data-ttu-id="87c1b-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="87c1b-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="87c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="87c1b-103">Regeneriert einen Speicherschlüssel für ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="87c1b-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="87c1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87c1b-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87c1b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="87c1b-106">Das **Cmdlet New-AzStorageAccountKey** generiert einen Speicherschlüssel für ein Azure Storage-Konto neu.</span><span class="sxs-lookup"><span data-stu-id="87c1b-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="87c1b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="87c1b-108">Beispiel 1: Regenerieren eines Speicherschlüssels</span><span class="sxs-lookup"><span data-stu-id="87c1b-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="87c1b-109">Mit diesem Befehl wird ein Speicherschlüssel für das angegebene Speicherkonto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="87c1b-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="87c1b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="87c1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c1b-111">-DefaultProfile</span></span>
<span data-ttu-id="87c1b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87c1b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87c1b-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="87c1b-113">-KeyName</span></span>
<span data-ttu-id="87c1b-114">Gibt an, welcher Schlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="87c1b-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="87c1b-115">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="87c1b-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87c1b-116">Taste1</span><span class="sxs-lookup"><span data-stu-id="87c1b-116">key1</span></span>
- <span data-ttu-id="87c1b-117">Taste2</span><span class="sxs-lookup"><span data-stu-id="87c1b-117">key2</span></span>
- <span data-ttu-id="87c1b-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="87c1b-118">kerb1</span></span>
- <span data-ttu-id="87c1b-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="87c1b-119">kerb2</span></span>

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

### <span data-ttu-id="87c1b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="87c1b-120">-Name</span></span>
<span data-ttu-id="87c1b-121">Gibt den Namen des Speicherkontos an, für das ein Speicherschlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="87c1b-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="87c1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="87c1b-123">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="87c1b-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="87c1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c1b-124">CommonParameters</span></span>
<span data-ttu-id="87c1b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c1b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c1b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c1b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87c1b-127">INPUTS</span></span>

### <span data-ttu-id="87c1b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="87c1b-128">System.String</span></span>

## <span data-ttu-id="87c1b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87c1b-129">OUTPUTS</span></span>

### <span data-ttu-id="87c1b-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="87c1b-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="87c1b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87c1b-131">NOTES</span></span>

## <span data-ttu-id="87c1b-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87c1b-132">RELATED LINKS</span></span>

[<span data-ttu-id="87c1b-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="87c1b-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
