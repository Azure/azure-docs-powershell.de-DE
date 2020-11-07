---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 5e34e0b1ba9e9ab24c0cb47de636ceecec9751f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658672"
---
# <span data-ttu-id="81a60-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="81a60-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="81a60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81a60-102">SYNOPSIS</span></span>
<span data-ttu-id="81a60-103">Ruft Funktionen in einem Datenstrom Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="81a60-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="81a60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81a60-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a60-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81a60-105">DESCRIPTION</span></span>
<span data-ttu-id="81a60-106">Das Cmdlet " **Get-AzStreamAnalyticsFunction** " Ruft eine Liste der Funktionen ab, die in einem Azure Stream-Analyse Auftrag oder Informationen zu einer bestimmten Funktion definiert sind.</span><span class="sxs-lookup"><span data-stu-id="81a60-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="81a60-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81a60-107">EXAMPLES</span></span>

### <span data-ttu-id="81a60-108">Beispiel 1: Abrufen aller Datenstrom Analysefunktionen</span><span class="sxs-lookup"><span data-stu-id="81a60-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="81a60-109">Dieser Befehl ruft die Funktionen ab, die für den Auftrag mit dem Namen StreamJob22 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="81a60-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="81a60-110">Beispiel 2: Abrufen einer bestimmten Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="81a60-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="81a60-111">Dieser Befehl ruft Informationen zur Funktion ScoreTweet ab, die für den Auftrag mit dem Namen StreamJob22 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="81a60-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="81a60-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="81a60-112">PARAMETERS</span></span>

### <span data-ttu-id="81a60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a60-113">-DefaultProfile</span></span>
<span data-ttu-id="81a60-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81a60-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a60-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="81a60-115">-JobName</span></span>
<span data-ttu-id="81a60-116">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="81a60-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="81a60-117">Dieses Cmdlet ruft Funktionen für den Auftrag ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="81a60-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="81a60-118">-Name</span><span class="sxs-lookup"><span data-stu-id="81a60-118">-Name</span></span>
<span data-ttu-id="81a60-119">Gibt den Namen der Datenstrom Analysefunktion an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="81a60-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="81a60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a60-120">-ResourceGroupName</span></span>
<span data-ttu-id="81a60-121">Gibt den Namen der Ressourcengruppe an, zu der Datenstrom Analysefunktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="81a60-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="81a60-122">Dieses Cmdlet ruft Funktionen für die Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="81a60-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="81a60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a60-123">CommonParameters</span></span>
<span data-ttu-id="81a60-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a60-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a60-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a60-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81a60-126">INPUTS</span></span>

### <span data-ttu-id="81a60-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81a60-127">System.String</span></span>

## <span data-ttu-id="81a60-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81a60-128">OUTPUTS</span></span>

### <span data-ttu-id="81a60-129">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="81a60-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="81a60-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="81a60-130">NOTES</span></span>

## <span data-ttu-id="81a60-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81a60-131">RELATED LINKS</span></span>

[<span data-ttu-id="81a60-132">Neu – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="81a60-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="81a60-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="81a60-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="81a60-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="81a60-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


