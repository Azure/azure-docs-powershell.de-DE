---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849819"
---
# <span data-ttu-id="31f69-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="31f69-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="31f69-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31f69-102">SYNOPSIS</span></span>
<span data-ttu-id="31f69-103">Erstellt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="31f69-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f69-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31f69-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31f69-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31f69-105">DESCRIPTION</span></span>
<span data-ttu-id="31f69-106">Das Cmdlet **New-AzureStorageQueue** erstellt eine Speicherwarteschlange in Azure.</span><span class="sxs-lookup"><span data-stu-id="31f69-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="31f69-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31f69-107">EXAMPLES</span></span>

### <span data-ttu-id="31f69-108">Beispiel 1: Erstellen einer Azure Storage-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="31f69-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="31f69-109">In diesem Beispiel wird eine Speicherwarteschlange mit dem Namen "queueabc" erstellt.</span><span class="sxs-lookup"><span data-stu-id="31f69-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="31f69-110">Beispiel 2: Erstellen mehrerer Azure Storage-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="31f69-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="31f69-111">In diesem Beispiel werden mehrere Speicher Warteschlangen erstellt.</span><span class="sxs-lookup"><span data-stu-id="31f69-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="31f69-112">Sie verwendet die Split-Methode der .net-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="31f69-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="31f69-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="31f69-113">PARAMETERS</span></span>

### <span data-ttu-id="31f69-114">-Context</span><span class="sxs-lookup"><span data-stu-id="31f69-114">-Context</span></span>
<span data-ttu-id="31f69-115">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="31f69-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="31f69-116">Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="31f69-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="31f69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f69-117">-DefaultProfile</span></span>
<span data-ttu-id="31f69-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31f69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f69-119">-Name</span><span class="sxs-lookup"><span data-stu-id="31f69-119">-Name</span></span>
<span data-ttu-id="31f69-120">Gibt einen Namen für die Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="31f69-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="31f69-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f69-121">CommonParameters</span></span>
<span data-ttu-id="31f69-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f69-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f69-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f69-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f69-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31f69-124">INPUTS</span></span>

### <span data-ttu-id="31f69-125">System. String</span><span class="sxs-lookup"><span data-stu-id="31f69-125">System.String</span></span>

### <span data-ttu-id="31f69-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="31f69-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="31f69-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31f69-127">OUTPUTS</span></span>

### <span data-ttu-id="31f69-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="31f69-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="31f69-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="31f69-129">NOTES</span></span>

## <span data-ttu-id="31f69-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31f69-130">RELATED LINKS</span></span>

[<span data-ttu-id="31f69-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="31f69-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="31f69-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="31f69-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


