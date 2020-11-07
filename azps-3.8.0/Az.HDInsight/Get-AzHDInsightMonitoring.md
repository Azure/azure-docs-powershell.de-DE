---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847575"
---
# <span data-ttu-id="257a5-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="257a5-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="257a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="257a5-102">SYNOPSIS</span></span>
<span data-ttu-id="257a5-103">Ruft den Status der überwachungsinstallation auf dem Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="257a5-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="257a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="257a5-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="257a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="257a5-105">DESCRIPTION</span></span>
<span data-ttu-id="257a5-106">Das Cmdlet " **Get-AzHDInsightMonitoring** " Ruft den Status der überwachungsinstallation in einem Azure HDInsight-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="257a5-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="257a5-107">Wenn die Überwachung aktiviert ist, gibt Sie auch die Arbeitsbereichs-ID für die Protokollanalyse zurück.</span><span class="sxs-lookup"><span data-stu-id="257a5-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="257a5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="257a5-108">EXAMPLES</span></span>

### <span data-ttu-id="257a5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="257a5-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="257a5-110">Die Überwachung ist auf dem Cluster aktiviert, da die ClusterMonitoringEnabled-Eigenschaft true ist.</span><span class="sxs-lookup"><span data-stu-id="257a5-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="257a5-111">Die ID des Überwachungs Arbeitsbereichs, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="257a5-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="257a5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="257a5-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="257a5-113">Die Überwachung ist auf dem Cluster aktiviert, da die ClusterMonitoringEnabled-Eigenschaft true ist.</span><span class="sxs-lookup"><span data-stu-id="257a5-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="257a5-114">Die ID des Überwachungs Arbeitsbereichs, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="257a5-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="257a5-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="257a5-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="257a5-116">Die Überwachung ist auf dem Cluster deaktiviert, da die ClusterMonitoringEnabled-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="257a5-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="257a5-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="257a5-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="257a5-118">Die Überwachung ist auf dem Cluster deaktiviert, da die ClusterMonitoringEnabled-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="257a5-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="257a5-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="257a5-119">PARAMETERS</span></span>

### <span data-ttu-id="257a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257a5-120">-DefaultProfile</span></span>
<span data-ttu-id="257a5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="257a5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="257a5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="257a5-122">-Name</span></span>
<span data-ttu-id="257a5-123">Der Name des Clusters, um den Status der Überwachung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="257a5-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="257a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="257a5-125">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="257a5-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="257a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257a5-126">CommonParameters</span></span>
<span data-ttu-id="257a5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257a5-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="257a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257a5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="257a5-129">INPUTS</span></span>

### <span data-ttu-id="257a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="257a5-130">System.String</span></span>

## <span data-ttu-id="257a5-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="257a5-131">OUTPUTS</span></span>

### <span data-ttu-id="257a5-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="257a5-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="257a5-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="257a5-133">NOTES</span></span>

## <span data-ttu-id="257a5-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="257a5-134">RELATED LINKS</span></span>
