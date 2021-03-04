---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e5d177776e288a855c35def8d45310a6f6849c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938283"
---
# <span data-ttu-id="4273c-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="4273c-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="4273c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4273c-102">SYNOPSIS</span></span>
<span data-ttu-id="4273c-103">Ruft batchgestützte Bilder für ein Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="4273c-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="4273c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4273c-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4273c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4273c-105">DESCRIPTION</span></span>
<span data-ttu-id="4273c-106">Das **Get-AzBatchSupportedImage-Cmdlet** ruft unterstützte Bilder virtueller Computer ab, die in einem Azure Batch-Konto verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4273c-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="4273c-107">Geben Sie das Konto mithilfe des *BatchContext-Parameters* an.</span><span class="sxs-lookup"><span data-stu-id="4273c-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="4273c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4273c-108">EXAMPLES</span></span>

### <span data-ttu-id="4273c-109">Beispiel 1: Alle verfügbaren unterstützten Bilder erhalten</span><span class="sxs-lookup"><span data-stu-id="4273c-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="4273c-110">Der erste Befehl ruft mithilfe von **Get-AzBatchAccountKey einen Batchkontokontext** ab, der Zugriffstasten für Ihr Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="4273c-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="4273c-111">Der Befehl speichert den Kontext in der $Context, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4273c-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="4273c-112">Der zweite Befehl ruft alle verfügbaren unterstützten Bilder für dieses Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="4273c-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="4273c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4273c-113">PARAMETERS</span></span>

### <span data-ttu-id="4273c-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4273c-114">-BatchContext</span></span>
<span data-ttu-id="4273c-115">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batchdienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4273c-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="4273c-116">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="4273c-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="4273c-117">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4273c-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="4273c-118">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="4273c-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="4273c-119">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="4273c-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4273c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4273c-120">-DefaultProfile</span></span>
<span data-ttu-id="4273c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4273c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4273c-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="4273c-122">-Filter</span></span>
<span data-ttu-id="4273c-123">Gibt eine OData-Filterklausel für unterstützte Bilder an.</span><span class="sxs-lookup"><span data-stu-id="4273c-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="4273c-124">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Bilder zurück, die vom Batchkonto unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4273c-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4273c-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4273c-125">-MaxCount</span></span>
<span data-ttu-id="4273c-126">Gibt die maximale Anzahl unterstützter Bilder an, die zurückzukehren sind.</span><span class="sxs-lookup"><span data-stu-id="4273c-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4273c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4273c-127">CommonParameters</span></span>
<span data-ttu-id="4273c-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4273c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4273c-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4273c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4273c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4273c-130">INPUTS</span></span>

### <span data-ttu-id="4273c-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4273c-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4273c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4273c-132">OUTPUTS</span></span>

### <span data-ttu-id="4273c-133">Microsoft.Azure.Commands.Batch. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="4273c-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="4273c-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4273c-134">NOTES</span></span>

## <span data-ttu-id="4273c-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4273c-135">RELATED LINKS</span></span>

[<span data-ttu-id="4273c-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4273c-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)