---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846363"
---
# <span data-ttu-id="630a0-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="630a0-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="630a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="630a0-102">SYNOPSIS</span></span>
<span data-ttu-id="630a0-103">Testet, ob Datenstrom Analyse eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="630a0-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="630a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="630a0-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="630a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="630a0-105">DESCRIPTION</span></span>
<span data-ttu-id="630a0-106">Das Cmdlet **Test-AzStreamAnalyticsFunction** testet, ob Azure Stream Analytics eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="630a0-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="630a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="630a0-107">EXAMPLES</span></span>

### <span data-ttu-id="630a0-108">Beispiel 1: Testen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="630a0-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="630a0-109">Dieser Befehl testet den Verbindungsstatus der Funktion mit dem Namen ScoreTweet im Auftrag mit dem Namen StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="630a0-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="630a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="630a0-110">PARAMETERS</span></span>

### <span data-ttu-id="630a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="630a0-111">-DefaultProfile</span></span>
<span data-ttu-id="630a0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="630a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="630a0-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="630a0-113">-JobName</span></span>
<span data-ttu-id="630a0-114">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="630a0-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="630a0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="630a0-115">-Name</span></span>
<span data-ttu-id="630a0-116">Gibt den Namen der Datenstrom Analysefunktion an, die von diesem Cmdlet getestet wird.</span><span class="sxs-lookup"><span data-stu-id="630a0-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="630a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="630a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="630a0-118">Gibt den Namen der Ressourcengruppe an, zu der eine Datenstrom Analysefunktion gehört.</span><span class="sxs-lookup"><span data-stu-id="630a0-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="630a0-119">Dieses Cmdlet testet eine Funktion in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="630a0-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="630a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630a0-120">CommonParameters</span></span>
<span data-ttu-id="630a0-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630a0-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="630a0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630a0-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="630a0-123">INPUTS</span></span>

### <span data-ttu-id="630a0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="630a0-124">System.String</span></span>

## <span data-ttu-id="630a0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="630a0-125">OUTPUTS</span></span>

### <span data-ttu-id="630a0-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="630a0-126">System.Boolean</span></span>

## <span data-ttu-id="630a0-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="630a0-127">NOTES</span></span>

## <span data-ttu-id="630a0-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="630a0-128">RELATED LINKS</span></span>

[<span data-ttu-id="630a0-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="630a0-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="630a0-130">Neu – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="630a0-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="630a0-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="630a0-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


