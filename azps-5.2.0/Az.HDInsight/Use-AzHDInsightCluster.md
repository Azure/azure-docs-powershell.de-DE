---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289649"
---
# <span data-ttu-id="71330-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="71330-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="71330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71330-102">SYNOPSIS</span></span>
<span data-ttu-id="71330-103">Wählt einen Cluster aus, der mit dem cmdlet Invoke-RmAzureHDInsightHiveJob verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="71330-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="71330-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71330-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71330-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71330-105">DESCRIPTION</span></span>
<span data-ttu-id="71330-106">Das **Cmdlet "Use-AzHDInsightCluster"** wählt den Azure HDInsight-Cluster für das cmdlet Invoke-AzHDInsightHiveJob aus, das zum Übermitteln von Aufträgen mit Strukture verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="71330-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="71330-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71330-107">EXAMPLES</span></span>

### <span data-ttu-id="71330-108">Beispiel 1: Auswählen eines Clusters für die Übermittlung von Strukturabfragen</span><span class="sxs-lookup"><span data-stu-id="71330-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="71330-109">Mit diesem Befehl wird ein Cluster für eine Strukture-Abfrageübermittlung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="71330-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="71330-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71330-110">PARAMETERS</span></span>

### <span data-ttu-id="71330-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="71330-111">-ClusterName</span></span>
<span data-ttu-id="71330-112">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="71330-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="71330-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71330-113">-DefaultProfile</span></span>
<span data-ttu-id="71330-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="71330-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71330-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="71330-115">-HttpCredential</span></span>
<span data-ttu-id="71330-116">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="71330-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71330-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71330-117">-ResourceGroupName</span></span>
<span data-ttu-id="71330-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="71330-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="71330-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71330-119">CommonParameters</span></span>
<span data-ttu-id="71330-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71330-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71330-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71330-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71330-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71330-122">INPUTS</span></span>

### <span data-ttu-id="71330-123">Keine</span><span class="sxs-lookup"><span data-stu-id="71330-123">None</span></span>

## <span data-ttu-id="71330-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71330-124">OUTPUTS</span></span>

### <span data-ttu-id="71330-125">System.String</span><span class="sxs-lookup"><span data-stu-id="71330-125">System.String</span></span>

## <span data-ttu-id="71330-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71330-126">NOTES</span></span>

## <span data-ttu-id="71330-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71330-127">RELATED LINKS</span></span>

[<span data-ttu-id="71330-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="71330-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="71330-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="71330-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


