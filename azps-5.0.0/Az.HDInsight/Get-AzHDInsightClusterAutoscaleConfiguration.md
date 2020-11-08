---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175581"
---
# <span data-ttu-id="3b1a5-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b1a5-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="3b1a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1a5-103">Ruft die AutoScale-Konfiguration des HDInsight-Clusters ab.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="3b1a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b1a5-104">SYNTAX</span></span>

### <span data-ttu-id="3b1a5-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b1a5-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b1a5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1a5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b1a5-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1a5-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b1a5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b1a5-108">DESCRIPTION</span></span>
<span data-ttu-id="3b1a5-109">Das Cmdlet " **Get-AzHDInsightClusterAutoscaleConfiguration** " Ruft die AutoScale-Konfiguration des HDInsight-Clusters ab.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="3b1a5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b1a5-110">EXAMPLES</span></span>

### <span data-ttu-id="3b1a5-111">Beispiel 1: Abrufen der AutoScale-Konfiguration des HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="3b1a5-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="3b1a5-112">Dieser Befehl ruft die AutoScale-Konfiguration des HDInsight-Clusters ab.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="3b1a5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b1a5-113">PARAMETERS</span></span>

### <span data-ttu-id="3b1a5-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3b1a5-114">-ClusterName</span></span>
<span data-ttu-id="3b1a5-115">Ruft den Namen des Clusters ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-115">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="3b1a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1a5-116">-DefaultProfile</span></span>
<span data-ttu-id="3b1a5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b1a5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b1a5-118">-InputObject</span></span>
<span data-ttu-id="3b1a5-119">Ruft das Eingabeobjekt ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-119">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="3b1a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b1a5-121">Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-121">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="3b1a5-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3b1a5-122">-ResourceId</span></span>
<span data-ttu-id="3b1a5-123">Ruft die Ressourcen-ID ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-123">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="3b1a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1a5-124">CommonParameters</span></span>
<span data-ttu-id="3b1a5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1a5-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b1a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1a5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b1a5-127">INPUTS</span></span>

### <span data-ttu-id="3b1a5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3b1a5-128">System.String</span></span>

### <span data-ttu-id="3b1a5-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3b1a5-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3b1a5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b1a5-130">OUTPUTS</span></span>

### <span data-ttu-id="3b1a5-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="3b1a5-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="3b1a5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b1a5-132">NOTES</span></span>

## <span data-ttu-id="3b1a5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b1a5-133">RELATED LINKS</span></span>

<span data-ttu-id="3b1a5-134">[Neu – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Satz-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b1a5-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
