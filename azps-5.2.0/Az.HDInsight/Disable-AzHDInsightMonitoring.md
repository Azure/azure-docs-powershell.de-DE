---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362731"
---
# <span data-ttu-id="5f492-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5f492-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="5f492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f492-102">SYNOPSIS</span></span>
<span data-ttu-id="5f492-103">Deaktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle fließen nicht mehr zum Überwachungsarbeitsbereich, der während der Aktivierung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5f492-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="5f492-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f492-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f492-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f492-105">DESCRIPTION</span></span>
<span data-ttu-id="5f492-106">Das **Cmdlet "Disable-AzHDInsightMonitoring"** deaktiviert die Überwachung in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f492-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5f492-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f492-107">EXAMPLES</span></span>

### <span data-ttu-id="5f492-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f492-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="5f492-109">Die Überwachung wird im Cluster "HDInsight" deaktiviert, und relevante Protokolle werden nicht mehr in den Überwachungsarbeitsbereich fließen.</span><span class="sxs-lookup"><span data-stu-id="5f492-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="5f492-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5f492-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="5f492-111">Die Überwachung wird im Cluster "HDInsight" deaktiviert, und relevante Protokolle werden nicht mehr in den Überwachungsarbeitsbereich fließen.</span><span class="sxs-lookup"><span data-stu-id="5f492-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="5f492-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f492-112">PARAMETERS</span></span>

### <span data-ttu-id="5f492-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f492-113">-DefaultProfile</span></span>
<span data-ttu-id="5f492-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5f492-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f492-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5f492-115">-Name</span></span>
<span data-ttu-id="5f492-116">Der Name des Clusters, um die Überwachung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f492-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="5f492-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f492-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f492-118">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="5f492-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="5f492-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f492-119">-Confirm</span></span>
<span data-ttu-id="5f492-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f492-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f492-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5f492-121">-WhatIf</span></span>
<span data-ttu-id="5f492-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f492-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f492-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f492-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f492-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f492-124">CommonParameters</span></span>
<span data-ttu-id="5f492-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f492-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f492-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f492-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f492-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f492-127">INPUTS</span></span>

### <span data-ttu-id="5f492-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f492-128">System.String</span></span>

## <span data-ttu-id="5f492-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f492-129">OUTPUTS</span></span>

### <span data-ttu-id="5f492-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5f492-130">System.Boolean</span></span>

## <span data-ttu-id="5f492-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5f492-131">NOTES</span></span>

## <span data-ttu-id="5f492-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5f492-132">RELATED LINKS</span></span>
