---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: d4b184dfbf834822110369e40fbbfb4eb168e424
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009837"
---
# <span data-ttu-id="79c83-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="79c83-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="79c83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79c83-102">SYNOPSIS</span></span>
<span data-ttu-id="79c83-103">Startet die einzelnen Hosts des HDInsight-Clusters neu.</span><span class="sxs-lookup"><span data-stu-id="79c83-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="79c83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c83-104">SYNTAX</span></span>

### <span data-ttu-id="79c83-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79c83-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [[-DefaultProfile] <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c83-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="79c83-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [[-DefaultProfile] <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c83-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79c83-107">DESCRIPTION</span></span>
<span data-ttu-id="79c83-108">Mit diesem Cmdlet " **Restart-AzHDInsightHost** " werden die speziellen Hosts des HDInsight-Clusters neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="79c83-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="79c83-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79c83-109">EXAMPLES</span></span>

### <span data-ttu-id="79c83-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79c83-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="79c83-111">Mit diesem Befehl werden zwei Hosts des Clusters neu gestartet: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="79c83-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="79c83-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79c83-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="79c83-113">Dieser Befehl zeigt, wie Sie mit dem Cmdlet "Get-AzHDInsightHost" zusammenarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="79c83-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="79c83-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c83-114">PARAMETERS</span></span>

### <span data-ttu-id="79c83-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79c83-115">-AsJob</span></span>
<span data-ttu-id="79c83-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="79c83-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79c83-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="79c83-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="79c83-118">Ruft den Namen des Hosts ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="79c83-118">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="79c83-119">-Clustername</span><span class="sxs-lookup"><span data-stu-id="79c83-119">-ClusterName</span></span>
<span data-ttu-id="79c83-120">Ruft den Namen des Clusters ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="79c83-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="79c83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c83-121">-DefaultProfile</span></span>
<span data-ttu-id="79c83-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79c83-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c83-123">-Name</span><span class="sxs-lookup"><span data-stu-id="79c83-123">-Name</span></span>
<span data-ttu-id="79c83-124">Ruft den Namen des Hosts ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="79c83-124">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="79c83-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79c83-125">-PassThru</span></span>
<span data-ttu-id="79c83-126">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="79c83-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="79c83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c83-127">-ResourceGroupName</span></span>
<span data-ttu-id="79c83-128">Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="79c83-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="79c83-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79c83-129">-Confirm</span></span>
<span data-ttu-id="79c83-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79c83-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c83-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c83-131">-WhatIf</span></span>
<span data-ttu-id="79c83-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79c83-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c83-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79c83-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c83-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c83-134">CommonParameters</span></span>
<span data-ttu-id="79c83-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c83-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c83-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79c83-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c83-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79c83-137">INPUTS</span></span>

### <span data-ttu-id="79c83-138">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightHostInfo, Microsoft. Azure. PowerShell. Cmdlets. HDInsight, Version = 3.2.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="79c83-138">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo, Microsoft.Azure.PowerShell.Cmdlets.HDInsight, Version=3.2.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="79c83-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79c83-139">OUTPUTS</span></span>

### <span data-ttu-id="79c83-140">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="79c83-140">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="79c83-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="79c83-141">NOTES</span></span>

## <span data-ttu-id="79c83-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79c83-142">RELATED LINKS</span></span>
