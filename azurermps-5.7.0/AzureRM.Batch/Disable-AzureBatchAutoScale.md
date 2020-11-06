---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505802"
---
# <span data-ttu-id="5c40d-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5c40d-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="5c40d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c40d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c40d-103">Deaktiviert die automatische Skalierung eines Pools.</span><span class="sxs-lookup"><span data-stu-id="5c40d-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c40d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c40d-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c40d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c40d-105">DESCRIPTION</span></span>
<span data-ttu-id="5c40d-106">Das Cmdlet **Disable-AzureBatchAutoScale** deaktiviert die automatische Skalierung des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="5c40d-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="5c40d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c40d-107">EXAMPLES</span></span>

### <span data-ttu-id="5c40d-108">Beispiel 1: Deaktivieren der automatischen Skalierung eines Pools</span><span class="sxs-lookup"><span data-stu-id="5c40d-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="5c40d-109">Mit diesem Befehl wird die automatische Skalierung für den Pool mit dem Namen MyPool deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5c40d-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="5c40d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c40d-110">PARAMETERS</span></span>

### <span data-ttu-id="5c40d-111">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="5c40d-111">-BatchContext</span></span>
<span data-ttu-id="5c40d-112">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c40d-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5c40d-113">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c40d-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5c40d-114">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5c40d-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5c40d-115">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c40d-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5c40d-116">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5c40d-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c40d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c40d-117">-DefaultProfile</span></span>
<span data-ttu-id="5c40d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c40d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c40d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5c40d-119">-Id</span></span>
<span data-ttu-id="5c40d-120">Gibt die Objekt-ID des Pools an.</span><span class="sxs-lookup"><span data-stu-id="5c40d-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c40d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c40d-121">CommonParameters</span></span>
<span data-ttu-id="5c40d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c40d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c40d-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c40d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c40d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c40d-124">INPUTS</span></span>

### <span data-ttu-id="5c40d-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5c40d-125">BatchAccountContext</span></span>
<span data-ttu-id="5c40d-126">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c40d-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5c40d-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5c40d-127">String</span></span>
<span data-ttu-id="5c40d-128">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c40d-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5c40d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c40d-129">OUTPUTS</span></span>

## <span data-ttu-id="5c40d-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c40d-130">NOTES</span></span>

## <span data-ttu-id="5c40d-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c40d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5c40d-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5c40d-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="5c40d-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5c40d-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="5c40d-134">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c40d-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


