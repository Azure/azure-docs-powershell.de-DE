---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471669"
---
# <span data-ttu-id="5aaf8-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5aaf8-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="5aaf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aaf8-102">SYNOPSIS</span></span>
<span data-ttu-id="5aaf8-103">Überprüft, ob Stream Analytics eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="5aaf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5aaf8-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5aaf8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5aaf8-105">DESCRIPTION</span></span>
<span data-ttu-id="5aaf8-106">Mit **dem Cmdlet "Test-AzStreamAnalyticsFunction"** wird überprüft, ob Azure Stream Analytics eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="5aaf8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5aaf8-107">EXAMPLES</span></span>

### <span data-ttu-id="5aaf8-108">Beispiel 1: Testen einer Datenstromanalysefunktion</span><span class="sxs-lookup"><span data-stu-id="5aaf8-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="5aaf8-109">Mit diesem Befehl wird der Verbindungsstatus der Funktion "ScoreTweet" im Auftrag "StreamJob22" getestet.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="5aaf8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5aaf8-110">PARAMETERS</span></span>

### <span data-ttu-id="5aaf8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aaf8-111">-DefaultProfile</span></span>
<span data-ttu-id="5aaf8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aaf8-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5aaf8-113">-JobName</span></span>
<span data-ttu-id="5aaf8-114">Gibt den Namen des Datenstromanalyseauftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="5aaf8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5aaf8-115">-Name</span></span>
<span data-ttu-id="5aaf8-116">Gibt den Namen der Stream Analytics-Funktion an, die von diesem Cmdlet getestet wird.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="5aaf8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aaf8-117">-ResourceGroupName</span></span>
<span data-ttu-id="5aaf8-118">Gibt den Namen der Ressourcengruppe an, zu der eine Stream Analytics-Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="5aaf8-119">Dieses Cmdlet testet eine Funktion in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5aaf8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aaf8-120">CommonParameters</span></span>
<span data-ttu-id="5aaf8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aaf8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aaf8-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aaf8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aaf8-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5aaf8-123">INPUTS</span></span>

### <span data-ttu-id="5aaf8-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5aaf8-124">System.String</span></span>

## <span data-ttu-id="5aaf8-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5aaf8-125">OUTPUTS</span></span>

### <span data-ttu-id="5aaf8-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5aaf8-126">System.Boolean</span></span>

## <span data-ttu-id="5aaf8-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5aaf8-127">NOTES</span></span>

## <span data-ttu-id="5aaf8-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5aaf8-128">RELATED LINKS</span></span>

[<span data-ttu-id="5aaf8-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5aaf8-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5aaf8-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5aaf8-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5aaf8-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5aaf8-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


