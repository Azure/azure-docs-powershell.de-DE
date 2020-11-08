---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008300"
---
# <span data-ttu-id="c06c6-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c06c6-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="c06c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c06c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c06c6-103">Ruft alle Azure HDInsight-Cluster ab, die dem aktuellen Abonnement oder einer angegebenen Ressourcengruppe zugeordnet sind, oder Ruft einen bestimmten Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="c06c6-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="c06c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c06c6-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c06c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c06c6-105">DESCRIPTION</span></span>
<span data-ttu-id="c06c6-106">Das Cmdlet " **Get-AzHDInsightCluster** " listet die Azure HDInsight-Dienst Cluster für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="c06c6-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="c06c6-107">Verwenden Sie den Parameter *Clustername* , um Details zu einem bestimmten Cluster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c06c6-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="c06c6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c06c6-108">EXAMPLES</span></span>

### <span data-ttu-id="c06c6-109">Beispiel 1: Auflisten aller Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="c06c6-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="c06c6-110">Dieser Befehl listet alle Azure HDInsight-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="c06c6-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="c06c6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c06c6-111">PARAMETERS</span></span>

### <span data-ttu-id="c06c6-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c06c6-112">-ClusterName</span></span>
<span data-ttu-id="c06c6-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="c06c6-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c06c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06c6-114">-DefaultProfile</span></span>
<span data-ttu-id="c06c6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c06c6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c06c6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06c6-116">-ResourceGroupName</span></span>
<span data-ttu-id="c06c6-117">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c06c6-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c06c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06c6-118">CommonParameters</span></span>
<span data-ttu-id="c06c6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c06c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06c6-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c06c6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06c6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c06c6-121">INPUTS</span></span>

### <span data-ttu-id="c06c6-122">Keine</span><span class="sxs-lookup"><span data-stu-id="c06c6-122">None</span></span>

## <span data-ttu-id="c06c6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c06c6-123">OUTPUTS</span></span>

### <span data-ttu-id="c06c6-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c06c6-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c06c6-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="c06c6-125">NOTES</span></span>

## <span data-ttu-id="c06c6-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c06c6-126">RELATED LINKS</span></span>

[<span data-ttu-id="c06c6-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c06c6-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="c06c6-128">Verwenden von-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c06c6-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


