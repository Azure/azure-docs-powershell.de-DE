---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
ms.openlocfilehash: 42633beddee9e6681e68ce1ba61e71d276abf478
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849324"
---
# <span data-ttu-id="70be0-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="70be0-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="70be0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70be0-102">SYNOPSIS</span></span>
<span data-ttu-id="70be0-103">Erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="70be0-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70be0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70be0-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70be0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70be0-105">DESCRIPTION</span></span>
<span data-ttu-id="70be0-106">Das Cmdlet **New-AzureRmMetricFilter** erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="70be0-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="70be0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70be0-107">EXAMPLES</span></span>

### <span data-ttu-id="70be0-108">Beispiel 1: Erstellen eines metrischen Bemaßungs Filters</span><span class="sxs-lookup"><span data-stu-id="70be0-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="70be0-109">Mit diesem Befehl wird der metrische Dimensionsfilter des Formats "City EQ ' Seattle" oder "City EQ ' New York" erstellt.</span><span class="sxs-lookup"><span data-stu-id="70be0-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="70be0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="70be0-110">PARAMETERS</span></span>

### <span data-ttu-id="70be0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70be0-111">-DefaultProfile</span></span>
<span data-ttu-id="70be0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70be0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be0-113">-Bemaßung</span><span class="sxs-lookup"><span data-stu-id="70be0-113">-Dimension</span></span>
<span data-ttu-id="70be0-114">Der Name der metrischen Dimension.</span><span class="sxs-lookup"><span data-stu-id="70be0-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="70be0-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="70be0-115">-Operator</span></span>
<span data-ttu-id="70be0-116">Gibt den Operator an, der zum Auswählen der metrischen Bemaßung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70be0-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="70be0-117">-Wert</span><span class="sxs-lookup"><span data-stu-id="70be0-117">-Value</span></span>
<span data-ttu-id="70be0-118">Gibt das Array von metrischen Bemaßungswerten an.</span><span class="sxs-lookup"><span data-stu-id="70be0-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="70be0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70be0-119">CommonParameters</span></span>
<span data-ttu-id="70be0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70be0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70be0-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70be0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70be0-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70be0-122">INPUTS</span></span>

### <span data-ttu-id="70be0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="70be0-123">System.String</span></span>

### <span data-ttu-id="70be0-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="70be0-124">System.String[]</span></span>

## <span data-ttu-id="70be0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70be0-125">OUTPUTS</span></span>

### <span data-ttu-id="70be0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="70be0-126">System.String</span></span>

## <span data-ttu-id="70be0-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="70be0-127">NOTES</span></span>

## <span data-ttu-id="70be0-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70be0-128">RELATED LINKS</span></span>

<span data-ttu-id="70be0-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="70be0-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

