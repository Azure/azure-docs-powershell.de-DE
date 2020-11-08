---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995098"
---
# <span data-ttu-id="e3b77-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="e3b77-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="e3b77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3b77-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b77-103">Erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3b77-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="e3b77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3b77-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3b77-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3b77-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b77-106">Das Cmdlet **New-AzMetricFilter** erstellt einen metrischen Dimensionsfilter, der zum Abfragen von Metriken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3b77-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="e3b77-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3b77-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b77-108">Beispiel 1: Erstellen eines metrischen Bemaßungs Filters</span><span class="sxs-lookup"><span data-stu-id="e3b77-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="e3b77-109">Mit diesem Befehl wird der metrische Dimensionsfilter des Formats "City EQ ' Seattle" oder "City EQ ' New York" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3b77-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="e3b77-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3b77-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b77-111">-DefaultProfile</span></span>
<span data-ttu-id="e3b77-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3b77-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b77-113">-Bemaßung</span><span class="sxs-lookup"><span data-stu-id="e3b77-113">-Dimension</span></span>
<span data-ttu-id="e3b77-114">Der Name der metrischen Dimension.</span><span class="sxs-lookup"><span data-stu-id="e3b77-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="e3b77-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="e3b77-115">-Operator</span></span>
<span data-ttu-id="e3b77-116">Gibt den Operator an, der zum Auswählen der metrischen Bemaßung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3b77-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="e3b77-117">-Wert</span><span class="sxs-lookup"><span data-stu-id="e3b77-117">-Value</span></span>
<span data-ttu-id="e3b77-118">Gibt das Array von metrischen Bemaßungswerten an.</span><span class="sxs-lookup"><span data-stu-id="e3b77-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="e3b77-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b77-119">CommonParameters</span></span>
<span data-ttu-id="e3b77-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b77-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b77-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3b77-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b77-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3b77-122">INPUTS</span></span>

### <span data-ttu-id="e3b77-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b77-123">System.String</span></span>

### <span data-ttu-id="e3b77-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="e3b77-124">System.String[]</span></span>

## <span data-ttu-id="e3b77-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3b77-125">OUTPUTS</span></span>

### <span data-ttu-id="e3b77-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b77-126">System.String</span></span>

## <span data-ttu-id="e3b77-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3b77-127">NOTES</span></span>

## <span data-ttu-id="e3b77-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3b77-128">RELATED LINKS</span></span>

<span data-ttu-id="e3b77-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="e3b77-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

