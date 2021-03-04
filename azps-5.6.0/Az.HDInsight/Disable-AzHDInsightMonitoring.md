---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 04e4a2e45f799367060c76e30807f75eaedb0465
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927112"
---
# <span data-ttu-id="6f781-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="6f781-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="6f781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f781-102">SYNOPSIS</span></span>
<span data-ttu-id="6f781-103">Deaktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle fließen nicht mehr zum Überwachungsarbeitsbereich, der während der Aktivierung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6f781-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="6f781-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f781-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f781-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f781-105">DESCRIPTION</span></span>
<span data-ttu-id="6f781-106">Das **Cmdlet Disable-AzHDInsightMonitoring** deaktiviert die Überwachung in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6f781-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6f781-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f781-107">EXAMPLES</span></span>

### <span data-ttu-id="6f781-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f781-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="6f781-109">Die Überwachung wird im HDInsight-Cluster deaktiviert, und relevante Protokolle fließen nicht mehr zum Überwachungsarbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="6f781-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="6f781-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6f781-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="6f781-111">Die Überwachung wird im HDInsight-Cluster deaktiviert, und relevante Protokolle fließen nicht mehr zum Überwachungsarbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="6f781-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="6f781-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6f781-112">PARAMETERS</span></span>

### <span data-ttu-id="6f781-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f781-113">-DefaultProfile</span></span>
<span data-ttu-id="6f781-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f781-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f781-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6f781-115">-Name</span></span>
<span data-ttu-id="6f781-116">Der Name des Clusters zum Deaktivieren der Überwachung.</span><span class="sxs-lookup"><span data-stu-id="6f781-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="6f781-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f781-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f781-118">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="6f781-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="6f781-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f781-119">-Confirm</span></span>
<span data-ttu-id="6f781-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f781-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f781-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f781-121">-WhatIf</span></span>
<span data-ttu-id="6f781-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f781-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f781-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f781-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f781-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f781-124">CommonParameters</span></span>
<span data-ttu-id="6f781-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f781-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f781-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f781-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f781-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f781-127">INPUTS</span></span>

### <span data-ttu-id="6f781-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6f781-128">System.String</span></span>

## <span data-ttu-id="6f781-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f781-129">OUTPUTS</span></span>

### <span data-ttu-id="6f781-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f781-130">System.Boolean</span></span>

## <span data-ttu-id="6f781-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6f781-131">NOTES</span></span>

## <span data-ttu-id="6f781-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6f781-132">RELATED LINKS</span></span>
