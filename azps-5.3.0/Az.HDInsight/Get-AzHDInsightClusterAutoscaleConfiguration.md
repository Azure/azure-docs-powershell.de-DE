---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469695"
---
# <span data-ttu-id="9c186-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c186-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="9c186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c186-102">SYNOPSIS</span></span>
<span data-ttu-id="9c186-103">Ruft die Autoskalenkonfiguration des Cluster "HDInsight" ab.</span><span class="sxs-lookup"><span data-stu-id="9c186-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="9c186-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c186-104">SYNTAX</span></span>

### <span data-ttu-id="9c186-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c186-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c186-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c186-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c186-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c186-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c186-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c186-108">DESCRIPTION</span></span>
<span data-ttu-id="9c186-109">Das **Cmdlet "Get-AzHDInsightClusterAutoscaleConfiguration"** ruft die Autoskalenkonfiguration des Cluster "HDInsight" ab.</span><span class="sxs-lookup"><span data-stu-id="9c186-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="9c186-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9c186-110">EXAMPLES</span></span>

### <span data-ttu-id="9c186-111">Beispiel 1: Holen Sie sich die Konfiguration der Automatischskala des HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="9c186-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="9c186-112">Dieser Befehl ruft die Konfiguration der Automatischskala des Cluster "HDInsight" ab.</span><span class="sxs-lookup"><span data-stu-id="9c186-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="9c186-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c186-113">PARAMETERS</span></span>

### <span data-ttu-id="9c186-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9c186-114">-ClusterName</span></span>
<span data-ttu-id="9c186-115">Ruft den Namen des Cluster ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="9c186-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c186-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c186-116">-DefaultProfile</span></span>
<span data-ttu-id="9c186-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c186-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c186-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c186-118">-InputObject</span></span>
<span data-ttu-id="9c186-119">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="9c186-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c186-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c186-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c186-121">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="9c186-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c186-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c186-122">-ResourceId</span></span>
<span data-ttu-id="9c186-123">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="9c186-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c186-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c186-124">CommonParameters</span></span>
<span data-ttu-id="9c186-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c186-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c186-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c186-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c186-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9c186-127">INPUTS</span></span>

### <span data-ttu-id="9c186-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9c186-128">System.String</span></span>

### <span data-ttu-id="9c186-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9c186-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="9c186-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9c186-130">OUTPUTS</span></span>

### <span data-ttu-id="9c186-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="9c186-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="9c186-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9c186-132">NOTES</span></span>

## <span data-ttu-id="9c186-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9c186-133">RELATED LINKS</span></span>

<span data-ttu-id="9c186-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9c186-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
