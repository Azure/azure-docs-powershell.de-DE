---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 28a595b3e63a01439417ed07f6fd47c1cfc40a79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933595"
---
# <span data-ttu-id="79c1a-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="79c1a-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="79c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="79c1a-103">Testet den Verbindungsstatus einer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="79c1a-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="79c1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79c1a-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c1a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="79c1a-106">Das **Test-AzStreamAnalyticsOutput-Cmdlet** testet die Fähigkeit von Stream Analytics, eine Verbindung mit einer Ausgabe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="79c1a-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="79c1a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="79c1a-108">Beispiel 1: Testen des Verbindungsstatus einer Ausgabe</span><span class="sxs-lookup"><span data-stu-id="79c1a-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="79c1a-109">Dadurch wird der Verbindungsstatus der Ausgabeausgabe in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="79c1a-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="79c1a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79c1a-110">PARAMETERS</span></span>

### <span data-ttu-id="79c1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c1a-111">-DefaultProfile</span></span>
<span data-ttu-id="79c1a-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79c1a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c1a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="79c1a-113">-JobName</span></span>
<span data-ttu-id="79c1a-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die gewünschte Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="79c1a-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="79c1a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="79c1a-115">-Name</span></span>
<span data-ttu-id="79c1a-116">Gibt den Namen der zu testenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="79c1a-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="79c1a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c1a-117">-ResourceGroupName</span></span>
<span data-ttu-id="79c1a-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="79c1a-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="79c1a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c1a-119">CommonParameters</span></span>
<span data-ttu-id="79c1a-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c1a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c1a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c1a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c1a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79c1a-122">INPUTS</span></span>

### <span data-ttu-id="79c1a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="79c1a-123">System.String</span></span>

## <span data-ttu-id="79c1a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79c1a-124">OUTPUTS</span></span>

### <span data-ttu-id="79c1a-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79c1a-125">System.Boolean</span></span>

## <span data-ttu-id="79c1a-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79c1a-126">NOTES</span></span>

## <span data-ttu-id="79c1a-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79c1a-127">RELATED LINKS</span></span>

[<span data-ttu-id="79c1a-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="79c1a-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="79c1a-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="79c1a-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="79c1a-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="79c1a-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


