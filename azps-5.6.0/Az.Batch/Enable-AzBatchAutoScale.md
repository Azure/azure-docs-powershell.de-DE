---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: b7b63da46832c94466a58bb04f62436a6778af96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939723"
---
# <span data-ttu-id="bb8f5-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="bb8f5-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="bb8f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8f5-103">Ermöglicht die automatische Skalierung eines Pools.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="bb8f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb8f5-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb8f5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb8f5-105">DESCRIPTION</span></span>
<span data-ttu-id="bb8f5-106">Das **Enable-AzBatchAutoScale-Cmdlet** ermöglicht die automatische Skalierung des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="bb8f5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb8f5-107">EXAMPLES</span></span>

### <span data-ttu-id="bb8f5-108">Beispiel 1: Aktivieren der automatischen Skalierung für einen Pool</span><span class="sxs-lookup"><span data-stu-id="bb8f5-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="bb8f5-109">Der erste Befehl definiert eine Formel und speichert sie dann in der $Formula Variablen.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="bb8f5-110">Der zweite Befehl ermöglicht die automatische Skalierung für den Pool mit dem Namen "MyPool" mithilfe der Formel in $Formula.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="bb8f5-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bb8f5-111">PARAMETERS</span></span>

### <span data-ttu-id="bb8f5-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="bb8f5-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="bb8f5-113">Gibt den Zeitraum (in Minuten) an, der verstrichen ist, bevor die Poolgröße gemäß der Formel "AutoScale" automatisch angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="bb8f5-114">Der Standardwert beträgt 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f5-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="bb8f5-115">-AutoScaleFormula</span></span>
<span data-ttu-id="bb8f5-116">Gibt die Formel für die gewünschte Anzahl von Computeknoten im Pool an.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f5-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bb8f5-117">-BatchContext</span></span>
<span data-ttu-id="bb8f5-118">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bb8f5-119">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bb8f5-120">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bb8f5-121">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bb8f5-122">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bb8f5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8f5-123">-DefaultProfile</span></span>
<span data-ttu-id="bb8f5-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb8f5-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bb8f5-125">-Id</span></span>
<span data-ttu-id="bb8f5-126">Gibt die Objekt-ID des Pools an, für den die automatische Skalierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="bb8f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8f5-127">CommonParameters</span></span>
<span data-ttu-id="bb8f5-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8f5-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb8f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8f5-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb8f5-130">INPUTS</span></span>

### <span data-ttu-id="bb8f5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bb8f5-131">System.String</span></span>

### <span data-ttu-id="bb8f5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bb8f5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bb8f5-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb8f5-133">OUTPUTS</span></span>

### <span data-ttu-id="bb8f5-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="bb8f5-134">System.Void</span></span>

## <span data-ttu-id="bb8f5-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bb8f5-135">NOTES</span></span>

## <span data-ttu-id="bb8f5-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bb8f5-136">RELATED LINKS</span></span>

[<span data-ttu-id="bb8f5-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="bb8f5-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="bb8f5-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="bb8f5-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="bb8f5-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bb8f5-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
