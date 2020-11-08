---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165437"
---
# <span data-ttu-id="66b6f-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="66b6f-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="66b6f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="66b6f-103">Testet, ob Datenstrom Analyse eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="66b6f-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="66b6f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66b6f-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66b6f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="66b6f-106">Das Cmdlet **Test-AzStreamAnalyticsFunction** testet, ob Azure Stream Analytics eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="66b6f-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="66b6f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66b6f-107">EXAMPLES</span></span>

### <span data-ttu-id="66b6f-108">Beispiel 1: Testen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="66b6f-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="66b6f-109">Dieser Befehl testet den Verbindungsstatus der Funktion mit dem Namen ScoreTweet im Auftrag mit dem Namen StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="66b6f-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="66b6f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66b6f-110">PARAMETERS</span></span>

### <span data-ttu-id="66b6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b6f-111">-DefaultProfile</span></span>
<span data-ttu-id="66b6f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66b6f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b6f-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="66b6f-113">-JobName</span></span>
<span data-ttu-id="66b6f-114">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="66b6f-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="66b6f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="66b6f-115">-Name</span></span>
<span data-ttu-id="66b6f-116">Gibt den Namen der Datenstrom Analysefunktion an, die von diesem Cmdlet getestet wird.</span><span class="sxs-lookup"><span data-stu-id="66b6f-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="66b6f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b6f-117">-ResourceGroupName</span></span>
<span data-ttu-id="66b6f-118">Gibt den Namen der Ressourcengruppe an, zu der eine Datenstrom Analysefunktion gehört.</span><span class="sxs-lookup"><span data-stu-id="66b6f-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="66b6f-119">Dieses Cmdlet testet eine Funktion in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="66b6f-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="66b6f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b6f-120">CommonParameters</span></span>
<span data-ttu-id="66b6f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b6f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b6f-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b6f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b6f-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66b6f-123">INPUTS</span></span>

### <span data-ttu-id="66b6f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="66b6f-124">System.String</span></span>

## <span data-ttu-id="66b6f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66b6f-125">OUTPUTS</span></span>

### <span data-ttu-id="66b6f-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66b6f-126">System.Boolean</span></span>

## <span data-ttu-id="66b6f-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="66b6f-127">NOTES</span></span>

## <span data-ttu-id="66b6f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66b6f-128">RELATED LINKS</span></span>

[<span data-ttu-id="66b6f-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="66b6f-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="66b6f-130">Neu – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="66b6f-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="66b6f-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="66b6f-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


