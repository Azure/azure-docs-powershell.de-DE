---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 55cee15e3b5327fa0a10def6e2090a77b68b207e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944494"
---
# <span data-ttu-id="0ed18-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="0ed18-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="0ed18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed18-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed18-103">Erstellt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="0ed18-103">Creates a storage queue.</span></span>

## <span data-ttu-id="0ed18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ed18-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ed18-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ed18-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed18-106">Das **New-AzStorageQueue-Cmdlet** erstellt eine Speicherwarteschlange in Azure.</span><span class="sxs-lookup"><span data-stu-id="0ed18-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="0ed18-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ed18-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed18-108">Beispiel 1: Erstellen einer Azure-Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="0ed18-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="0ed18-109">In diesem Beispiel wird eine Speicherwarteschlange namens queueabc erstellt.</span><span class="sxs-lookup"><span data-stu-id="0ed18-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="0ed18-110">Beispiel 2: Erstellen mehrerer Azure-Speicherwarteschlangen</span><span class="sxs-lookup"><span data-stu-id="0ed18-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="0ed18-111">In diesem Beispiel werden mehrere Speicherwarteschlangen erstellt.</span><span class="sxs-lookup"><span data-stu-id="0ed18-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="0ed18-112">Sie verwendet die Split-Methode der .NET String-Klasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0ed18-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="0ed18-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0ed18-113">PARAMETERS</span></span>

### <span data-ttu-id="0ed18-114">-Context</span><span class="sxs-lookup"><span data-stu-id="0ed18-114">-Context</span></span>
<span data-ttu-id="0ed18-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="0ed18-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0ed18-116">Sie können sie mithilfe des cmdlets New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ed18-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0ed18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed18-117">-DefaultProfile</span></span>
<span data-ttu-id="0ed18-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ed18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed18-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0ed18-119">-Name</span></span>
<span data-ttu-id="0ed18-120">Gibt einen Namen für die Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="0ed18-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="0ed18-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed18-121">CommonParameters</span></span>
<span data-ttu-id="0ed18-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed18-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed18-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed18-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed18-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ed18-124">INPUTS</span></span>

### <span data-ttu-id="0ed18-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0ed18-125">System.String</span></span>

### <span data-ttu-id="0ed18-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0ed18-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0ed18-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ed18-127">OUTPUTS</span></span>

### <span data-ttu-id="0ed18-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="0ed18-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="0ed18-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0ed18-129">NOTES</span></span>

## <span data-ttu-id="0ed18-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0ed18-130">RELATED LINKS</span></span>

[<span data-ttu-id="0ed18-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="0ed18-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="0ed18-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="0ed18-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


