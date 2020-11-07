---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 5fbc34f3a5a2a7b87c0e7319c5d6243e1207dc61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662814"
---
# <span data-ttu-id="b971e-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="b971e-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="b971e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b971e-102">SYNOPSIS</span></span>
<span data-ttu-id="b971e-103">Ruft den Status der Operation Management Suite (OMS)-Installation auf dem Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="b971e-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b971e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b971e-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b971e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b971e-105">DESCRIPTION</span></span>
<span data-ttu-id="b971e-106">Das Cmdlet " **Get-AzureRmHDInsightOperationsManagementSuite** " Ruft den Status der OMS-Installation in einem Azure HDInsight-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="b971e-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="b971e-107">Wenn OMS aktiviert ist, gibt es auch die OMS-Arbeitsbereichs-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="b971e-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="b971e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b971e-108">EXAMPLES</span></span>

### <span data-ttu-id="b971e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b971e-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="b971e-110">Die Operations Management Suite (OMS) ist im Cluster aktiviert, da die ClusterMonitoringEnabled-Eigenschaft true ist.</span><span class="sxs-lookup"><span data-stu-id="b971e-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="b971e-111">Die OMS-Arbeitsbereichs-ID, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="b971e-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="b971e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b971e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="b971e-113">Die Operations Management Suite (OMS) ist im Cluster aktiviert, da die ClusterMonitoringEnabled-Eigenschaft true ist.</span><span class="sxs-lookup"><span data-stu-id="b971e-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="b971e-114">Die OMS-Arbeitsbereichs-ID, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="b971e-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="b971e-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b971e-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="b971e-116">Die Operations Management Suite (OMS) ist auf dem Cluster deaktiviert, da die ClusterMonitoringEnabled-Eigenschaft false ist.</span><span class="sxs-lookup"><span data-stu-id="b971e-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="b971e-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="b971e-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="b971e-118">Die Operations Management Suite (OMS) ist auf dem Cluster deaktiviert, da die ClusterMonitoringEnabled-Eigenschaft false ist.</span><span class="sxs-lookup"><span data-stu-id="b971e-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="b971e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b971e-119">PARAMETERS</span></span>

### <span data-ttu-id="b971e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b971e-120">-DefaultProfile</span></span>
<span data-ttu-id="b971e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b971e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b971e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b971e-122">-Name</span></span>
<span data-ttu-id="b971e-123">Der Name des Clusters, in dem der Status von Operations Management Suite (OMS) abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b971e-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b971e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b971e-124">-ResourceGroupName</span></span>
<span data-ttu-id="b971e-125">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="b971e-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="b971e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b971e-126">CommonParameters</span></span>
<span data-ttu-id="b971e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b971e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b971e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b971e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b971e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b971e-129">INPUTS</span></span>

### <span data-ttu-id="b971e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b971e-130">System.String</span></span>

## <span data-ttu-id="b971e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b971e-131">OUTPUTS</span></span>

### <span data-ttu-id="b971e-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b971e-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="b971e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b971e-133">NOTES</span></span>

## <span data-ttu-id="b971e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b971e-134">RELATED LINKS</span></span>
