---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150129"
---
# <span data-ttu-id="4a2c0-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4a2c0-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="4a2c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2c0-103">Überprüft den Verbindungsstatus einer Eingabe.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="4a2c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a2c0-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a2c0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="4a2c0-106">Das **Cmdlet "Test-AzStreamAnalyticsInput"** testet die Fähigkeit von Stream Analytics, eine Verbindung mit einer Eingabe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="4a2c0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a2c0-107">EXAMPLES</span></span>

### <span data-ttu-id="4a2c0-108">Beispiel 1: Testen des Verbindungsstatus eines Eingabedatenstroms</span><span class="sxs-lookup"><span data-stu-id="4a2c0-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="4a2c0-109">Dadurch wird der Verbindungsstatus des Eingabedatenstroms in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="4a2c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a2c0-110">PARAMETERS</span></span>

### <span data-ttu-id="4a2c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a2c0-111">-DefaultProfile</span></span>
<span data-ttu-id="4a2c0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a2c0-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="4a2c0-113">-JobName</span></span>
<span data-ttu-id="4a2c0-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4a2c0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4a2c0-115">-Name</span></span>
<span data-ttu-id="4a2c0-116">Gibt den Namen der zu testden Azure Stream Analytics-Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="4a2c0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a2c0-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a2c0-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4a2c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2c0-119">CommonParameters</span></span>
<span data-ttu-id="4a2c0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a2c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2c0-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a2c0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2c0-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a2c0-122">INPUTS</span></span>

### <span data-ttu-id="4a2c0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4a2c0-123">System.String</span></span>

## <span data-ttu-id="4a2c0-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a2c0-124">OUTPUTS</span></span>

### <span data-ttu-id="4a2c0-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a2c0-125">System.Boolean</span></span>

## <span data-ttu-id="4a2c0-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a2c0-126">NOTES</span></span>

## <span data-ttu-id="4a2c0-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a2c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="4a2c0-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4a2c0-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4a2c0-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4a2c0-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4a2c0-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4a2c0-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


