---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173660"
---
# <span data-ttu-id="7c664-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="7c664-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="7c664-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c664-102">SYNOPSIS</span></span>
<span data-ttu-id="7c664-103">Wartet darauf, dass ein Synapse Analytics Spark-Auftrag abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="7c664-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="7c664-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c664-104">SYNTAX</span></span>

### <span data-ttu-id="7c664-105">WaitSparkJobByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c664-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c664-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c664-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c664-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c664-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c664-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c664-108">DESCRIPTION</span></span>
<span data-ttu-id="7c664-109">Das **Wait-AzSynapseSparkJob-** Cmdlet wartet darauf, dass ein Azure Synapse-Analyse Auftrag abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="7c664-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="7c664-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c664-110">EXAMPLES</span></span>

### <span data-ttu-id="7c664-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c664-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="7c664-112">Dieser Befehl wartet auf den Auftrag mit der angegebenen ID, um ihn abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7c664-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="7c664-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c664-113">PARAMETERS</span></span>

### <span data-ttu-id="7c664-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c664-114">-DefaultProfile</span></span>
<span data-ttu-id="7c664-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c664-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c664-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="7c664-116">-LivyId</span></span>
<span data-ttu-id="7c664-117">Kennung des Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="7c664-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="7c664-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="7c664-118">-SparkJobObject</span></span>
<span data-ttu-id="7c664-119">Spark Job Input-Objekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="7c664-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7c664-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="7c664-120">-SparkPoolName</span></span>
<span data-ttu-id="7c664-121">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="7c664-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="7c664-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="7c664-122">-SparkPoolObject</span></span>
<span data-ttu-id="7c664-123">Spark Pool-Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="7c664-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7c664-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c664-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="7c664-125">Die maximale Wartezeit, bevor ein Fehler auftritt. Der Standardwert ist "nie Timeout".</span><span class="sxs-lookup"><span data-stu-id="7c664-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="7c664-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c664-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="7c664-127">Das Abrufintervall zwischen überprüft den Auftragsstatus in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7c664-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="7c664-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c664-128">-WorkspaceName</span></span>
<span data-ttu-id="7c664-129">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7c664-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7c664-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c664-130">CommonParameters</span></span>
<span data-ttu-id="7c664-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c664-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c664-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c664-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c664-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c664-133">INPUTS</span></span>

### <span data-ttu-id="7c664-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="7c664-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="7c664-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="7c664-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="7c664-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c664-136">OUTPUTS</span></span>

### <span data-ttu-id="7c664-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c664-137">System.Boolean</span></span>

## <span data-ttu-id="7c664-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c664-138">NOTES</span></span>

## <span data-ttu-id="7c664-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c664-139">RELATED LINKS</span></span>
