---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: 01dfcbbc9a8996ff351ecc9d88c688c96be345d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503689"
---
# <span data-ttu-id="e050d-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="e050d-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="e050d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e050d-102">SYNOPSIS</span></span>
<span data-ttu-id="e050d-103">Legt die Anzahl der Arbeitskraft Knoten in einem angegebenen Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="e050d-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e050d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e050d-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e050d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e050d-105">DESCRIPTION</span></span>
<span data-ttu-id="e050d-106">Das Cmdlet " **Set-AzureRmHDInsightClusterSize** " legt die Anzahl der Arbeits Knoten in einem angegebenen Azure HDInsight-Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="e050d-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e050d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e050d-107">EXAMPLES</span></span>

### <span data-ttu-id="e050d-108">Beispiel 1: Bestimmen der Größe eines angegebenen Clusters</span><span class="sxs-lookup"><span data-stu-id="e050d-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="e050d-109">Mit diesem Befehl wird die Größe des Clusters "Your-Hadoop-001" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e050d-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e050d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e050d-110">PARAMETERS</span></span>

### <span data-ttu-id="e050d-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e050d-111">-ClusterName</span></span>
<span data-ttu-id="e050d-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e050d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e050d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e050d-113">-DefaultProfile</span></span>
<span data-ttu-id="e050d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e050d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e050d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e050d-115">-ResourceGroupName</span></span>
<span data-ttu-id="e050d-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e050d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e050d-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="e050d-117">-TargetInstanceCount</span></span>
<span data-ttu-id="e050d-118">Gibt die gewünschte Anzahl von Arbeits Knoten im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e050d-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="e050d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e050d-119">CommonParameters</span></span>
<span data-ttu-id="e050d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e050d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e050d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e050d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e050d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e050d-122">INPUTS</span></span>

### <span data-ttu-id="e050d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="e050d-123">None</span></span>

## <span data-ttu-id="e050d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e050d-124">OUTPUTS</span></span>

### <span data-ttu-id="e050d-125">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="e050d-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="e050d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e050d-126">NOTES</span></span>

## <span data-ttu-id="e050d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e050d-127">RELATED LINKS</span></span>
