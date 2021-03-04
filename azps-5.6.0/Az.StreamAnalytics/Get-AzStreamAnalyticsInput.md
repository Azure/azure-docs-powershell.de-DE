---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 726d9d9294c4cf6e5789399ec821d4657e6f787e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929552"
---
# <span data-ttu-id="f1131-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1131-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="f1131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1131-102">SYNOPSIS</span></span>
<span data-ttu-id="f1131-103">Ruft Stream Analytics-Auftragseingaben ab.</span><span class="sxs-lookup"><span data-stu-id="f1131-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="f1131-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1131-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1131-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1131-105">DESCRIPTION</span></span>
<span data-ttu-id="f1131-106">Das **Get-AzStreamAnalyticsInput-Cmdlet** listet alle Eingaben auf, die in einem Stream Analytics-Auftrag definiert sind oder Informationen zu einer bestimmten Eingabe erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1131-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="f1131-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1131-107">EXAMPLES</span></span>

### <span data-ttu-id="f1131-108">Beispiel 1: Informationen zu den für einen Auftrag definierten Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1131-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="f1131-109">Dieser Befehl gibt Informationen zu allen Eingaben zurück, die im Auftrag StreamingJob definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f1131-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="f1131-110">Beispiel 2: Erhalten von Informationen zu einer bestimmten Eingabe, die für einen Auftrag definiert wurde</span><span class="sxs-lookup"><span data-stu-id="f1131-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="f1131-111">Dieser Befehl gibt Informationen zur Eingabe mit dem Namen EntryStream zurück, die im Auftrag StreamingJob definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1131-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="f1131-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1131-112">PARAMETERS</span></span>

### <span data-ttu-id="f1131-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1131-113">-DefaultProfile</span></span>
<span data-ttu-id="f1131-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1131-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1131-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="f1131-115">-JobName</span></span>
<span data-ttu-id="f1131-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="f1131-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f1131-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f1131-117">-Name</span></span>
<span data-ttu-id="f1131-118">Gibt den Namen der abzurufenden Azure Stream Analytics-Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="f1131-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="f1131-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1131-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1131-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="f1131-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f1131-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1131-121">CommonParameters</span></span>
<span data-ttu-id="f1131-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1131-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1131-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1131-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1131-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1131-124">INPUTS</span></span>

### <span data-ttu-id="f1131-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f1131-125">System.String</span></span>

## <span data-ttu-id="f1131-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1131-126">OUTPUTS</span></span>

### <span data-ttu-id="f1131-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="f1131-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="f1131-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1131-128">NOTES</span></span>

## <span data-ttu-id="f1131-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1131-129">RELATED LINKS</span></span>

[<span data-ttu-id="f1131-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1131-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="f1131-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1131-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="f1131-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f1131-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


