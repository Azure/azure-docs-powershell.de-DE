---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: 479d31afca4bb21fdad10a594917bd8eb51706b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93818908"
---
# <span data-ttu-id="759b6-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="759b6-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="759b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="759b6-102">SYNOPSIS</span></span>
<span data-ttu-id="759b6-103">Erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="759b6-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="759b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="759b6-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="759b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="759b6-105">DESCRIPTION</span></span>
<span data-ttu-id="759b6-106">Das Cmdlet **New-AzMetricFilter** erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="759b6-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="759b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="759b6-107">EXAMPLES</span></span>

### <span data-ttu-id="759b6-108">Beispiel 1: Erstellen eines metrischen Bemaßungs Filters</span><span class="sxs-lookup"><span data-stu-id="759b6-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="759b6-109">Mit diesem Befehl wird der metrische Dimensionsfilter des Formats "City EQ ' Seattle" oder "City EQ ' New York" erstellt.</span><span class="sxs-lookup"><span data-stu-id="759b6-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="759b6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="759b6-110">PARAMETERS</span></span>

### <span data-ttu-id="759b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759b6-111">-DefaultProfile</span></span>
<span data-ttu-id="759b6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="759b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="759b6-113">-Bemaßung</span><span class="sxs-lookup"><span data-stu-id="759b6-113">-Dimension</span></span>
<span data-ttu-id="759b6-114">Der Name der metrischen Dimension.</span><span class="sxs-lookup"><span data-stu-id="759b6-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="759b6-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="759b6-115">-Operator</span></span>
<span data-ttu-id="759b6-116">Gibt den Operator an, der zum Auswählen der metrischen Bemaßung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="759b6-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="759b6-117">-Wert</span><span class="sxs-lookup"><span data-stu-id="759b6-117">-Value</span></span>
<span data-ttu-id="759b6-118">Gibt das Array von metrischen Bemaßungswerten an.</span><span class="sxs-lookup"><span data-stu-id="759b6-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="759b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759b6-119">CommonParameters</span></span>
<span data-ttu-id="759b6-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="759b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759b6-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="759b6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759b6-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="759b6-122">INPUTS</span></span>

### <span data-ttu-id="759b6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="759b6-123">System.String</span></span>

### <span data-ttu-id="759b6-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="759b6-124">System.String[]</span></span>

## <span data-ttu-id="759b6-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="759b6-125">OUTPUTS</span></span>

### <span data-ttu-id="759b6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="759b6-126">System.String</span></span>

## <span data-ttu-id="759b6-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="759b6-127">NOTES</span></span>

## <span data-ttu-id="759b6-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="759b6-128">RELATED LINKS</span></span>

<span data-ttu-id="759b6-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="759b6-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

