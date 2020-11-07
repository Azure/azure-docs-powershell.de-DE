---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: ba64089da3673957eead10ef1301f5c7c4a59467
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847488"
---
# <span data-ttu-id="444f0-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="444f0-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="444f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="444f0-102">SYNOPSIS</span></span>
<span data-ttu-id="444f0-103">Ruft Datenstrom Analyse-Auftrags Eingaben ab.</span><span class="sxs-lookup"><span data-stu-id="444f0-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="444f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="444f0-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="444f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="444f0-105">DESCRIPTION</span></span>
<span data-ttu-id="444f0-106">Das Cmdlet " **Get-AzStreamAnalyticsInput** " listet alle Eingaben auf, die in einem Datenstrom Analyse Auftrag definiert sind, oder ruft Informationen zu einer bestimmten Eingabe ab.</span><span class="sxs-lookup"><span data-stu-id="444f0-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="444f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="444f0-107">EXAMPLES</span></span>

### <span data-ttu-id="444f0-108">Beispiel 1: Abrufen von Informationen zu den für einen Auftrag definierten Eingaben</span><span class="sxs-lookup"><span data-stu-id="444f0-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="444f0-109">Dieser Befehl gibt Informationen zu allen Eingaben zurück, die für den Job-StreamingJob definiert sind.</span><span class="sxs-lookup"><span data-stu-id="444f0-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="444f0-110">Beispiel 2: Abrufen von Informationen zu einer bestimmten Eingabe, die für einen Auftrag definiert ist</span><span class="sxs-lookup"><span data-stu-id="444f0-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="444f0-111">Dieser Befehl gibt Informationen zur Eingabe mit dem Namen "EntryStream" zurück, die für den Job-StreamingJob definiert ist.</span><span class="sxs-lookup"><span data-stu-id="444f0-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="444f0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="444f0-112">PARAMETERS</span></span>

### <span data-ttu-id="444f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444f0-113">-DefaultProfile</span></span>
<span data-ttu-id="444f0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="444f0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="444f0-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="444f0-115">-JobName</span></span>
<span data-ttu-id="444f0-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="444f0-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="444f0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="444f0-117">-Name</span></span>
<span data-ttu-id="444f0-118">Gibt den Namen der zu abrufenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="444f0-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="444f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="444f0-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="444f0-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="444f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444f0-121">CommonParameters</span></span>
<span data-ttu-id="444f0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="444f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444f0-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="444f0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444f0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="444f0-124">INPUTS</span></span>

### <span data-ttu-id="444f0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="444f0-125">System.String</span></span>

## <span data-ttu-id="444f0-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="444f0-126">OUTPUTS</span></span>

### <span data-ttu-id="444f0-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="444f0-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="444f0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="444f0-128">NOTES</span></span>

## <span data-ttu-id="444f0-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="444f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="444f0-130">Neu – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="444f0-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="444f0-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="444f0-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="444f0-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="444f0-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


