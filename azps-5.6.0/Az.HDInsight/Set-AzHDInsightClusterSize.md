---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: eba552917b17b9bb1337a2b62c83d3d1adebc1cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944158"
---
# <span data-ttu-id="94b62-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="94b62-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="94b62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b62-102">SYNOPSIS</span></span>
<span data-ttu-id="94b62-103">Legt die Anzahl der Workerknoten in einem angegebenen Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="94b62-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="94b62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94b62-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94b62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94b62-105">DESCRIPTION</span></span>
<span data-ttu-id="94b62-106">Das **Cmdlet Set-AzHDInsightClusterSize** legt die Anzahl der Workerknoten in einem angegebenen Azure HDInsight-Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="94b62-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="94b62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94b62-107">EXAMPLES</span></span>

### <span data-ttu-id="94b62-108">Beispiel 1: Festlegen der Größe eines angegebenen Clusters</span><span class="sxs-lookup"><span data-stu-id="94b62-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="94b62-109">Mit diesem Befehl wird die Größe des Clusters mit dem Namen "your-hadoop-001" bestimmt.</span><span class="sxs-lookup"><span data-stu-id="94b62-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="94b62-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="94b62-110">PARAMETERS</span></span>

### <span data-ttu-id="94b62-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94b62-111">-ClusterName</span></span>
<span data-ttu-id="94b62-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="94b62-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b62-113">-DefaultProfile</span></span>
<span data-ttu-id="94b62-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="94b62-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94b62-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b62-115">-ResourceGroupName</span></span>
<span data-ttu-id="94b62-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="94b62-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="94b62-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="94b62-117">-TargetInstanceCount</span></span>
<span data-ttu-id="94b62-118">Gibt die gewünschte Anzahl von Workerknoten im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="94b62-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b62-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b62-119">CommonParameters</span></span>
<span data-ttu-id="94b62-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b62-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b62-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94b62-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b62-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94b62-122">INPUTS</span></span>

### <span data-ttu-id="94b62-123">Keine</span><span class="sxs-lookup"><span data-stu-id="94b62-123">None</span></span>

## <span data-ttu-id="94b62-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94b62-124">OUTPUTS</span></span>

### <span data-ttu-id="94b62-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="94b62-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="94b62-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="94b62-126">NOTES</span></span>

## <span data-ttu-id="94b62-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="94b62-127">RELATED LINKS</span></span>
