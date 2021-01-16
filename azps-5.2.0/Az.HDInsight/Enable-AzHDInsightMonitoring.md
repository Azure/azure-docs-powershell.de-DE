---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291329"
---
# <span data-ttu-id="f6b57-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="f6b57-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="f6b57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b57-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b57-103">Aktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle werden an den Überwachungsarbeitsbereich gesendet, der während der Aktivierung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f6b57-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="f6b57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6b57-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6b57-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6b57-105">DESCRIPTION</span></span>
<span data-ttu-id="f6b57-106">Das **Cmdlet "Enable-AzHDInsightMonitoring"** ermöglicht die Überwachung in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f6b57-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f6b57-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6b57-107">EXAMPLES</span></span>

### <span data-ttu-id="f6b57-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6b57-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="f6b57-109">Die Überwachung wird im Cluster "HDInsight" aktiviert, und relevante Protokolle werden an den Überwachungsarbeitsbereich mit der ID 1d364e89-bb71-4503-aa3d-a23535aea7bd gesendet.</span><span class="sxs-lookup"><span data-stu-id="f6b57-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="f6b57-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f6b57-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="f6b57-111">Die Überwachung wird im Cluster "HDInsight" aktiviert, und relevante Protokolle werden an den Überwachungsarbeitsbereich mit der ID 1d364e89-bb71-4503-aa3d-a23535aea7bd gesendet.</span><span class="sxs-lookup"><span data-stu-id="f6b57-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="f6b57-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6b57-112">PARAMETERS</span></span>

### <span data-ttu-id="f6b57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b57-113">-DefaultProfile</span></span>
<span data-ttu-id="f6b57-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f6b57-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6b57-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f6b57-115">-Name</span></span>
<span data-ttu-id="f6b57-116">Der Name des Clusters, um die Überwachung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f6b57-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="f6b57-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f6b57-117">-PrimaryKey</span></span>
<span data-ttu-id="f6b57-118">Der Primärschlüssel des Überwachungsarbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f6b57-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b57-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b57-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6b57-120">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="f6b57-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="f6b57-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="f6b57-121">-WorkspaceId</span></span>
<span data-ttu-id="f6b57-122">Die ID des Überwachungsarbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f6b57-122">The id of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b57-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6b57-123">-Confirm</span></span>
<span data-ttu-id="f6b57-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6b57-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6b57-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f6b57-125">-WhatIf</span></span>
<span data-ttu-id="f6b57-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6b57-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6b57-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6b57-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6b57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b57-128">CommonParameters</span></span>
<span data-ttu-id="f6b57-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b57-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6b57-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b57-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6b57-131">INPUTS</span></span>

### <span data-ttu-id="f6b57-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f6b57-132">System.String</span></span>

## <span data-ttu-id="f6b57-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6b57-133">OUTPUTS</span></span>

### <span data-ttu-id="f6b57-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6b57-134">System.Boolean</span></span>

## <span data-ttu-id="f6b57-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f6b57-135">NOTES</span></span>

## <span data-ttu-id="f6b57-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f6b57-136">RELATED LINKS</span></span>
