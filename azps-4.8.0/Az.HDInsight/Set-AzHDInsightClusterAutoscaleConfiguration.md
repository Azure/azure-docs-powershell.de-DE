---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172961"
---
# <span data-ttu-id="f6929-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6929-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="f6929-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6929-102">SYNOPSIS</span></span>
<span data-ttu-id="f6929-103">Legt die AutoScale-Konfiguration eines Azure HDInsight-Clusters fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f6929-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6929-104">SYNTAX</span></span>

### <span data-ttu-id="f6929-105">LoadAutoscaleByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6929-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6929-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6929-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6929-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6929-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6929-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6929-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6929-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6929-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6929-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6929-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6929-114">DESCRIPTION</span></span>
<span data-ttu-id="f6929-115">Mit diesem Cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** wird die AutoScale-Konfiguration eines Azure HDInsight-Clusters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6929-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f6929-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6929-116">EXAMPLES</span></span>

### <span data-ttu-id="f6929-117">Beispiel 1: Einrichten der Last basierten Konfiguration des HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="f6929-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="f6929-118">Mit diesem Befehl wird die Last basierte AutoScale-Konfiguration eines Azure HDInsight-Clusters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6929-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="f6929-119">Beispiel 2: Festlegen der zeitplanbasierten autoskala des HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="f6929-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="f6929-120">Mit diesem Befehl wird die Plan basierte AutoScale-Konfiguration des HDInsight-Clusters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6929-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="f6929-121">Beispiel 3: Einrichten der AutoScale-Konfiguration des HDInsight-Clusters basierend auf einem anderen Cluster, der die Konfiguration der AutoScale-Konfiguration eingestellt hat</span><span class="sxs-lookup"><span data-stu-id="f6929-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="f6929-122">Mit diesem Befehl wird die AutoScale-Konfiguration des HDInsight-Clusters basierend auf einem anderen Cluster festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6929-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="f6929-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6929-123">PARAMETERS</span></span>

### <span data-ttu-id="f6929-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6929-124">-AsJob</span></span>
<span data-ttu-id="f6929-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f6929-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6929-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6929-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="f6929-127">Ruft die Konfiguration des AutoScale ab oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="f6929-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-128">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f6929-128">-ClusterName</span></span>
<span data-ttu-id="f6929-129">Ruft den Namen des Clusters ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-130">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="f6929-130">-Condition</span></span>
<span data-ttu-id="f6929-131">Ruft die Bedingung des zeitplanbasierten AutoScale ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6929-132">-DefaultProfile</span></span>
<span data-ttu-id="f6929-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6929-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6929-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f6929-134">-InputObject</span></span>
<span data-ttu-id="f6929-135">Ruft das Eingabeobjekt ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="f6929-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="f6929-137">Ruft die maximale workernode-Anzahl der Last basierten autoskala ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="f6929-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="f6929-139">Ruft die minimale workernode-Anzahl der Last basierten autoskala ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6929-140">-ResourceGroupName</span></span>
<span data-ttu-id="f6929-141">Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f6929-142">-ResourceId</span></span>
<span data-ttu-id="f6929-143">Ruft die Ressourcen-ID ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-144">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="f6929-144">-Schedule</span></span>
<span data-ttu-id="f6929-145">Festlegen von zeitplanbasierten Parametern</span><span class="sxs-lookup"><span data-stu-id="f6929-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="f6929-146">-TimeZone</span></span>
<span data-ttu-id="f6929-147">Ruft die Zeitzone der zeitplanbasierten autoskala ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f6929-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6929-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6929-148">-Confirm</span></span>
<span data-ttu-id="f6929-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6929-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6929-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6929-150">-WhatIf</span></span>
<span data-ttu-id="f6929-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6929-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6929-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6929-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6929-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6929-153">CommonParameters</span></span>
<span data-ttu-id="f6929-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6929-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6929-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6929-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6929-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6929-156">INPUTS</span></span>

### <span data-ttu-id="f6929-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f6929-157">System.String</span></span>

### <span data-ttu-id="f6929-158">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f6929-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f6929-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6929-159">OUTPUTS</span></span>

### <span data-ttu-id="f6929-160">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="f6929-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="f6929-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6929-161">NOTES</span></span>

## <span data-ttu-id="f6929-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6929-162">RELATED LINKS</span></span>

<span data-ttu-id="f6929-163">[Neu – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f6929-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
