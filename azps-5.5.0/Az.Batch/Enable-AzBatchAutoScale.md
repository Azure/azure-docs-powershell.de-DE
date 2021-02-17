---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171600"
---
# <span data-ttu-id="59f42-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="59f42-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="59f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f42-102">SYNOPSIS</span></span>
<span data-ttu-id="59f42-103">Ermöglicht die automatische Skalierung eines Pools.</span><span class="sxs-lookup"><span data-stu-id="59f42-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="59f42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59f42-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59f42-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59f42-105">DESCRIPTION</span></span>
<span data-ttu-id="59f42-106">Das **Cmdlet "Enable-AzBatchAutoScale"** ermöglicht die automatische Skalierung des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="59f42-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="59f42-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59f42-107">EXAMPLES</span></span>

### <span data-ttu-id="59f42-108">Beispiel 1: Aktivieren der automatischen Skalierung für einen Pool</span><span class="sxs-lookup"><span data-stu-id="59f42-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="59f42-109">Der erste Befehl definiert eine Formel und speichert sie dann in der $Formula Variable.</span><span class="sxs-lookup"><span data-stu-id="59f42-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="59f42-110">Der zweite Befehl ermöglicht die automatische Skalierung des Pools namens "MyPool" mithilfe der Formel in $Formula.</span><span class="sxs-lookup"><span data-stu-id="59f42-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="59f42-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59f42-111">PARAMETERS</span></span>

### <span data-ttu-id="59f42-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="59f42-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="59f42-113">Gibt die Zeitdauer (in Minuten) an, die verstrichen ist, bevor die Größe des Pool gemäß der Formel für die AutoSkala automatisch angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="59f42-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="59f42-114">Der Standardwert ist 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="59f42-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="59f42-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="59f42-115">-AutoScaleFormula</span></span>
<span data-ttu-id="59f42-116">Gibt die Formel für die gewünschte Anzahl von Berechnungsknoten im Pool an.</span><span class="sxs-lookup"><span data-stu-id="59f42-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="59f42-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="59f42-117">-BatchContext</span></span>
<span data-ttu-id="59f42-118">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59f42-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="59f42-119">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="59f42-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="59f42-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="59f42-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="59f42-121">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="59f42-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="59f42-122">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="59f42-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="59f42-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f42-123">-DefaultProfile</span></span>
<span data-ttu-id="59f42-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59f42-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59f42-125">-ID</span><span class="sxs-lookup"><span data-stu-id="59f42-125">-Id</span></span>
<span data-ttu-id="59f42-126">Gibt die Objekt-ID des Pools an, für den die automatische Skalierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="59f42-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="59f42-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f42-127">CommonParameters</span></span>
<span data-ttu-id="59f42-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f42-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f42-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59f42-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f42-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59f42-130">INPUTS</span></span>

### <span data-ttu-id="59f42-131">System.String</span><span class="sxs-lookup"><span data-stu-id="59f42-131">System.String</span></span>

### <span data-ttu-id="59f42-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="59f42-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="59f42-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59f42-133">OUTPUTS</span></span>

### <span data-ttu-id="59f42-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="59f42-134">System.Void</span></span>

## <span data-ttu-id="59f42-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59f42-135">NOTES</span></span>

## <span data-ttu-id="59f42-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59f42-136">RELATED LINKS</span></span>

[<span data-ttu-id="59f42-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="59f42-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="59f42-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="59f42-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="59f42-139">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="59f42-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
