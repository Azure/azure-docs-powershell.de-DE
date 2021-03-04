---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: bdedaee92a187d1086cdcd71948981e93fed508a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936200"
---
# <span data-ttu-id="79036-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="79036-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="79036-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79036-102">SYNOPSIS</span></span>
<span data-ttu-id="79036-103">Startet die spezifischen Hosts des HDInsight-Clusters neu.</span><span class="sxs-lookup"><span data-stu-id="79036-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="79036-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79036-104">SYNTAX</span></span>

### <span data-ttu-id="79036-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79036-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79036-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="79036-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79036-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79036-107">DESCRIPTION</span></span>
<span data-ttu-id="79036-108">Dieses **Cmdlet Restart-AzHDInsightHost** startet die spezifischen Hosts des HDInsight-Clusters neu.</span><span class="sxs-lookup"><span data-stu-id="79036-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="79036-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79036-109">EXAMPLES</span></span>

### <span data-ttu-id="79036-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79036-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="79036-111">Mit diesem Befehl werden zwei Hosts des Clusters neu gestartet: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="79036-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="79036-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79036-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="79036-113">Dieser Befehl zeigt, wie Sie mit dem Cmdlet "Get-AzHDInsightHost" zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="79036-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="79036-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79036-114">PARAMETERS</span></span>

### <span data-ttu-id="79036-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79036-115">-AsJob</span></span>
<span data-ttu-id="79036-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="79036-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79036-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="79036-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="79036-118">Ruft den Namen des Hosts ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="79036-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79036-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="79036-119">-ClusterName</span></span>
<span data-ttu-id="79036-120">Ruft den Namen des Clusters ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="79036-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="79036-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79036-121">-DefaultProfile</span></span>
<span data-ttu-id="79036-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79036-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79036-123">-Name</span><span class="sxs-lookup"><span data-stu-id="79036-123">-Name</span></span>
<span data-ttu-id="79036-124">Ruft den Namen des Hosts ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="79036-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79036-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79036-125">-PassThru</span></span>
<span data-ttu-id="79036-126">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="79036-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="79036-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79036-127">-ResourceGroupName</span></span>
<span data-ttu-id="79036-128">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="79036-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79036-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79036-129">-Confirm</span></span>
<span data-ttu-id="79036-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79036-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79036-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79036-131">-WhatIf</span></span>
<span data-ttu-id="79036-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79036-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79036-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79036-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79036-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79036-134">CommonParameters</span></span>
<span data-ttu-id="79036-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79036-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79036-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79036-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79036-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79036-137">INPUTS</span></span>

### <span data-ttu-id="79036-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="79036-138">System.String[]</span></span>

### <span data-ttu-id="79036-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="79036-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="79036-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79036-140">OUTPUTS</span></span>

### <span data-ttu-id="79036-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79036-141">System.Boolean</span></span>

## <span data-ttu-id="79036-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79036-142">NOTES</span></span>

## <span data-ttu-id="79036-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79036-143">RELATED LINKS</span></span>
