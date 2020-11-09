---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296331"
---
# <span data-ttu-id="ef389-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="ef389-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="ef389-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef389-102">SYNOPSIS</span></span>
<span data-ttu-id="ef389-103">Legt die Anzahl der Arbeitskraft Knoten in einem angegebenen Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="ef389-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="ef389-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef389-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef389-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef389-105">DESCRIPTION</span></span>
<span data-ttu-id="ef389-106">Das Cmdlet " **Set-AzHDInsightClusterSize** " legt die Anzahl der Arbeits Knoten in einem angegebenen Azure HDInsight-Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="ef389-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ef389-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef389-107">EXAMPLES</span></span>

### <span data-ttu-id="ef389-108">Beispiel 1: Bestimmen der Größe eines angegebenen Clusters</span><span class="sxs-lookup"><span data-stu-id="ef389-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="ef389-109">Mit diesem Befehl wird die Größe des Clusters "Your-Hadoop-001" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef389-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ef389-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef389-110">PARAMETERS</span></span>

### <span data-ttu-id="ef389-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ef389-111">-ClusterName</span></span>
<span data-ttu-id="ef389-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ef389-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ef389-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef389-113">-DefaultProfile</span></span>
<span data-ttu-id="ef389-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ef389-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef389-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef389-115">-ResourceGroupName</span></span>
<span data-ttu-id="ef389-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ef389-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ef389-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="ef389-117">-TargetInstanceCount</span></span>
<span data-ttu-id="ef389-118">Gibt die gewünschte Anzahl von Arbeits Knoten im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="ef389-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="ef389-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef389-119">CommonParameters</span></span>
<span data-ttu-id="ef389-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef389-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef389-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef389-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef389-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef389-122">INPUTS</span></span>

### <span data-ttu-id="ef389-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ef389-123">None</span></span>

## <span data-ttu-id="ef389-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef389-124">OUTPUTS</span></span>

### <span data-ttu-id="ef389-125">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="ef389-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="ef389-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef389-126">NOTES</span></span>

## <span data-ttu-id="ef389-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef389-127">RELATED LINKS</span></span>
