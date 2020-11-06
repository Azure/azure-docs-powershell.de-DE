---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475318"
---
# <span data-ttu-id="ee32f-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ee32f-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="ee32f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee32f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee32f-103">Erstellt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="ee32f-103">Creates a storage queue.</span></span>

## <span data-ttu-id="ee32f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee32f-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ee32f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee32f-105">DESCRIPTION</span></span>
<span data-ttu-id="ee32f-106">Das Cmdlet **New-AzureStorageQueue** erstellt eine Speicherwarteschlange in Azure.</span><span class="sxs-lookup"><span data-stu-id="ee32f-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="ee32f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee32f-107">EXAMPLES</span></span>

### <span data-ttu-id="ee32f-108">Beispiel 1: Erstellen einer Azure Storage-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="ee32f-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="ee32f-109">In diesem Beispiel wird eine Speicherwarteschlange mit dem Namen "queueabc" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee32f-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="ee32f-110">Beispiel 2: Erstellen mehrerer Azure Storage-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="ee32f-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="ee32f-111">In diesem Beispiel werden mehrere Speicher Warteschlangen erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee32f-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="ee32f-112">Sie verwendet die Split-Methode der .net-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ee32f-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="ee32f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee32f-113">PARAMETERS</span></span>

### <span data-ttu-id="ee32f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ee32f-114">-Context</span></span>
<span data-ttu-id="ee32f-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ee32f-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ee32f-116">Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee32f-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee32f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ee32f-117">-Name</span></span>
<span data-ttu-id="ee32f-118">Gibt einen Namen für die Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="ee32f-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="ee32f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee32f-119">CommonParameters</span></span>
<span data-ttu-id="ee32f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee32f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee32f-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee32f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee32f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee32f-122">INPUTS</span></span>

## <span data-ttu-id="ee32f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee32f-123">OUTPUTS</span></span>

## <span data-ttu-id="ee32f-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee32f-124">NOTES</span></span>

## <span data-ttu-id="ee32f-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee32f-125">RELATED LINKS</span></span>

[<span data-ttu-id="ee32f-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ee32f-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="ee32f-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ee32f-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


