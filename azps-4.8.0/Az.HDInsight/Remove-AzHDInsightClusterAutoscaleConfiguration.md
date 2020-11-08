---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009264"
---
# <span data-ttu-id="379a4-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="379a4-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="379a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="379a4-102">SYNOPSIS</span></span>
<span data-ttu-id="379a4-103">Entfernt die AutoScale-Konfiguration des HDInsight-Clusters.</span><span class="sxs-lookup"><span data-stu-id="379a4-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="379a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="379a4-104">SYNTAX</span></span>

### <span data-ttu-id="379a4-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="379a4-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379a4-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="379a4-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379a4-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="379a4-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="379a4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="379a4-108">DESCRIPTION</span></span>
<span data-ttu-id="379a4-109">Das Cmdlet **Remove-AzHDInsightClusterAutoscaleConfiguration** entfernt die AutoScale-Konfiguration des HDInsight-Clusters.</span><span class="sxs-lookup"><span data-stu-id="379a4-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="379a4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="379a4-110">EXAMPLES</span></span>

### <span data-ttu-id="379a4-111">Beispiel 1: Entfernen der AutoScale-Konfiguration des HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="379a4-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="379a4-112">Dieser Befehl entfernt die AutoScale-Konfiguration des HDInsight-Clusters.</span><span class="sxs-lookup"><span data-stu-id="379a4-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="379a4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="379a4-113">PARAMETERS</span></span>

### <span data-ttu-id="379a4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="379a4-114">-AsJob</span></span>
<span data-ttu-id="379a4-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="379a4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="379a4-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="379a4-116">-ClusterName</span></span>
<span data-ttu-id="379a4-117">Ruft den Namen des Clusters ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="379a4-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="379a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379a4-118">-DefaultProfile</span></span>
<span data-ttu-id="379a4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="379a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379a4-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="379a4-120">-InputObject</span></span>
<span data-ttu-id="379a4-121">Ruft das Eingabeobjekt ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="379a4-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="379a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="379a4-123">Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="379a4-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="379a4-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="379a4-124">-ResourceId</span></span>
<span data-ttu-id="379a4-125">Ruft die Ressourcen-ID ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="379a4-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="379a4-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="379a4-126">-Confirm</span></span>
<span data-ttu-id="379a4-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="379a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="379a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="379a4-128">-WhatIf</span></span>
<span data-ttu-id="379a4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="379a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="379a4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="379a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="379a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379a4-131">CommonParameters</span></span>
<span data-ttu-id="379a4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379a4-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="379a4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379a4-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="379a4-134">INPUTS</span></span>

### <span data-ttu-id="379a4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="379a4-135">System.String</span></span>

### <span data-ttu-id="379a4-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="379a4-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="379a4-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="379a4-137">OUTPUTS</span></span>

### <span data-ttu-id="379a4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="379a4-138">System.Boolean</span></span>

## <span data-ttu-id="379a4-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="379a4-139">NOTES</span></span>

## <span data-ttu-id="379a4-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="379a4-140">RELATED LINKS</span></span>

<span data-ttu-id="379a4-141">[Neu – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Satz-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="379a4-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
