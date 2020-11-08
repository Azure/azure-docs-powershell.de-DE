---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175570"
---
# <span data-ttu-id="ef2a1-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef2a1-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="ef2a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef2a1-103">Erstellt ein nicht beibehaltenes Objekt, das die AutoSkalieren-Konfiguration eines Azure HDInsight-Clusters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ef2a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef2a1-104">SYNTAX</span></span>

### <span data-ttu-id="ef2a1-105">LoadAutoscaleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef2a1-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef2a1-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef2a1-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef2a1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef2a1-107">DESCRIPTION</span></span>
<span data-ttu-id="ef2a1-108">Das Cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** erstellt ein nicht beibehaltenes Objekt, das die AutoSkalieren-Konfiguration eines Azure HDInsight-Clusters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ef2a1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef2a1-109">EXAMPLES</span></span>

### <span data-ttu-id="ef2a1-110">Beispiel 1: Erstellen eines Objekts, das die Auslastungs basierte Konfiguration von AutoScale beschreibt</span><span class="sxs-lookup"><span data-stu-id="ef2a1-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="ef2a1-111">Mit diesem Befehl wird ein Objekt erstellt, das die Auslastungs basierte Konfiguration von AutoScale beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="ef2a1-112">Beispiel 2: Erstellen eines Objekts, das die zeitplanbasierte Konfiguration von AutoScale beschreibt</span><span class="sxs-lookup"><span data-stu-id="ef2a1-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="ef2a1-113">Mit diesem Befehl wird ein Objekt erstellt, das die Plan basierte AutoScale-Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="ef2a1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef2a1-114">PARAMETERS</span></span>

### <span data-ttu-id="ef2a1-115">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="ef2a1-115">-Condition</span></span>
<span data-ttu-id="ef2a1-116">Ruft die Bedingung des zeitplanbasierten AutoScale ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef2a1-117">-DefaultProfile</span></span>
<span data-ttu-id="ef2a1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef2a1-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="ef2a1-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="ef2a1-120">Ruft die maximale workernode-Anzahl der Last basierten autoskala ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2a1-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="ef2a1-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="ef2a1-122">Ruft die minimale workernode-Anzahl der Last basierten autoskala ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2a1-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ef2a1-123">-TimeZone</span></span>
<span data-ttu-id="ef2a1-124">Ruft die Zeitzone der zeitplanbasierten autoskala ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef2a1-125">CommonParameters</span></span>
<span data-ttu-id="ef2a1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef2a1-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef2a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef2a1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef2a1-128">INPUTS</span></span>

### <span data-ttu-id="ef2a1-129">Keine</span><span class="sxs-lookup"><span data-stu-id="ef2a1-129">None</span></span>

## <span data-ttu-id="ef2a1-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef2a1-130">OUTPUTS</span></span>

### <span data-ttu-id="ef2a1-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="ef2a1-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="ef2a1-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef2a1-132">NOTES</span></span>

## <span data-ttu-id="ef2a1-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef2a1-133">RELATED LINKS</span></span>

<span data-ttu-id="ef2a1-134">[Satz-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ef2a1-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
