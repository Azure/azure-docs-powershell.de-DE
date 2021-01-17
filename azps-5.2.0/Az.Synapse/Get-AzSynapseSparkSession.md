---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359454"
---
# <span data-ttu-id="a9b1d-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="a9b1d-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="a9b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b1d-103">Ruft eine Synapse Analytics Spark-Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="a9b1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9b1d-104">SYNTAX</span></span>

### <span data-ttu-id="a9b1d-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9b1d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9b1d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9b1d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9b1d-107">DESCRIPTION</span></span>
<span data-ttu-id="a9b1d-108">Das **Cmdlet "Get-AzSynapseSparkSession"** ruft Informationen zu einer Azure Synapse Analytics Spark-Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="a9b1d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9b1d-109">EXAMPLES</span></span>

### <span data-ttu-id="a9b1d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9b1d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="a9b1d-111">Dieser Befehl ruft alle Spark-Sitzungen unter dem angegebenen Sparkpool ab.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="a9b1d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9b1d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="a9b1d-113">Mit diesem Befehl wird die Sparksitzung mit der angegebenen neuen ID ruft.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="a9b1d-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a9b1d-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="a9b1d-115">Dieser Befehl ruft alle Spark-Sitzungen unter dem angegebenen Sparkpool über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="a9b1d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9b1d-116">PARAMETERS</span></span>

### <span data-ttu-id="a9b1d-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9b1d-117">-ApplicationId</span></span>
<span data-ttu-id="a9b1d-118">Der Anwendungsbezeichner der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="a9b1d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b1d-119">-DefaultProfile</span></span>
<span data-ttu-id="a9b1d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9b1d-121">-YYId</span><span class="sxs-lookup"><span data-stu-id="a9b1d-121">-LivyId</span></span>
<span data-ttu-id="a9b1d-122">Id der Sparksitzung.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="a9b1d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a9b1d-123">-Name</span></span>
<span data-ttu-id="a9b1d-124">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="a9b1d-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="a9b1d-125">-SparkPoolName</span></span>
<span data-ttu-id="a9b1d-126">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b1d-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="a9b1d-127">-SparkPoolObject</span></span>
<span data-ttu-id="a9b1d-128">Sparkpooleingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b1d-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9b1d-129">-WorkspaceName</span></span>
<span data-ttu-id="a9b1d-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b1d-131">CommonParameters</span></span>
<span data-ttu-id="a9b1d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b1d-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b1d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9b1d-134">INPUTS</span></span>

### <span data-ttu-id="a9b1d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a9b1d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="a9b1d-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9b1d-136">OUTPUTS</span></span>

### <span data-ttu-id="a9b1d-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="a9b1d-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="a9b1d-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9b1d-138">NOTES</span></span>

## <span data-ttu-id="a9b1d-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9b1d-139">RELATED LINKS</span></span>
