---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: eb2fbc1bf327bcfe9b7ca72139742d102e5b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841967"
---
# <span data-ttu-id="42de0-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="42de0-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="42de0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42de0-102">SYNOPSIS</span></span>
<span data-ttu-id="42de0-103">Erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="42de0-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="42de0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42de0-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42de0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42de0-105">DESCRIPTION</span></span>
<span data-ttu-id="42de0-106">Das Cmdlet **New-AzMetricFilter** erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="42de0-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="42de0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42de0-107">EXAMPLES</span></span>

### <span data-ttu-id="42de0-108">Beispiel 1: Erstellen eines metrischen Bemaßungs Filters</span><span class="sxs-lookup"><span data-stu-id="42de0-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="42de0-109">Mit diesem Befehl wird der metrische Dimensionsfilter des Formats "City EQ ' Seattle" oder "City EQ ' New York" erstellt.</span><span class="sxs-lookup"><span data-stu-id="42de0-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="42de0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="42de0-110">PARAMETERS</span></span>

### <span data-ttu-id="42de0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42de0-111">-DefaultProfile</span></span>
<span data-ttu-id="42de0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42de0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42de0-113">-Bemaßung</span><span class="sxs-lookup"><span data-stu-id="42de0-113">-Dimension</span></span>
<span data-ttu-id="42de0-114">Der Name der metrischen Dimension.</span><span class="sxs-lookup"><span data-stu-id="42de0-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="42de0-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="42de0-115">-Operator</span></span>
<span data-ttu-id="42de0-116">Gibt den Operator an, der zum Auswählen der metrischen Bemaßung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42de0-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="42de0-117">-Wert</span><span class="sxs-lookup"><span data-stu-id="42de0-117">-Value</span></span>
<span data-ttu-id="42de0-118">Gibt das Array von metrischen Bemaßungswerten an.</span><span class="sxs-lookup"><span data-stu-id="42de0-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="42de0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42de0-119">CommonParameters</span></span>
<span data-ttu-id="42de0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42de0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42de0-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42de0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42de0-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42de0-122">INPUTS</span></span>

### <span data-ttu-id="42de0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="42de0-123">System.String</span></span>

### <span data-ttu-id="42de0-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="42de0-124">System.String[]</span></span>

## <span data-ttu-id="42de0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42de0-125">OUTPUTS</span></span>

### <span data-ttu-id="42de0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="42de0-126">System.String</span></span>

## <span data-ttu-id="42de0-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="42de0-127">NOTES</span></span>

## <span data-ttu-id="42de0-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42de0-128">RELATED LINKS</span></span>

<span data-ttu-id="42de0-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="42de0-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

