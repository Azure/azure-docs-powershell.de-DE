---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: df6f616aacb066ec17aa089b8d91226a5bd171b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658813"
---
# <span data-ttu-id="f26eb-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f26eb-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="f26eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f26eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f26eb-103">Erstellt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="f26eb-103">Creates a storage queue.</span></span>

## <span data-ttu-id="f26eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f26eb-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f26eb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f26eb-105">DESCRIPTION</span></span>
<span data-ttu-id="f26eb-106">Das Cmdlet **New-AzStorageQueue** erstellt eine Speicherwarteschlange in Azure.</span><span class="sxs-lookup"><span data-stu-id="f26eb-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="f26eb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f26eb-107">EXAMPLES</span></span>

### <span data-ttu-id="f26eb-108">Beispiel 1: Erstellen einer Azure Storage-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="f26eb-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="f26eb-109">In diesem Beispiel wird eine Speicherwarteschlange mit dem Namen "queueabc" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f26eb-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="f26eb-110">Beispiel 2: Erstellen mehrerer Azure Storage-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="f26eb-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="f26eb-111">In diesem Beispiel werden mehrere Speicher Warteschlangen erstellt.</span><span class="sxs-lookup"><span data-stu-id="f26eb-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="f26eb-112">Sie verwendet die Split-Methode der .net-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f26eb-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="f26eb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f26eb-113">PARAMETERS</span></span>

### <span data-ttu-id="f26eb-114">-Context</span><span class="sxs-lookup"><span data-stu-id="f26eb-114">-Context</span></span>
<span data-ttu-id="f26eb-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f26eb-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f26eb-116">Sie können es mithilfe des New-AzStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="f26eb-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f26eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26eb-117">-DefaultProfile</span></span>
<span data-ttu-id="f26eb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f26eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f26eb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f26eb-119">-Name</span></span>
<span data-ttu-id="f26eb-120">Gibt einen Namen für die Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="f26eb-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="f26eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26eb-121">CommonParameters</span></span>
<span data-ttu-id="f26eb-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f26eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26eb-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f26eb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26eb-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f26eb-124">INPUTS</span></span>

### <span data-ttu-id="f26eb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f26eb-125">System.String</span></span>

### <span data-ttu-id="f26eb-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f26eb-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f26eb-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f26eb-127">OUTPUTS</span></span>

### <span data-ttu-id="f26eb-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f26eb-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="f26eb-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f26eb-129">NOTES</span></span>

## <span data-ttu-id="f26eb-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f26eb-130">RELATED LINKS</span></span>

[<span data-ttu-id="f26eb-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f26eb-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="f26eb-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f26eb-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


