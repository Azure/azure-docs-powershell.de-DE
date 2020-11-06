---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 307a07254f61bcbd37127a2a4d15bb41944a3508
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483250"
---
# <span data-ttu-id="54445-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="54445-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="54445-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54445-102">SYNOPSIS</span></span>
<span data-ttu-id="54445-103">Ruft die Standard Definition einer Funktion in der Datenstrom Analyse ab.</span><span class="sxs-lookup"><span data-stu-id="54445-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54445-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54445-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54445-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54445-105">DESCRIPTION</span></span>
<span data-ttu-id="54445-106">Das Cmdlet " **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** " Ruft die Standard Definition einer Funktion in Azure Stream Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="54445-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="54445-107">Sie können die Standard Definition und das New-AzureRmStreamAnalyticsFunction-Cmdlet verwenden, um eine Funktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="54445-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="54445-108">Sie können die Standard Definition ändern, bevor Sie eine Funktion erstellen.</span><span class="sxs-lookup"><span data-stu-id="54445-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="54445-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54445-109">EXAMPLES</span></span>

### <span data-ttu-id="54445-110">Beispiel 1: Abrufen der Standard Definition einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="54445-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="54445-111">Dieser Befehl ruft die Standard Definition der Funktion mit dem Namen ScoreTweet mithilfe der Parameter ab, die in der Datei RetrieveDefaultDefinitionRequest.jsangegeben sind.</span><span class="sxs-lookup"><span data-stu-id="54445-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="54445-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="54445-112">PARAMETERS</span></span>

### <span data-ttu-id="54445-113">-Datei</span><span class="sxs-lookup"><span data-stu-id="54445-113">-File</span></span>
<span data-ttu-id="54445-114">Gibt den Pfad einer JSON-Datei an, die die JSON-Darstellung (JavaScript Object Notation) des Anforderungstexts für die Abruffunktion der Standard Funktions Definitions Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="54445-114">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54445-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="54445-115">-JobName</span></span>
<span data-ttu-id="54445-116">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="54445-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="54445-117">Dieses Cmdlet ruft die Standard Definition für eine Funktion in dem Auftrag ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54445-117">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="54445-118">-Name</span><span class="sxs-lookup"><span data-stu-id="54445-118">-Name</span></span>
<span data-ttu-id="54445-119">Gibt den Namen der Datenstrom Analysefunktion an, für die dieses Cmdlet die Standard Definition abruft.</span><span class="sxs-lookup"><span data-stu-id="54445-119">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54445-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54445-120">-ResourceGroupName</span></span>
<span data-ttu-id="54445-121">Gibt den Namen der Ressourcengruppe an, zu der Datenstrom Analysefunktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="54445-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="54445-122">Dieses Cmdlet ruft eine Funktionsdefinition für die Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54445-122">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="54445-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54445-123">-DefaultProfile</span></span>
<span data-ttu-id="54445-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54445-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54445-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54445-125">CommonParameters</span></span>
<span data-ttu-id="54445-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54445-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54445-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54445-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54445-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54445-128">INPUTS</span></span>

## <span data-ttu-id="54445-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54445-129">OUTPUTS</span></span>

### <span data-ttu-id="54445-130">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="54445-130">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="54445-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="54445-131">NOTES</span></span>

## <span data-ttu-id="54445-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54445-132">RELATED LINKS</span></span>

[<span data-ttu-id="54445-133">Neu – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="54445-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


