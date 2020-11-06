---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: c62d829da193ae36f10a64149260cf34c6bc20ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502814"
---
# <span data-ttu-id="a45c8-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a45c8-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="a45c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a45c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a45c8-103">Testet, ob Datenstrom Analyse eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a45c8-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a45c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a45c8-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a45c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a45c8-105">DESCRIPTION</span></span>
<span data-ttu-id="a45c8-106">Das Cmdlet **Test-AzureRmStreamAnalyticsFunction** testet, ob Azure Stream Analytics eine Verbindung mit einer Funktion herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a45c8-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="a45c8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a45c8-107">EXAMPLES</span></span>

### <span data-ttu-id="a45c8-108">Beispiel 1: Testen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="a45c8-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="a45c8-109">Dieser Befehl testet den Verbindungsstatus der Funktion mit dem Namen ScoreTweet im Auftrag mit dem Namen StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="a45c8-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="a45c8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a45c8-110">PARAMETERS</span></span>

### <span data-ttu-id="a45c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45c8-111">-DefaultProfile</span></span>
<span data-ttu-id="a45c8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a45c8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a45c8-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="a45c8-113">-JobName</span></span>
<span data-ttu-id="a45c8-114">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="a45c8-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="a45c8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a45c8-115">-Name</span></span>
<span data-ttu-id="a45c8-116">Gibt den Namen der Datenstrom Analysefunktion an, die von diesem Cmdlet getestet wird.</span><span class="sxs-lookup"><span data-stu-id="a45c8-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="a45c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a45c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a45c8-118">Gibt den Namen der Ressourcengruppe an, zu der eine Datenstrom Analysefunktion gehört.</span><span class="sxs-lookup"><span data-stu-id="a45c8-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="a45c8-119">Dieses Cmdlet testet eine Funktion in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a45c8-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a45c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45c8-120">CommonParameters</span></span>
<span data-ttu-id="a45c8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a45c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45c8-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a45c8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45c8-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a45c8-123">INPUTS</span></span>

### <span data-ttu-id="a45c8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a45c8-124">System.String</span></span>

## <span data-ttu-id="a45c8-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a45c8-125">OUTPUTS</span></span>

### <span data-ttu-id="a45c8-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a45c8-126">System.Boolean</span></span>

## <span data-ttu-id="a45c8-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a45c8-127">NOTES</span></span>

## <span data-ttu-id="a45c8-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a45c8-128">RELATED LINKS</span></span>

[<span data-ttu-id="a45c8-129">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a45c8-129">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a45c8-130">Neu – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a45c8-130">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a45c8-131">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a45c8-131">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


