---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1ce3615d7eeef4986f1fefd20ec5be2ea1aaac7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842991"
---
# <span data-ttu-id="06762-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="06762-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="06762-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06762-102">SYNOPSIS</span></span>
<span data-ttu-id="06762-103">Erstellt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="06762-103">Creates a storage queue.</span></span>

## <span data-ttu-id="06762-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06762-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06762-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06762-105">DESCRIPTION</span></span>
<span data-ttu-id="06762-106">Das Cmdlet **New-AzStorageQueue** erstellt eine Speicherwarteschlange in Azure.</span><span class="sxs-lookup"><span data-stu-id="06762-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="06762-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06762-107">EXAMPLES</span></span>

### <span data-ttu-id="06762-108">Beispiel 1: Erstellen einer Azure Storage-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="06762-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="06762-109">In diesem Beispiel wird eine Speicherwarteschlange mit dem Namen "queueabc" erstellt.</span><span class="sxs-lookup"><span data-stu-id="06762-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="06762-110">Beispiel 2: Erstellen mehrerer Azure Storage-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="06762-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="06762-111">In diesem Beispiel werden mehrere Speicher Warteschlangen erstellt.</span><span class="sxs-lookup"><span data-stu-id="06762-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="06762-112">Sie verwendet die Split-Methode der .net-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="06762-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="06762-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="06762-113">PARAMETERS</span></span>

### <span data-ttu-id="06762-114">-Context</span><span class="sxs-lookup"><span data-stu-id="06762-114">-Context</span></span>
<span data-ttu-id="06762-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="06762-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="06762-116">Sie können es mithilfe des New-AzStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="06762-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06762-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06762-117">-DefaultProfile</span></span>
<span data-ttu-id="06762-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06762-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06762-119">-Name</span><span class="sxs-lookup"><span data-stu-id="06762-119">-Name</span></span>
<span data-ttu-id="06762-120">Gibt einen Namen für die Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="06762-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06762-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06762-121">CommonParameters</span></span>
<span data-ttu-id="06762-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06762-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06762-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06762-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06762-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06762-124">INPUTS</span></span>

### <span data-ttu-id="06762-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06762-125">System.String</span></span>

### <span data-ttu-id="06762-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06762-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="06762-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06762-127">OUTPUTS</span></span>

### <span data-ttu-id="06762-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="06762-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="06762-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="06762-129">NOTES</span></span>

## <span data-ttu-id="06762-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06762-130">RELATED LINKS</span></span>

[<span data-ttu-id="06762-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="06762-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="06762-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="06762-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


