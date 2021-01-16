---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289702"
---
# <span data-ttu-id="a48f8-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a48f8-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="a48f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a48f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a48f8-103">Entfernt die Konfiguration der Automatischskala des HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a48f8-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a48f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a48f8-104">SYNTAX</span></span>

### <span data-ttu-id="a48f8-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a48f8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a48f8-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a48f8-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a48f8-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a48f8-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a48f8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a48f8-108">DESCRIPTION</span></span>
<span data-ttu-id="a48f8-109">Das **Cmdlet "Remove-AzHDInsightClusterAutoscaleConfiguration"** entfernt die Autoskalenkonfiguration des HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a48f8-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a48f8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a48f8-110">EXAMPLES</span></span>

### <span data-ttu-id="a48f8-111">Beispiel 1: Entfernen der Autoskalenkonfiguration des Cluster "HDInsight".</span><span class="sxs-lookup"><span data-stu-id="a48f8-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="a48f8-112">Mit diesem Befehl wird die Konfiguration der Automatischskala des Cluster "HDInsight" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a48f8-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a48f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a48f8-113">PARAMETERS</span></span>

### <span data-ttu-id="a48f8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a48f8-114">-AsJob</span></span>
<span data-ttu-id="a48f8-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a48f8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a48f8-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a48f8-116">-ClusterName</span></span>
<span data-ttu-id="a48f8-117">Ruft den Namen des Cluster ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="a48f8-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48f8-118">-DefaultProfile</span></span>
<span data-ttu-id="a48f8-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a48f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a48f8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a48f8-120">-InputObject</span></span>
<span data-ttu-id="a48f8-121">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="a48f8-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a48f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="a48f8-123">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="a48f8-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a48f8-124">-ResourceId</span></span>
<span data-ttu-id="a48f8-125">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="a48f8-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48f8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a48f8-126">-Confirm</span></span>
<span data-ttu-id="a48f8-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a48f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a48f8-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a48f8-128">-WhatIf</span></span>
<span data-ttu-id="a48f8-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a48f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a48f8-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a48f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a48f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48f8-131">CommonParameters</span></span>
<span data-ttu-id="a48f8-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a48f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48f8-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a48f8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48f8-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a48f8-134">INPUTS</span></span>

### <span data-ttu-id="a48f8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a48f8-135">System.String</span></span>

### <span data-ttu-id="a48f8-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a48f8-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="a48f8-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a48f8-137">OUTPUTS</span></span>

### <span data-ttu-id="a48f8-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a48f8-138">System.Boolean</span></span>

## <span data-ttu-id="a48f8-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a48f8-139">NOTES</span></span>

## <span data-ttu-id="a48f8-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a48f8-140">RELATED LINKS</span></span>

<span data-ttu-id="a48f8-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a48f8-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
