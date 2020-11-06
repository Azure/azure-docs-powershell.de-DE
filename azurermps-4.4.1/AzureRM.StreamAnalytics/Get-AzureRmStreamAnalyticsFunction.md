---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4a387da5b8f1f4ed9e6f3653a32ff8880ffaa734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483249"
---
# <span data-ttu-id="f9e27-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f9e27-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="f9e27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9e27-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e27-103">Ruft Funktionen in einem Datenstrom Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="f9e27-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9e27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9e27-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9e27-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9e27-105">DESCRIPTION</span></span>
<span data-ttu-id="f9e27-106">Das Cmdlet " **Get-AzureRmStreamAnalyticsFunction** " Ruft eine Liste der Funktionen ab, die in einem Azure Stream-Analyse Auftrag oder Informationen zu einer bestimmten Funktion definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f9e27-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="f9e27-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9e27-107">EXAMPLES</span></span>

### <span data-ttu-id="f9e27-108">Beispiel 1: Abrufen aller Datenstrom Analysefunktionen</span><span class="sxs-lookup"><span data-stu-id="f9e27-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="f9e27-109">Dieser Befehl ruft die Funktionen ab, die für den Auftrag mit dem Namen StreamJob22 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f9e27-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="f9e27-110">Beispiel 2: Abrufen einer bestimmten Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="f9e27-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="f9e27-111">Dieser Befehl ruft Informationen zur Funktion ScoreTweet ab, die für den Auftrag mit dem Namen StreamJob22 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9e27-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="f9e27-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e27-112">PARAMETERS</span></span>

### <span data-ttu-id="f9e27-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="f9e27-113">-JobName</span></span>
<span data-ttu-id="f9e27-114">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="f9e27-114">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="f9e27-115">Dieses Cmdlet ruft Funktionen für den Auftrag ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f9e27-115">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9e27-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f9e27-116">-Name</span></span>
<span data-ttu-id="f9e27-117">Gibt den Namen der Datenstrom Analysefunktion an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f9e27-117">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f9e27-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e27-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9e27-119">Gibt den Namen der Ressourcengruppe an, zu der Datenstrom Analysefunktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="f9e27-119">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="f9e27-120">Dieses Cmdlet ruft Funktionen für die Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f9e27-120">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9e27-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e27-121">-DefaultProfile</span></span>
<span data-ttu-id="f9e27-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9e27-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9e27-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e27-123">CommonParameters</span></span>
<span data-ttu-id="f9e27-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e27-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e27-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9e27-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e27-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9e27-126">INPUTS</span></span>

## <span data-ttu-id="f9e27-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9e27-127">OUTPUTS</span></span>

### <span data-ttu-id="f9e27-128">System. Collections. Generic. List [Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="f9e27-128">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="f9e27-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9e27-129">NOTES</span></span>

## <span data-ttu-id="f9e27-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9e27-130">RELATED LINKS</span></span>

[<span data-ttu-id="f9e27-131">Neu – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f9e27-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="f9e27-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f9e27-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="f9e27-133">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f9e27-133">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


