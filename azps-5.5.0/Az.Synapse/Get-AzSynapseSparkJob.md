---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162852"
---
# <span data-ttu-id="aad30-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="aad30-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="aad30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad30-102">SYNOPSIS</span></span>
<span data-ttu-id="aad30-103">Ruft einen Synapse Analytics Spark-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="aad30-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="aad30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aad30-104">SYNTAX</span></span>

### <span data-ttu-id="aad30-105">GetSparkJobsByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aad30-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aad30-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aad30-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aad30-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aad30-107">DESCRIPTION</span></span>
<span data-ttu-id="aad30-108">Das **Cmdlet "Get-AzSynapseSparkJob"** erhält einen Azure Synapse Analytics Spark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="aad30-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="aad30-109">Wenn Sie keinen Auftrag angeben, erhält dieses Cmdlet alle Aufträge.</span><span class="sxs-lookup"><span data-stu-id="aad30-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="aad30-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aad30-110">EXAMPLES</span></span>

### <span data-ttu-id="aad30-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aad30-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="aad30-112">Dieser Befehl ruft alle Aufträge unter einem Sparkpool ab.</span><span class="sxs-lookup"><span data-stu-id="aad30-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="aad30-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aad30-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="aad30-114">Dieser Befehl ruft den Auftrag mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="aad30-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="aad30-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="aad30-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="aad30-116">Dieser Befehl ruft den Auftrag mit der angegebenen Anwendungs-ID ab.</span><span class="sxs-lookup"><span data-stu-id="aad30-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="aad30-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="aad30-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="aad30-118">Dieser Befehl ruft über die Pipeline alle Aufträge unter einem Sparkpool ab.</span><span class="sxs-lookup"><span data-stu-id="aad30-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="aad30-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aad30-119">PARAMETERS</span></span>

### <span data-ttu-id="aad30-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="aad30-120">-ApplicationId</span></span>
<span data-ttu-id="aad30-121">Der Anwendungsbezeichner der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="aad30-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="aad30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad30-122">-DefaultProfile</span></span>
<span data-ttu-id="aad30-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aad30-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aad30-124">-YYId</span><span class="sxs-lookup"><span data-stu-id="aad30-124">-LivyId</span></span>
<span data-ttu-id="aad30-125">Id des Sparkauftrags.</span><span class="sxs-lookup"><span data-stu-id="aad30-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad30-126">-Name</span><span class="sxs-lookup"><span data-stu-id="aad30-126">-Name</span></span>
<span data-ttu-id="aad30-127">Name des Sparkauftrags.</span><span class="sxs-lookup"><span data-stu-id="aad30-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="aad30-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="aad30-128">-SparkPoolName</span></span>
<span data-ttu-id="aad30-129">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="aad30-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad30-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="aad30-130">-SparkPoolObject</span></span>
<span data-ttu-id="aad30-131">Sparkpooleingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="aad30-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad30-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aad30-132">-WorkspaceName</span></span>
<span data-ttu-id="aad30-133">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="aad30-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad30-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad30-134">CommonParameters</span></span>
<span data-ttu-id="aad30-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad30-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad30-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aad30-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad30-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aad30-137">INPUTS</span></span>

### <span data-ttu-id="aad30-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="aad30-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="aad30-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aad30-139">OUTPUTS</span></span>

### <span data-ttu-id="aad30-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="aad30-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="aad30-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aad30-141">NOTES</span></span>

## <span data-ttu-id="aad30-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aad30-142">RELATED LINKS</span></span>
