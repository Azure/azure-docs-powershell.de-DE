---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 21c4cf10fc6464b3db5bcb999d1f477c2e73840e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662763"
---
# <span data-ttu-id="3f944-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3f944-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="3f944-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f944-102">SYNOPSIS</span></span>
<span data-ttu-id="3f944-103">Ruft die Ausgaben ab, die in einem angegebenen Datenstrom Analyse Auftrag oder einer angegebenen Ausgabe definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3f944-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f944-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f944-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f944-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f944-105">DESCRIPTION</span></span>
<span data-ttu-id="3f944-106">Das Cmdlet " **Get-AzureRmStreamAnalyticsOutput** " listet alle Ausgaben auf, die in einem angegebenen Datenstrom Analyse Auftrag definiert sind, oder ruft Informationen zu einer bestimmten Ausgabe ab.</span><span class="sxs-lookup"><span data-stu-id="3f944-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="3f944-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f944-107">EXAMPLES</span></span>

### <span data-ttu-id="3f944-108">Beispiel 1: Abrufen von Informationen zu Auftrags Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f944-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="3f944-109">Dieser Befehl gibt Informationen zu den für den Job-StreamingJob definierten Ausgaben zurück.</span><span class="sxs-lookup"><span data-stu-id="3f944-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="3f944-110">Beispiel 2: Abrufen von Informationen zu einer bestimmten Auftragsausgabe</span><span class="sxs-lookup"><span data-stu-id="3f944-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="3f944-111">Dieser Befehl gibt Informationen zur Ausgabe mit dem Namen Output zurück, die für den Job-StreamingJob definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f944-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="3f944-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f944-112">PARAMETERS</span></span>

### <span data-ttu-id="3f944-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="3f944-113">-JobName</span></span>
<span data-ttu-id="3f944-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="3f944-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="3f944-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3f944-115">-Name</span></span>
<span data-ttu-id="3f944-116">Gibt den Namen der auszurufenden Azure-Stream-Analyseausgabe an.</span><span class="sxs-lookup"><span data-stu-id="3f944-116">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="3f944-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f944-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f944-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="3f944-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="3f944-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f944-119">-DefaultProfile</span></span>
<span data-ttu-id="3f944-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f944-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f944-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f944-121">CommonParameters</span></span>
<span data-ttu-id="3f944-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f944-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f944-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f944-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f944-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f944-124">INPUTS</span></span>

## <span data-ttu-id="3f944-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f944-125">OUTPUTS</span></span>

### <span data-ttu-id="3f944-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="3f944-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="3f944-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f944-127">NOTES</span></span>

## <span data-ttu-id="3f944-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f944-128">RELATED LINKS</span></span>

[<span data-ttu-id="3f944-129">Neu – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3f944-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="3f944-130">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3f944-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="3f944-131">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3f944-131">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


