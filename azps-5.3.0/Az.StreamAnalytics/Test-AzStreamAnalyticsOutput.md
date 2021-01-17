---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471665"
---
# <span data-ttu-id="d8a9c-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8a9c-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="d8a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a9c-103">Überprüft den Verbindungsstatus einer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="d8a9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8a9c-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a9c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a9c-106">Das **Cmdlet Test-AzStreamAnalyticsOutput** testet die Fähigkeit von Stream Analytics, eine Verbindung mit einer Ausgabe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="d8a9c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a9c-108">Beispiel 1: Testen des Verbindungsstatus einer Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d8a9c-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="d8a9c-109">Dadurch wird der Verbindungsstatus der Ausgabe in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="d8a9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a9c-111">-DefaultProfile</span></span>
<span data-ttu-id="d8a9c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8a9c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d8a9c-113">-JobName</span></span>
<span data-ttu-id="d8a9c-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die gewünschte Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d8a9c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d8a9c-115">-Name</span></span>
<span data-ttu-id="d8a9c-116">Gibt den Namen der zu testden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="d8a9c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a9c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8a9c-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d8a9c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a9c-119">CommonParameters</span></span>
<span data-ttu-id="d8a9c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a9c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a9c-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a9c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a9c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8a9c-122">INPUTS</span></span>

### <span data-ttu-id="d8a9c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d8a9c-123">System.String</span></span>

## <span data-ttu-id="d8a9c-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8a9c-124">OUTPUTS</span></span>

### <span data-ttu-id="d8a9c-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8a9c-125">System.Boolean</span></span>

## <span data-ttu-id="d8a9c-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8a9c-126">NOTES</span></span>

## <span data-ttu-id="d8a9c-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8a9c-127">RELATED LINKS</span></span>

[<span data-ttu-id="d8a9c-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8a9c-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d8a9c-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8a9c-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d8a9c-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8a9c-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


