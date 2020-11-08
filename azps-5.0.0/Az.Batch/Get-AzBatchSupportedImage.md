---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179432"
---
# <span data-ttu-id="7abf1-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="7abf1-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="7abf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7abf1-102">SYNOPSIS</span></span>
<span data-ttu-id="7abf1-103">Ruft Batch gestützte Bilder für ein Stapelverarbeitungs Konto ab.</span><span class="sxs-lookup"><span data-stu-id="7abf1-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="7abf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7abf1-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7abf1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7abf1-105">DESCRIPTION</span></span>
<span data-ttu-id="7abf1-106">Das Cmdlet " **Get-AzBatchSupportedImage** " ruft unterstützte virtuelle Computer Bilder ab, die in einem Azure-Batch Konto verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7abf1-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="7abf1-107">Geben Sie das Konto mithilfe des *batchcontext* -Parameters an.</span><span class="sxs-lookup"><span data-stu-id="7abf1-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="7abf1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7abf1-108">EXAMPLES</span></span>

### <span data-ttu-id="7abf1-109">Beispiel 1: Abrufen aller verfügbaren unterstützten Bilder</span><span class="sxs-lookup"><span data-stu-id="7abf1-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="7abf1-110">Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, indem **Sie Get-AzBatchAccountKey** verwenden.</span><span class="sxs-lookup"><span data-stu-id="7abf1-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="7abf1-111">Der Befehl speichert den Kontext in der $Context Variablen, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7abf1-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="7abf1-112">Der zweite Befehl ruft alle verfügbaren unterstützten Bilder für dieses Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="7abf1-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="7abf1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7abf1-113">PARAMETERS</span></span>

### <span data-ttu-id="7abf1-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="7abf1-114">-BatchContext</span></span>
<span data-ttu-id="7abf1-115">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7abf1-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="7abf1-116">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7abf1-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="7abf1-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7abf1-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="7abf1-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="7abf1-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="7abf1-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7abf1-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7abf1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abf1-120">-DefaultProfile</span></span>
<span data-ttu-id="7abf1-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7abf1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7abf1-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="7abf1-122">-Filter</span></span>
<span data-ttu-id="7abf1-123">Gibt eine OData-Filterklausel für unterstützte Bilder an.</span><span class="sxs-lookup"><span data-stu-id="7abf1-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="7abf1-124">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Bilder zurück, die vom Batch Konto unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7abf1-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="7abf1-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7abf1-125">-MaxCount</span></span>
<span data-ttu-id="7abf1-126">Gibt die maximale Anzahl unterstützter Bilder an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7abf1-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="7abf1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abf1-127">CommonParameters</span></span>
<span data-ttu-id="7abf1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abf1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abf1-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7abf1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abf1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7abf1-130">INPUTS</span></span>

### <span data-ttu-id="7abf1-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7abf1-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7abf1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7abf1-132">OUTPUTS</span></span>

### <span data-ttu-id="7abf1-133">Microsoft.Azure.Commands.Batch. Models. PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="7abf1-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="7abf1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="7abf1-134">NOTES</span></span>

## <span data-ttu-id="7abf1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7abf1-135">RELATED LINKS</span></span>

[<span data-ttu-id="7abf1-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7abf1-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)