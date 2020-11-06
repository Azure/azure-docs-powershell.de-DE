---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 724441a09ec2714048ec43b781f5792903bce73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478161"
---
# <span data-ttu-id="eb15d-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eb15d-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="eb15d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb15d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb15d-103">Ruft Datenstrom Analyse-Auftrags Eingaben ab.</span><span class="sxs-lookup"><span data-stu-id="eb15d-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb15d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb15d-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb15d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb15d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb15d-106">Das Cmdlet " **Get-AzureRmStreamAnalyticsInput** " listet alle Eingaben auf, die in einem Datenstrom Analyse Auftrag definiert sind, oder ruft Informationen zu einer bestimmten Eingabe ab.</span><span class="sxs-lookup"><span data-stu-id="eb15d-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="eb15d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb15d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb15d-108">Beispiel 1: Abrufen von Informationen zu den für einen Auftrag definierten Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb15d-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="eb15d-109">Dieser Befehl gibt Informationen zu allen Eingaben zurück, die für den Job-StreamingJob definiert sind.</span><span class="sxs-lookup"><span data-stu-id="eb15d-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="eb15d-110">Beispiel 2: Abrufen von Informationen zu einer bestimmten Eingabe, die für einen Auftrag definiert ist</span><span class="sxs-lookup"><span data-stu-id="eb15d-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="eb15d-111">Dieser Befehl gibt Informationen zur Eingabe mit dem Namen "EntryStream" zurück, die für den Job-StreamingJob definiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb15d-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="eb15d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb15d-112">PARAMETERS</span></span>

### <span data-ttu-id="eb15d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb15d-113">-DefaultProfile</span></span>
<span data-ttu-id="eb15d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb15d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb15d-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="eb15d-115">-JobName</span></span>
<span data-ttu-id="eb15d-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="eb15d-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb15d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="eb15d-117">-Name</span></span>
<span data-ttu-id="eb15d-118">Gibt den Namen der zu abrufenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="eb15d-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb15d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb15d-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb15d-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="eb15d-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb15d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb15d-121">CommonParameters</span></span>
<span data-ttu-id="eb15d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb15d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb15d-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb15d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb15d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb15d-124">INPUTS</span></span>

### <span data-ttu-id="eb15d-125">Keine</span><span class="sxs-lookup"><span data-stu-id="eb15d-125">None</span></span>
<span data-ttu-id="eb15d-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="eb15d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb15d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb15d-127">OUTPUTS</span></span>

### <span data-ttu-id="eb15d-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="eb15d-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="eb15d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb15d-129">NOTES</span></span>

## <span data-ttu-id="eb15d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb15d-130">RELATED LINKS</span></span>

[<span data-ttu-id="eb15d-131">Neu – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eb15d-131">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="eb15d-132">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eb15d-132">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="eb15d-133">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eb15d-133">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


