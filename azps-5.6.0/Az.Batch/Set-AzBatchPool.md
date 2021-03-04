---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 26a280ef567ed09ff14cf143048aadceeeed29e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939003"
---
# <span data-ttu-id="5ce9f-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5ce9f-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="5ce9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ce9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce9f-103">Aktualisiert die Eigenschaften eines Pools.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="5ce9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ce9f-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ce9f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ce9f-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce9f-106">Das **Cmdlet Set-AzBatchPool** aktualisiert die Eigenschaften eines Pools im Azure Batch-Dienst.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="5ce9f-107">Verwenden Sie Get-AzBatchPool-Cmdlet, um ein **PSCloudPool-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="5ce9f-108">Ändern Sie die Eigenschaften dieses Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Batchdienst zu commiten.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="5ce9f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ce9f-109">EXAMPLES</span></span>

### <span data-ttu-id="5ce9f-110">Beispiel 1: Aktualisieren eines Pools</span><span class="sxs-lookup"><span data-stu-id="5ce9f-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="5ce9f-111">Der erste Befehl ruft einen Pool mithilfe von **Get-AzBatchPool ab** und speichert ihn dann in der $Pool Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="5ce9f-112">Mit den nächsten drei Befehlen wird die Startaufgabesspezifikation für das $Pool geändert.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="5ce9f-113">Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in $Pool.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="5ce9f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5ce9f-114">PARAMETERS</span></span>

### <span data-ttu-id="5ce9f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5ce9f-115">-BatchContext</span></span>
<span data-ttu-id="5ce9f-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5ce9f-117">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5ce9f-118">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5ce9f-119">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5ce9f-120">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5ce9f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce9f-121">-DefaultProfile</span></span>
<span data-ttu-id="5ce9f-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ce9f-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="5ce9f-123">-Pool</span></span>
<span data-ttu-id="5ce9f-124">Gibt den **PSCloudPool an,** auf den dieses Cmdlet den Batchdienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce9f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce9f-125">CommonParameters</span></span>
<span data-ttu-id="5ce9f-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce9f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce9f-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ce9f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce9f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ce9f-128">INPUTS</span></span>

### <span data-ttu-id="5ce9f-129">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="5ce9f-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="5ce9f-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5ce9f-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5ce9f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ce9f-131">OUTPUTS</span></span>

### <span data-ttu-id="5ce9f-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="5ce9f-132">System.Void</span></span>

## <span data-ttu-id="5ce9f-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5ce9f-133">NOTES</span></span>

## <span data-ttu-id="5ce9f-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5ce9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ce9f-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5ce9f-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="5ce9f-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5ce9f-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5ce9f-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5ce9f-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="5ce9f-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5ce9f-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="5ce9f-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5ce9f-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
