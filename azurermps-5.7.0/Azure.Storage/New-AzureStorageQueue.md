---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496733"
---
# <span data-ttu-id="9e658-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e658-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="9e658-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e658-102">SYNOPSIS</span></span>
<span data-ttu-id="9e658-103">Erstellt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="9e658-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e658-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e658-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="9e658-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e658-105">DESCRIPTION</span></span>
<span data-ttu-id="9e658-106">Das Cmdlet **New-AzureStorageQueue** erstellt eine Speicherwarteschlange in Azure.</span><span class="sxs-lookup"><span data-stu-id="9e658-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="9e658-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e658-107">EXAMPLES</span></span>

### <span data-ttu-id="9e658-108">Beispiel 1: Erstellen einer Azure Storage-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="9e658-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="9e658-109">In diesem Beispiel wird eine Speicherwarteschlange mit dem Namen "queueabc" erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e658-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="9e658-110">Beispiel 2: Erstellen mehrerer Azure Storage-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="9e658-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="9e658-111">In diesem Beispiel werden mehrere Speicher Warteschlangen erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e658-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="9e658-112">Sie verwendet die Split-Methode der .net-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e658-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="9e658-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e658-113">PARAMETERS</span></span>

### <span data-ttu-id="9e658-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9e658-114">-Context</span></span>
<span data-ttu-id="9e658-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9e658-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9e658-116">Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e658-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e658-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9e658-117">-Name</span></span>
<span data-ttu-id="9e658-118">Gibt einen Namen für die Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="9e658-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e658-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e658-119">CommonParameters</span></span>
<span data-ttu-id="9e658-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e658-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e658-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e658-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e658-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e658-122">INPUTS</span></span>

### <span data-ttu-id="9e658-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e658-123">IStorageContext</span></span>

<span data-ttu-id="9e658-124">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e658-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="9e658-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9e658-125">String</span></span>

<span data-ttu-id="9e658-126">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e658-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9e658-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e658-127">OUTPUTS</span></span>

### <span data-ttu-id="9e658-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e658-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="9e658-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e658-129">NOTES</span></span>

## <span data-ttu-id="9e658-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e658-130">RELATED LINKS</span></span>

[<span data-ttu-id="9e658-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e658-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="9e658-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e658-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


