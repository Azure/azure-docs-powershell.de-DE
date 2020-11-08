---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009822"
---
# <span data-ttu-id="4ad4c-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4ad4c-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="4ad4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ad4c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad4c-103">Wählt einen Cluster aus, der mit dem Invoke-RmAzureHDInsightHiveJob-Cmdlet verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ad4c-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="4ad4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ad4c-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ad4c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ad4c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad4c-106">Das Cmdlet **use-AzHDInsightCluster** wählt den Azure HDInsight-Cluster für das Invoke-AzHDInsightHiveJob-Cmdlet aus, das zum Übermitteln von Hive-Aufträgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ad4c-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="4ad4c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ad4c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad4c-108">Beispiel 1: Auswählen eines Clusters für die Übermittlung von Hive-Abfragen</span><span class="sxs-lookup"><span data-stu-id="4ad4c-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="4ad4c-109">Mit diesem Befehl wird ein Cluster für die Übermittlung einer Hive-Abfrage ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4ad4c-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="4ad4c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ad4c-110">PARAMETERS</span></span>

### <span data-ttu-id="4ad4c-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4ad4c-111">-ClusterName</span></span>
<span data-ttu-id="4ad4c-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4ad4c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4ad4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad4c-113">-DefaultProfile</span></span>
<span data-ttu-id="4ad4c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4ad4c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ad4c-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4ad4c-115">-HttpCredential</span></span>
<span data-ttu-id="4ad4c-116">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4ad4c-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4ad4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ad4c-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4ad4c-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4ad4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad4c-119">CommonParameters</span></span>
<span data-ttu-id="4ad4c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad4c-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad4c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad4c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ad4c-122">INPUTS</span></span>

### <span data-ttu-id="4ad4c-123">Keine</span><span class="sxs-lookup"><span data-stu-id="4ad4c-123">None</span></span>

## <span data-ttu-id="4ad4c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ad4c-124">OUTPUTS</span></span>

### <span data-ttu-id="4ad4c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4ad4c-125">System.String</span></span>

## <span data-ttu-id="4ad4c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ad4c-126">NOTES</span></span>

## <span data-ttu-id="4ad4c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ad4c-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ad4c-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4ad4c-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="4ad4c-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4ad4c-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


