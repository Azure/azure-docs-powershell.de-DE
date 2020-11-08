---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173371"
---
# <span data-ttu-id="1abbe-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="1abbe-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="1abbe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1abbe-102">SYNOPSIS</span></span>
<span data-ttu-id="1abbe-103">Ruft eine Synapse Analytics Spark Job.</span><span class="sxs-lookup"><span data-stu-id="1abbe-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="1abbe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1abbe-104">SYNTAX</span></span>

### <span data-ttu-id="1abbe-105">GetSparkJobsByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1abbe-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1abbe-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1abbe-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1abbe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1abbe-107">DESCRIPTION</span></span>
<span data-ttu-id="1abbe-108">Das Cmdlet " **Get-AzSynapseSparkJob** " erhält eine Azure Synapse Analytics Spark-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1abbe-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="1abbe-109">Wenn Sie keinen Auftrag angeben, ruft dieses Cmdlet alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="1abbe-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="1abbe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1abbe-110">EXAMPLES</span></span>

### <span data-ttu-id="1abbe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1abbe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="1abbe-112">Dieser Befehl ruft alle Aufträge unter einem Spark-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="1abbe-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="1abbe-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1abbe-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="1abbe-114">Mit diesem Befehl wird der Auftrag mit der angegebenen ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1abbe-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="1abbe-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1abbe-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="1abbe-116">Mit diesem Befehl wird der Auftrag mit der angegebenen Anwendungs-ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1abbe-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="1abbe-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="1abbe-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="1abbe-118">Dieser Befehl ruft alle Aufträge unter einem Spark-Pool durch Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="1abbe-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="1abbe-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1abbe-119">PARAMETERS</span></span>

### <span data-ttu-id="1abbe-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1abbe-120">-ApplicationId</span></span>
<span data-ttu-id="1abbe-121">Die Anwendungs-ID der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1abbe-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="1abbe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abbe-122">-DefaultProfile</span></span>
<span data-ttu-id="1abbe-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1abbe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1abbe-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="1abbe-124">-LivyId</span></span>
<span data-ttu-id="1abbe-125">Kennung des Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1abbe-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="1abbe-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1abbe-126">-Name</span></span>
<span data-ttu-id="1abbe-127">Name des Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1abbe-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="1abbe-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="1abbe-128">-SparkPoolName</span></span>
<span data-ttu-id="1abbe-129">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="1abbe-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1abbe-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="1abbe-130">-SparkPoolObject</span></span>
<span data-ttu-id="1abbe-131">Spark Pool-Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="1abbe-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1abbe-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1abbe-132">-WorkspaceName</span></span>
<span data-ttu-id="1abbe-133">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1abbe-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1abbe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abbe-134">CommonParameters</span></span>
<span data-ttu-id="1abbe-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1abbe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abbe-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1abbe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abbe-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1abbe-137">INPUTS</span></span>

### <span data-ttu-id="1abbe-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1abbe-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="1abbe-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1abbe-139">OUTPUTS</span></span>

### <span data-ttu-id="1abbe-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="1abbe-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="1abbe-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="1abbe-141">NOTES</span></span>

## <span data-ttu-id="1abbe-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1abbe-142">RELATED LINKS</span></span>
