---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380916"
---
# <span data-ttu-id="5cf45-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="5cf45-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="5cf45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf45-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf45-103">Wartet auf den Abschluss eines Synapse Analytics Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="5cf45-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="5cf45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cf45-104">SYNTAX</span></span>

### <span data-ttu-id="5cf45-105">WaitSparkJobByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cf45-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5cf45-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cf45-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cf45-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cf45-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cf45-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cf45-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf45-109">Das **Cmdlet "Wait-AzSynapseSparkJob"** wartet auf den Abschluss eines Azure Synapse Analytics-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="5cf45-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="5cf45-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5cf45-110">EXAMPLES</span></span>

### <span data-ttu-id="5cf45-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cf45-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="5cf45-112">Dieser Befehl wartet auf den Abschluss des Auftrags mit der angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="5cf45-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="5cf45-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cf45-113">PARAMETERS</span></span>

### <span data-ttu-id="5cf45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf45-114">-DefaultProfile</span></span>
<span data-ttu-id="5cf45-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cf45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf45-116">-YYId</span><span class="sxs-lookup"><span data-stu-id="5cf45-116">-LivyId</span></span>
<span data-ttu-id="5cf45-117">Id des Sparkauftrags.</span><span class="sxs-lookup"><span data-stu-id="5cf45-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="5cf45-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="5cf45-118">-SparkJobObject</span></span>
<span data-ttu-id="5cf45-119">Sparkauftragseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5cf45-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5cf45-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="5cf45-120">-SparkPoolName</span></span>
<span data-ttu-id="5cf45-121">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="5cf45-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="5cf45-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="5cf45-122">-SparkPoolObject</span></span>
<span data-ttu-id="5cf45-123">Sparkpooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5cf45-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5cf45-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5cf45-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="5cf45-125">Die maximale Wartezeit vor dem Fehler. Der Standardwert ist", dass "timeout" niemals verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cf45-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="5cf45-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5cf45-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="5cf45-127">Das Abfrageintervall zwischen der Überprüfung des Auftragsstatus in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5cf45-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="5cf45-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5cf45-128">-WorkspaceName</span></span>
<span data-ttu-id="5cf45-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="5cf45-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5cf45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf45-130">CommonParameters</span></span>
<span data-ttu-id="5cf45-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf45-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cf45-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf45-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5cf45-133">INPUTS</span></span>

### <span data-ttu-id="5cf45-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5cf45-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="5cf45-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="5cf45-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="5cf45-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5cf45-136">OUTPUTS</span></span>

### <span data-ttu-id="5cf45-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cf45-137">System.Boolean</span></span>

## <span data-ttu-id="5cf45-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5cf45-138">NOTES</span></span>

## <span data-ttu-id="5cf45-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5cf45-139">RELATED LINKS</span></span>
