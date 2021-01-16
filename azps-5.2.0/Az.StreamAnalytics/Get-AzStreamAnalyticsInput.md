---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 1f83eaf8ff358c211dbe8b83cfb99d986e56c1ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366441"
---
# <span data-ttu-id="4b14b-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4b14b-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="4b14b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b14b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b14b-103">Ruft Eingaben für Stream Analytics-Auftragseingaben ab.</span><span class="sxs-lookup"><span data-stu-id="4b14b-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="4b14b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b14b-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b14b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b14b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b14b-106">Im **Cmdlet "Get-AzStreamAnalyticsInput"** werden alle Eingaben aufgeführt, die in einem Stream Analytics-Auftrag definiert sind oder Informationen zu einer bestimmten Eingabe erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b14b-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="4b14b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b14b-107">EXAMPLES</span></span>

### <span data-ttu-id="4b14b-108">Beispiel 1: Erhalten von Informationen zu den für einen Auftrag definierten Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b14b-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="4b14b-109">Dieser Befehl gibt Informationen zu allen Eingaben zurück, die im Auftrag von StreamingJob definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4b14b-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="4b14b-110">Beispiel 2: Erhalten von Informationen zu einer bestimmten, für einen Auftrag definierten Eingabe</span><span class="sxs-lookup"><span data-stu-id="4b14b-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="4b14b-111">Dieser Befehl gibt Informationen über die Eingabe mit dem Namen EntryStream zurück, die im Auftrag von StreamingJob definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4b14b-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="4b14b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b14b-112">PARAMETERS</span></span>

### <span data-ttu-id="4b14b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b14b-113">-DefaultProfile</span></span>
<span data-ttu-id="4b14b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b14b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b14b-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="4b14b-115">-JobName</span></span>
<span data-ttu-id="4b14b-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="4b14b-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4b14b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4b14b-117">-Name</span></span>
<span data-ttu-id="4b14b-118">Gibt den Namen der Azure Stream Analytics-Eingabe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b14b-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b14b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b14b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b14b-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="4b14b-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4b14b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b14b-121">CommonParameters</span></span>
<span data-ttu-id="4b14b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b14b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b14b-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b14b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b14b-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b14b-124">INPUTS</span></span>

### <span data-ttu-id="4b14b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4b14b-125">System.String</span></span>

## <span data-ttu-id="4b14b-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b14b-126">OUTPUTS</span></span>

### <span data-ttu-id="4b14b-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="4b14b-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="4b14b-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b14b-128">NOTES</span></span>

## <span data-ttu-id="4b14b-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b14b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4b14b-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4b14b-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4b14b-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4b14b-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4b14b-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4b14b-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


