---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458512"
---
# <span data-ttu-id="74603-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="74603-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="74603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74603-102">SYNOPSIS</span></span>
<span data-ttu-id="74603-103">Entfernt den angegebenen Cluster "HDInsight" aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74603-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="74603-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74603-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74603-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74603-105">DESCRIPTION</span></span>
<span data-ttu-id="74603-106">Das **Cmdlet "Remove-AzHDInsightCluster"** entfernt den angegebenen HDInsight-Dienstcluster aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74603-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="74603-107">Durch diesen Vorgang werden auch alle Daten gelöscht, die im Hadoop Distributed File System (HDFS) im Cluster gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="74603-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="74603-108">Im zugeordneten Azure Storage-Konto gespeicherte Daten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="74603-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="74603-109">In externen Metastores gespeicherte Daten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="74603-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="74603-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74603-110">EXAMPLES</span></span>

### <span data-ttu-id="74603-111">Beispiel 1: Löschen eines Azure -HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="74603-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="74603-112">Mit diesem Befehl wird der Cluster namens "ihr-hadoop-001" entfernt.</span><span class="sxs-lookup"><span data-stu-id="74603-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="74603-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74603-113">PARAMETERS</span></span>

### <span data-ttu-id="74603-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="74603-114">-ClusterName</span></span>
<span data-ttu-id="74603-115">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="74603-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="74603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74603-116">-DefaultProfile</span></span>
<span data-ttu-id="74603-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="74603-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74603-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74603-118">-PassThru</span></span>
<span data-ttu-id="74603-119">Wenn "PassThru" vorhanden ist, geben Sie das Ergebnis aus.</span><span class="sxs-lookup"><span data-stu-id="74603-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74603-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74603-120">-ResourceGroupName</span></span>
<span data-ttu-id="74603-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="74603-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="74603-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74603-122">CommonParameters</span></span>
<span data-ttu-id="74603-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74603-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74603-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74603-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74603-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74603-125">INPUTS</span></span>

### <span data-ttu-id="74603-126">Keine</span><span class="sxs-lookup"><span data-stu-id="74603-126">None</span></span>
## <span data-ttu-id="74603-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74603-127">OUTPUTS</span></span>

### <span data-ttu-id="74603-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74603-128">System.Boolean</span></span>
## <span data-ttu-id="74603-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74603-129">NOTES</span></span>

## <span data-ttu-id="74603-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74603-130">RELATED LINKS</span></span>

[<span data-ttu-id="74603-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="74603-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="74603-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="74603-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


