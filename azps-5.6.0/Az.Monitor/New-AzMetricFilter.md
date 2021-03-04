---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: a7fdb0824d464f1704f46a8e8fe19705b2b160fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949067"
---
# <span data-ttu-id="d9c3f-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="d9c3f-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="d9c3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c3f-103">Erstellt einen Metrikdimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="d9c3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9c3f-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9c3f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9c3f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c3f-106">Das **Cmdlet New-AzMetricFilter** erstellt einen Metrikdimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="d9c3f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9c3f-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c3f-108">Beispiel 1: Erstellen eines Metrikdimensionsfilters</span><span class="sxs-lookup"><span data-stu-id="d9c3f-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="d9c3f-109">Mit diesem Befehl wird ein Metrikdimensionsfilter im Format "City eq 'Seattle' oder City eq 'New York'" erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="d9c3f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9c3f-110">PARAMETERS</span></span>

### <span data-ttu-id="d9c3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c3f-111">-DefaultProfile</span></span>
<span data-ttu-id="d9c3f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c3f-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="d9c3f-113">-Dimension</span></span>
<span data-ttu-id="d9c3f-114">Der Name der Metrikdimension.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="d9c3f-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="d9c3f-115">-Operator</span></span>
<span data-ttu-id="d9c3f-116">Gibt den Operator an, der zum Auswählen der Metrikdimension verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="d9c3f-117">-Wert</span><span class="sxs-lookup"><span data-stu-id="d9c3f-117">-Value</span></span>
<span data-ttu-id="d9c3f-118">Gibt das Array der Metrikdimensionswerte an.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="d9c3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c3f-119">CommonParameters</span></span>
<span data-ttu-id="d9c3f-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c3f-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9c3f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c3f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9c3f-122">INPUTS</span></span>

### <span data-ttu-id="d9c3f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d9c3f-123">System.String</span></span>

### <span data-ttu-id="d9c3f-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d9c3f-124">System.String[]</span></span>

## <span data-ttu-id="d9c3f-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9c3f-125">OUTPUTS</span></span>

### <span data-ttu-id="d9c3f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d9c3f-126">System.String</span></span>

## <span data-ttu-id="d9c3f-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d9c3f-127">NOTES</span></span>

## <span data-ttu-id="d9c3f-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d9c3f-128">RELATED LINKS</span></span>

<span data-ttu-id="d9c3f-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="d9c3f-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

