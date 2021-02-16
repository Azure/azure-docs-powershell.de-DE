---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170574"
---
# <span data-ttu-id="d2ceb-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="d2ceb-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="d2ceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ceb-103">Ruft den Status der Überwachung der Installation für den Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="d2ceb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2ceb-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2ceb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2ceb-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ceb-106">Das **Cmdlet "Get-AzHDInsightMonitoring"** ruft den Status der Überwachung der Installation in einem Azure -HDInsight-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="d2ceb-107">Wenn die Überwachung aktiviert ist, gibt sie auch die Log Analytics Workspace-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="d2ceb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2ceb-108">EXAMPLES</span></span>

### <span data-ttu-id="d2ceb-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2ceb-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="d2ceb-110">Die Überwachung für den Cluster ist aktiviert, da die Eigenschaft "ClusterMonitoringEnabled" wahr ist.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="d2ceb-111">Die Überwachungsarbeitsbereich-ID, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="d2ceb-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d2ceb-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="d2ceb-113">Die Überwachung für den Cluster ist aktiviert, da die Eigenschaft "ClusterMonitoringEnabled" wahr ist.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="d2ceb-114">Die Überwachungsarbeitsbereich-ID, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="d2ceb-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d2ceb-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="d2ceb-116">Die Überwachung für den Cluster ist deaktiviert, da die Eigenschaft "ClusterMonitoringEnabled" "false" ist.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="d2ceb-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d2ceb-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="d2ceb-118">Die Überwachung für den Cluster ist deaktiviert, da die Eigenschaft "ClusterMonitoringEnabled" "false" ist.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="d2ceb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2ceb-119">PARAMETERS</span></span>

### <span data-ttu-id="d2ceb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ceb-120">-DefaultProfile</span></span>
<span data-ttu-id="d2ceb-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d2ceb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ceb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d2ceb-122">-Name</span></span>
<span data-ttu-id="d2ceb-123">Der Name des Clusters, um den Status der Überwachung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="d2ceb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ceb-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2ceb-125">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="d2ceb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ceb-126">CommonParameters</span></span>
<span data-ttu-id="d2ceb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ceb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ceb-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2ceb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ceb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2ceb-129">INPUTS</span></span>

### <span data-ttu-id="d2ceb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d2ceb-130">System.String</span></span>

## <span data-ttu-id="d2ceb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2ceb-131">OUTPUTS</span></span>

### <span data-ttu-id="d2ceb-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="d2ceb-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="d2ceb-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2ceb-133">NOTES</span></span>

## <span data-ttu-id="d2ceb-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2ceb-134">RELATED LINKS</span></span>
