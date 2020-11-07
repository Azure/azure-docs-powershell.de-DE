---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: d20a52c3e907bd981bc0a692ebb4aa44495d0960
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847891"
---
# <span data-ttu-id="c0b4a-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c0b4a-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="c0b4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b4a-103">Deaktiviert die automatische Skalierung eines Pools.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="c0b4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0b4a-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0b4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b4a-106">Das Cmdlet **Disable-AzBatchAutoScale** deaktiviert die automatische Skalierung des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="c0b4a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0b4a-107">EXAMPLES</span></span>

### <span data-ttu-id="c0b4a-108">Beispiel 1: Deaktivieren der automatischen Skalierung eines Pools</span><span class="sxs-lookup"><span data-stu-id="c0b4a-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="c0b4a-109">Mit diesem Befehl wird die automatische Skalierung für den Pool mit dem Namen MyPool deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="c0b4a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="c0b4a-111">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="c0b4a-111">-BatchContext</span></span>
<span data-ttu-id="c0b4a-112">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c0b4a-113">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c0b4a-114">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c0b4a-115">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c0b4a-116">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c0b4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b4a-117">-DefaultProfile</span></span>
<span data-ttu-id="c0b4a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0b4a-119">-ID</span><span class="sxs-lookup"><span data-stu-id="c0b4a-119">-Id</span></span>
<span data-ttu-id="c0b4a-120">Gibt die Objekt-ID des Pools an.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b4a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b4a-121">CommonParameters</span></span>
<span data-ttu-id="c0b4a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b4a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b4a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0b4a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b4a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0b4a-124">INPUTS</span></span>

### <span data-ttu-id="c0b4a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c0b4a-125">System.String</span></span>

### <span data-ttu-id="c0b4a-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c0b4a-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c0b4a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0b4a-127">OUTPUTS</span></span>

### <span data-ttu-id="c0b4a-128">System. void</span><span class="sxs-lookup"><span data-stu-id="c0b4a-128">System.Void</span></span>

## <span data-ttu-id="c0b4a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0b4a-129">NOTES</span></span>

## <span data-ttu-id="c0b4a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0b4a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0b4a-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c0b4a-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="c0b4a-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c0b4a-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="c0b4a-133">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c0b4a-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


