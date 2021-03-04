---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: 8b0bf38d68f4dbab815b6de1f056439cd5e88e3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946680"
---
# <span data-ttu-id="fba84-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fba84-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="fba84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba84-102">SYNOPSIS</span></span>
<span data-ttu-id="fba84-103">Deaktiviert die automatische Skalierung eines Pools.</span><span class="sxs-lookup"><span data-stu-id="fba84-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="fba84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fba84-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba84-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba84-105">DESCRIPTION</span></span>
<span data-ttu-id="fba84-106">Das **Cmdlet Disable-AzBatchAutoScale** deaktiviert die automatische Skalierung des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="fba84-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="fba84-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fba84-107">EXAMPLES</span></span>

### <span data-ttu-id="fba84-108">Beispiel 1: Deaktivieren der automatischen Skalierung eines Pools</span><span class="sxs-lookup"><span data-stu-id="fba84-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="fba84-109">Mit diesem Befehl wird die automatische Skalierung für den Pool mit dem Namen MyPool deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fba84-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="fba84-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fba84-110">PARAMETERS</span></span>

### <span data-ttu-id="fba84-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fba84-111">-BatchContext</span></span>
<span data-ttu-id="fba84-112">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fba84-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fba84-113">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="fba84-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fba84-114">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fba84-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fba84-115">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="fba84-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fba84-116">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="fba84-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fba84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba84-117">-DefaultProfile</span></span>
<span data-ttu-id="fba84-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fba84-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fba84-119">-ID</span><span class="sxs-lookup"><span data-stu-id="fba84-119">-Id</span></span>
<span data-ttu-id="fba84-120">Gibt die Objekt-ID des Pools an.</span><span class="sxs-lookup"><span data-stu-id="fba84-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="fba84-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba84-121">CommonParameters</span></span>
<span data-ttu-id="fba84-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba84-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba84-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fba84-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba84-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fba84-124">INPUTS</span></span>

### <span data-ttu-id="fba84-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fba84-125">System.String</span></span>

### <span data-ttu-id="fba84-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fba84-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fba84-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fba84-127">OUTPUTS</span></span>

### <span data-ttu-id="fba84-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="fba84-128">System.Void</span></span>

## <span data-ttu-id="fba84-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fba84-129">NOTES</span></span>

## <span data-ttu-id="fba84-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fba84-130">RELATED LINKS</span></span>

[<span data-ttu-id="fba84-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fba84-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="fba84-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fba84-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="fba84-133">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fba84-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


