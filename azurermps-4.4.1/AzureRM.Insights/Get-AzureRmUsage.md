---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501846"
---
# <span data-ttu-id="50fec-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="50fec-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="50fec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50fec-102">SYNOPSIS</span></span>
<span data-ttu-id="50fec-103">Ruft die Verwendungs Metriken für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="50fec-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50fec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50fec-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50fec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50fec-105">DESCRIPTION</span></span>
<span data-ttu-id="50fec-106">Das Cmdlet " **Get-AzureRmUsage** " Ruft die Verwendungs Metriken für eine angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="50fec-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="50fec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50fec-107">EXAMPLES</span></span>

### <span data-ttu-id="50fec-108">Beispiel 1: Abrufen von Verwendungs Metriken nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="50fec-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="50fec-109">Dieser Befehl ruft die Verwendungs Metriken für die angegebene Website ab.</span><span class="sxs-lookup"><span data-stu-id="50fec-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="50fec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="50fec-110">PARAMETERS</span></span>

### <span data-ttu-id="50fec-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50fec-111">-ApiVersion</span></span>
<span data-ttu-id="50fec-112">Gibt eine API-Versionszeichenfolge an, beispielsweise 2014-04-01, die vom Ressourcenanbieter akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="50fec-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fec-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="50fec-113">-EndTime</span></span>
<span data-ttu-id="50fec-114">Gibt die aktuelle Uhrzeit und das Datum für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="50fec-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="50fec-115">Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50fec-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fec-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="50fec-116">-MetricNames</span></span>
<span data-ttu-id="50fec-117">Gibt ein Array mit Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="50fec-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fec-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="50fec-118">-ResourceId</span></span>
<span data-ttu-id="50fec-119">Gibt die ID der Ressource für die Metrik an.</span><span class="sxs-lookup"><span data-stu-id="50fec-119">Specifies the ID of the resource for the metric.</span></span>

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

### <span data-ttu-id="50fec-120">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="50fec-120">-StartTime</span></span>
<span data-ttu-id="50fec-121">Gibt die früheste Uhrzeit und das Datum an, zu dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="50fec-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="50fec-122">Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50fec-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fec-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fec-123">-DefaultProfile</span></span>
<span data-ttu-id="50fec-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50fec-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50fec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fec-125">CommonParameters</span></span>
<span data-ttu-id="50fec-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fec-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50fec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fec-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50fec-128">INPUTS</span></span>

## <span data-ttu-id="50fec-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50fec-129">OUTPUTS</span></span>

### <span data-ttu-id="50fec-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="50fec-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="50fec-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="50fec-131">NOTES</span></span>

## <span data-ttu-id="50fec-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50fec-132">RELATED LINKS</span></span>

[<span data-ttu-id="50fec-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="50fec-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


