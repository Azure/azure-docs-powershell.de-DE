---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500361"
---
# <span data-ttu-id="9fca2-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9fca2-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="9fca2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fca2-102">SYNOPSIS</span></span>
<span data-ttu-id="9fca2-103">Generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="9fca2-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fca2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fca2-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="9fca2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fca2-105">DESCRIPTION</span></span>
<span data-ttu-id="9fca2-106">Das Cmdlet **New-AzureRmStorageAccountKey** generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="9fca2-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="9fca2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fca2-107">EXAMPLES</span></span>

### <span data-ttu-id="9fca2-108">Beispiel 1: Erneutes Generieren eines Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="9fca2-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="9fca2-109">Mit diesem Befehl wird ein Speicherschlüssel für das angegebene Speicherkonto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="9fca2-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="9fca2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fca2-110">PARAMETERS</span></span>

### <span data-ttu-id="9fca2-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9fca2-111">-KeyName</span></span>
<span data-ttu-id="9fca2-112">Gibt an, welche Taste neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fca2-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="9fca2-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9fca2-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9fca2-114">key1</span><span class="sxs-lookup"><span data-stu-id="9fca2-114">key1</span></span>
- <span data-ttu-id="9fca2-115">key2</span><span class="sxs-lookup"><span data-stu-id="9fca2-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fca2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9fca2-116">-Name</span></span>
<span data-ttu-id="9fca2-117">Gibt den Namen des speicherkontos an, für das ein Speicherschlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fca2-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fca2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fca2-118">-ResourceGroupName</span></span>
<span data-ttu-id="9fca2-119">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="9fca2-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="9fca2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fca2-120">CommonParameters</span></span>
<span data-ttu-id="9fca2-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fca2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fca2-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fca2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fca2-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fca2-123">INPUTS</span></span>

### <span data-ttu-id="9fca2-124">Keine</span><span class="sxs-lookup"><span data-stu-id="9fca2-124">None</span></span>
<span data-ttu-id="9fca2-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9fca2-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fca2-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fca2-126">OUTPUTS</span></span>

## <span data-ttu-id="9fca2-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fca2-127">NOTES</span></span>

## <span data-ttu-id="9fca2-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fca2-128">RELATED LINKS</span></span>

[<span data-ttu-id="9fca2-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9fca2-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
