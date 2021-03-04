---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: fa658b7727c07b7457c2a10c1ac42e3fdb5fe347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946720"
---
# <span data-ttu-id="f088f-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="f088f-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="f088f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f088f-102">SYNOPSIS</span></span>
<span data-ttu-id="f088f-103">Wartet auf den Abschluss eines Synapse Analytics Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="f088f-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="f088f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f088f-104">SYNTAX</span></span>

### <span data-ttu-id="f088f-105">WaitSparkJobByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f088f-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f088f-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f088f-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f088f-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f088f-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f088f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f088f-108">DESCRIPTION</span></span>
<span data-ttu-id="f088f-109">Das **Cmdlet Wait-AzSynapseSparkJob** wartet auf den Abschluss eines Azure Synapse Analytics-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="f088f-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="f088f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f088f-110">EXAMPLES</span></span>

### <span data-ttu-id="f088f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f088f-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="f088f-112">Dieser Befehl wartet, bis der Auftrag mit der angegebenen ID abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f088f-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="f088f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f088f-113">PARAMETERS</span></span>

### <span data-ttu-id="f088f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f088f-114">-DefaultProfile</span></span>
<span data-ttu-id="f088f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f088f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f088f-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="f088f-116">-LivyId</span></span>
<span data-ttu-id="f088f-117">Bezeichner des Sparkauftrags.</span><span class="sxs-lookup"><span data-stu-id="f088f-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f088f-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="f088f-118">-SparkJobObject</span></span>
<span data-ttu-id="f088f-119">Sparkauftragseingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f088f-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f088f-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f088f-120">-SparkPoolName</span></span>
<span data-ttu-id="f088f-121">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="f088f-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f088f-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="f088f-122">-SparkPoolObject</span></span>
<span data-ttu-id="f088f-123">Spark pool input object, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="f088f-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f088f-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="f088f-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="f088f-125">Die maximale Wartezeit vor dem Fehler. Der Standardwert ist das Nie-Timeout.</span><span class="sxs-lookup"><span data-stu-id="f088f-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="f088f-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f088f-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="f088f-127">Das Abrufintervall zwischen den Überprüfungen für den Auftragsstatus in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f088f-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="f088f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f088f-128">-WorkspaceName</span></span>
<span data-ttu-id="f088f-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f088f-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f088f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f088f-130">CommonParameters</span></span>
<span data-ttu-id="f088f-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f088f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f088f-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f088f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f088f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f088f-133">INPUTS</span></span>

### <span data-ttu-id="f088f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f088f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="f088f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="f088f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="f088f-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f088f-136">OUTPUTS</span></span>

### <span data-ttu-id="f088f-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f088f-137">System.Boolean</span></span>

## <span data-ttu-id="f088f-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f088f-138">NOTES</span></span>

## <span data-ttu-id="f088f-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f088f-139">RELATED LINKS</span></span>
