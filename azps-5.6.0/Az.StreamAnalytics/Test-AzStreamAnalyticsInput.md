---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 09cf95f6fd7feb17053063952ae7110098353c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944404"
---
# <span data-ttu-id="57b79-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="57b79-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="57b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b79-102">SYNOPSIS</span></span>
<span data-ttu-id="57b79-103">Testet den Verbindungsstatus einer Eingabe.</span><span class="sxs-lookup"><span data-stu-id="57b79-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="57b79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57b79-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57b79-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57b79-105">DESCRIPTION</span></span>
<span data-ttu-id="57b79-106">Das **Cmdlet Test-AzStreamAnalyticsInput** testet die Fähigkeit von Stream Analytics, eine Verbindung mit einer Eingabe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="57b79-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="57b79-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57b79-107">EXAMPLES</span></span>

### <span data-ttu-id="57b79-108">Beispiel 1: Testen des Verbindungsstatus eines Eingabedatenstroms</span><span class="sxs-lookup"><span data-stu-id="57b79-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="57b79-109">Dadurch wird der Verbindungsstatus des Eingabedatenstroms in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="57b79-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="57b79-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="57b79-110">PARAMETERS</span></span>

### <span data-ttu-id="57b79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b79-111">-DefaultProfile</span></span>
<span data-ttu-id="57b79-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57b79-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57b79-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="57b79-113">-JobName</span></span>
<span data-ttu-id="57b79-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="57b79-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="57b79-115">-Name</span><span class="sxs-lookup"><span data-stu-id="57b79-115">-Name</span></span>
<span data-ttu-id="57b79-116">Gibt den Namen der azure stream analytics-Eingabe an, die sie testen soll.</span><span class="sxs-lookup"><span data-stu-id="57b79-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="57b79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b79-117">-ResourceGroupName</span></span>
<span data-ttu-id="57b79-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="57b79-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="57b79-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b79-119">CommonParameters</span></span>
<span data-ttu-id="57b79-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b79-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b79-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57b79-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b79-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57b79-122">INPUTS</span></span>

### <span data-ttu-id="57b79-123">System.String</span><span class="sxs-lookup"><span data-stu-id="57b79-123">System.String</span></span>

## <span data-ttu-id="57b79-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57b79-124">OUTPUTS</span></span>

### <span data-ttu-id="57b79-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57b79-125">System.Boolean</span></span>

## <span data-ttu-id="57b79-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="57b79-126">NOTES</span></span>

## <span data-ttu-id="57b79-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="57b79-127">RELATED LINKS</span></span>

[<span data-ttu-id="57b79-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="57b79-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="57b79-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="57b79-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="57b79-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="57b79-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


