---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: f232d1df7bef3800fc54b2469a51f3f69c8d4fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496149"
---
# <span data-ttu-id="9fede-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fede-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="9fede-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fede-102">SYNOPSIS</span></span>
<span data-ttu-id="9fede-103">Ruft alle Azure HDInsight-Cluster ab, die dem aktuellen Abonnement oder einer angegebenen Ressourcengruppe zugeordnet sind, oder Ruft einen bestimmten Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="9fede-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fede-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fede-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fede-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fede-105">DESCRIPTION</span></span>
<span data-ttu-id="9fede-106">Das Cmdlet " **Get-AzureRmHDInsightCluster** " listet die Azure HDInsight-Dienst Cluster für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="9fede-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="9fede-107">Verwenden Sie den Parameter *Clustername* , um Details zu einem bestimmten Cluster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9fede-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="9fede-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fede-108">EXAMPLES</span></span>

### <span data-ttu-id="9fede-109">Beispiel 1: Auflisten aller Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="9fede-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="9fede-110">Dieser Befehl listet alle Azure HDInsight-Cluster auf.</span><span class="sxs-lookup"><span data-stu-id="9fede-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="9fede-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fede-111">PARAMETERS</span></span>

### <span data-ttu-id="9fede-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="9fede-112">-ClusterName</span></span>
<span data-ttu-id="9fede-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="9fede-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9fede-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fede-114">-DefaultProfile</span></span>
<span data-ttu-id="9fede-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9fede-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fede-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fede-116">-ResourceGroupName</span></span>
<span data-ttu-id="9fede-117">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9fede-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9fede-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fede-118">CommonParameters</span></span>
<span data-ttu-id="9fede-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fede-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fede-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fede-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fede-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fede-121">INPUTS</span></span>

### <span data-ttu-id="9fede-122">Keine</span><span class="sxs-lookup"><span data-stu-id="9fede-122">None</span></span>

## <span data-ttu-id="9fede-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fede-123">OUTPUTS</span></span>

### <span data-ttu-id="9fede-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fede-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="9fede-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fede-125">NOTES</span></span>

## <span data-ttu-id="9fede-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fede-126">RELATED LINKS</span></span>

[<span data-ttu-id="9fede-127">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fede-127">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="9fede-128">Verwenden von-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9fede-128">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


