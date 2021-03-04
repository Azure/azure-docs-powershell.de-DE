---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: ad4867bc97f35a6e027d0f944d936da1760d1033
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947179"
---
# <span data-ttu-id="fee87-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fee87-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="fee87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee87-102">SYNOPSIS</span></span>
<span data-ttu-id="fee87-103">Ruft den Status der Überwachung der Installation im Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="fee87-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="fee87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fee87-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fee87-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fee87-105">DESCRIPTION</span></span>
<span data-ttu-id="fee87-106">Das **Get-AzHDInsightMonitoring-Cmdlet** erhält den Status der Überwachung der Installation in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fee87-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="fee87-107">Wenn die Überwachung aktiviert ist, gibt sie auch die Log Analytics-Arbeitsbereichs-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="fee87-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="fee87-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fee87-108">EXAMPLES</span></span>

### <span data-ttu-id="fee87-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fee87-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="fee87-110">Die Überwachung ist für den Cluster aktiviert, da die Eigenschaft ClusterMonitoringEnabled true ist.</span><span class="sxs-lookup"><span data-stu-id="fee87-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="fee87-111">Die Id des Überwachungsarbeitsbereichs, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fee87-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fee87-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fee87-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="fee87-113">Die Überwachung ist für den Cluster aktiviert, da die Eigenschaft ClusterMonitoringEnabled true ist.</span><span class="sxs-lookup"><span data-stu-id="fee87-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="fee87-114">Die Id des Überwachungsarbeitsbereichs, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fee87-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fee87-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fee87-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="fee87-116">Die Überwachung ist für den Cluster deaktiviert, da die Eigenschaft ClusterMonitoringEnabled falsch ist.</span><span class="sxs-lookup"><span data-stu-id="fee87-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="fee87-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="fee87-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="fee87-118">Die Überwachung ist für den Cluster deaktiviert, da die Eigenschaft ClusterMonitoringEnabled falsch ist.</span><span class="sxs-lookup"><span data-stu-id="fee87-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="fee87-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fee87-119">PARAMETERS</span></span>

### <span data-ttu-id="fee87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee87-120">-DefaultProfile</span></span>
<span data-ttu-id="fee87-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fee87-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fee87-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fee87-122">-Name</span></span>
<span data-ttu-id="fee87-123">Der Name des Clusters, um den Status der Überwachung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fee87-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee87-124">-ResourceGroupName</span></span>
<span data-ttu-id="fee87-125">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="fee87-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee87-126">CommonParameters</span></span>
<span data-ttu-id="fee87-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee87-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fee87-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee87-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fee87-129">INPUTS</span></span>

### <span data-ttu-id="fee87-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fee87-130">System.String</span></span>

## <span data-ttu-id="fee87-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fee87-131">OUTPUTS</span></span>

### <span data-ttu-id="fee87-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fee87-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="fee87-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fee87-133">NOTES</span></span>

## <span data-ttu-id="fee87-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fee87-134">RELATED LINKS</span></span>
