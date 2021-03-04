---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: 612ca41bf96a1372cda2b2abe984a56c1ec5411c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950480"
---
# <span data-ttu-id="aceeb-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="aceeb-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="aceeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aceeb-102">SYNOPSIS</span></span>
<span data-ttu-id="aceeb-103">Ruft eine Synapse Analytics Spark-Anweisung ab.</span><span class="sxs-lookup"><span data-stu-id="aceeb-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="aceeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aceeb-104">SYNTAX</span></span>

### <span data-ttu-id="aceeb-105">GetSparkStatementsByIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aceeb-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aceeb-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aceeb-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aceeb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aceeb-107">DESCRIPTION</span></span>
<span data-ttu-id="aceeb-108">Das **Cmdlet Get-AzSynapseSparkStatement** ruft Informationen zu einer Azure Synapse Analytics Spark-Anweisung ab.</span><span class="sxs-lookup"><span data-stu-id="aceeb-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="aceeb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aceeb-109">EXAMPLES</span></span>

### <span data-ttu-id="aceeb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aceeb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="aceeb-111">Dieser Befehl ruft alle Spark-Anweisungen unter einer Spark-Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="aceeb-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="aceeb-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aceeb-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="aceeb-113">Dieser Befehl ruft die Spark-Anweisung mit der angegebenen Lebenswert-ID ab.</span><span class="sxs-lookup"><span data-stu-id="aceeb-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="aceeb-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="aceeb-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="aceeb-115">Dieser Befehl ruft alle Spark-Anweisungen unter einer Spark-Sitzung per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="aceeb-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="aceeb-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aceeb-116">PARAMETERS</span></span>

### <span data-ttu-id="aceeb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aceeb-117">-DefaultProfile</span></span>
<span data-ttu-id="aceeb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aceeb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aceeb-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="aceeb-119">-LivyId</span></span>
<span data-ttu-id="aceeb-120">Bezeichner der Spark-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="aceeb-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="aceeb-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="aceeb-121">-SessionId</span></span>
<span data-ttu-id="aceeb-122">Bezeichner der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="aceeb-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceeb-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="aceeb-123">-SessionObject</span></span>
<span data-ttu-id="aceeb-124">Spark pool input object, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="aceeb-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aceeb-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="aceeb-125">-SparkPoolName</span></span>
<span data-ttu-id="aceeb-126">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="aceeb-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceeb-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aceeb-127">-WorkspaceName</span></span>
<span data-ttu-id="aceeb-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="aceeb-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceeb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aceeb-129">CommonParameters</span></span>
<span data-ttu-id="aceeb-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aceeb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aceeb-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aceeb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aceeb-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aceeb-132">INPUTS</span></span>

### <span data-ttu-id="aceeb-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="aceeb-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="aceeb-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aceeb-134">OUTPUTS</span></span>

### <span data-ttu-id="aceeb-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="aceeb-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="aceeb-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aceeb-136">NOTES</span></span>

## <span data-ttu-id="aceeb-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aceeb-137">RELATED LINKS</span></span>
