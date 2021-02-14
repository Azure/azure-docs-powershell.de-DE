---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157345"
---
# <span data-ttu-id="c7d17-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="c7d17-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="c7d17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d17-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d17-103">Erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7d17-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="c7d17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7d17-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d17-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7d17-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d17-106">Das **Cmdlet "New-AzMetricFilter"** erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7d17-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="c7d17-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7d17-107">EXAMPLES</span></span>

### <span data-ttu-id="c7d17-108">Beispiel 1: Erstellen eines metrischen Dimensionsfilters</span><span class="sxs-lookup"><span data-stu-id="c7d17-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="c7d17-109">Mit diesem Befehl wird ein metrischer Dimensionsfilter im Format "Stadt eq 'Seattle' oder City eq 'New York'" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7d17-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="c7d17-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7d17-110">PARAMETERS</span></span>

### <span data-ttu-id="c7d17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d17-111">-DefaultProfile</span></span>
<span data-ttu-id="c7d17-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7d17-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7d17-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="c7d17-113">-Dimension</span></span>
<span data-ttu-id="c7d17-114">Der Name der metrischen Dimension.</span><span class="sxs-lookup"><span data-stu-id="c7d17-114">The name of the metric dimension.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d17-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="c7d17-115">-Operator</span></span>
<span data-ttu-id="c7d17-116">Gibt den Operator an, mit dem die metrische Dimension ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c7d17-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d17-117">-Value</span><span class="sxs-lookup"><span data-stu-id="c7d17-117">-Value</span></span>
<span data-ttu-id="c7d17-118">Gibt das Array metrischer Dimensionswerte an.</span><span class="sxs-lookup"><span data-stu-id="c7d17-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d17-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d17-119">CommonParameters</span></span>
<span data-ttu-id="c7d17-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d17-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d17-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7d17-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d17-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7d17-122">INPUTS</span></span>

### <span data-ttu-id="c7d17-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c7d17-123">System.String</span></span>

### <span data-ttu-id="c7d17-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c7d17-124">System.String[]</span></span>

## <span data-ttu-id="c7d17-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7d17-125">OUTPUTS</span></span>

### <span data-ttu-id="c7d17-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c7d17-126">System.String</span></span>

## <span data-ttu-id="c7d17-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c7d17-127">NOTES</span></span>

## <span data-ttu-id="c7d17-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c7d17-128">RELATED LINKS</span></span>

<span data-ttu-id="c7d17-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="c7d17-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

