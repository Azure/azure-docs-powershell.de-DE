---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173289"
---
# <span data-ttu-id="95eb8-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="95eb8-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="95eb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="95eb8-103">Ruft die Autoskalenkonfiguration des Cluster "HDInsight" ab.</span><span class="sxs-lookup"><span data-stu-id="95eb8-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="95eb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95eb8-104">SYNTAX</span></span>

### <span data-ttu-id="95eb8-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95eb8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95eb8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95eb8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95eb8-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95eb8-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95eb8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95eb8-108">DESCRIPTION</span></span>
<span data-ttu-id="95eb8-109">Das **Cmdlet "Get-AzHDInsightClusterAutoscaleConfiguration"** ruft die Autoskalenkonfiguration des Cluster "HDInsight" ab.</span><span class="sxs-lookup"><span data-stu-id="95eb8-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="95eb8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95eb8-110">EXAMPLES</span></span>

### <span data-ttu-id="95eb8-111">Beispiel 1: Holen Sie sich die Konfiguration der Automatischskala des HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="95eb8-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="95eb8-112">Dieser Befehl ruft die Konfiguration der Automatischskala des Cluster "HDInsight" ab.</span><span class="sxs-lookup"><span data-stu-id="95eb8-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="95eb8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95eb8-113">PARAMETERS</span></span>

### <span data-ttu-id="95eb8-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="95eb8-114">-ClusterName</span></span>
<span data-ttu-id="95eb8-115">Ruft den Namen des Cluster ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="95eb8-115">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="95eb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95eb8-116">-DefaultProfile</span></span>
<span data-ttu-id="95eb8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95eb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95eb8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95eb8-118">-InputObject</span></span>
<span data-ttu-id="95eb8-119">Ruft das Eingabeobjekt ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="95eb8-119">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="95eb8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95eb8-120">-ResourceGroupName</span></span>
<span data-ttu-id="95eb8-121">Ruft den Namen der Ressourcengruppe ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="95eb8-121">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="95eb8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95eb8-122">-ResourceId</span></span>
<span data-ttu-id="95eb8-123">Ruft die Ressourcen-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="95eb8-123">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="95eb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95eb8-124">CommonParameters</span></span>
<span data-ttu-id="95eb8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95eb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95eb8-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95eb8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95eb8-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95eb8-127">INPUTS</span></span>

### <span data-ttu-id="95eb8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="95eb8-128">System.String</span></span>

### <span data-ttu-id="95eb8-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="95eb8-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="95eb8-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95eb8-130">OUTPUTS</span></span>

### <span data-ttu-id="95eb8-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="95eb8-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="95eb8-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95eb8-132">NOTES</span></span>

## <span data-ttu-id="95eb8-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95eb8-133">RELATED LINKS</span></span>

<span data-ttu-id="95eb8-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95eb8-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
