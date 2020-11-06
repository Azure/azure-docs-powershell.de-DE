---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501317"
---
# <span data-ttu-id="f5095-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f5095-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f5095-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5095-102">SYNOPSIS</span></span>
<span data-ttu-id="f5095-103">Testet den Verbindungsstatus einer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f5095-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5095-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5095-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5095-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5095-105">DESCRIPTION</span></span>
<span data-ttu-id="f5095-106">Das Cmdlet **Test-AzureRmStreamAnalyticsOutput** testet, ob Datenstrom Analyse eine Verbindung mit einer Ausgabe herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f5095-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="f5095-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5095-107">EXAMPLES</span></span>

### <span data-ttu-id="f5095-108">Beispiel 1: Testen des Verbindungsstatus einer Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f5095-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f5095-109">Dadurch wird der Verbindungsstatus der Ausgabe Ausgabe in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="f5095-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="f5095-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5095-110">PARAMETERS</span></span>

### <span data-ttu-id="f5095-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5095-111">-DefaultProfile</span></span>
<span data-ttu-id="f5095-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5095-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5095-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="f5095-113">-JobName</span></span>
<span data-ttu-id="f5095-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die gewünschte Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="f5095-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5095-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f5095-115">-Name</span></span>
<span data-ttu-id="f5095-116">Gibt den Namen der zu testenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="f5095-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5095-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5095-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5095-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="f5095-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5095-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5095-119">CommonParameters</span></span>
<span data-ttu-id="f5095-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5095-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5095-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5095-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5095-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5095-122">INPUTS</span></span>

### <span data-ttu-id="f5095-123">Keine</span><span class="sxs-lookup"><span data-stu-id="f5095-123">None</span></span>
<span data-ttu-id="f5095-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f5095-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5095-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5095-125">OUTPUTS</span></span>

### <span data-ttu-id="f5095-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="f5095-126">System.Object</span></span>

## <span data-ttu-id="f5095-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5095-127">NOTES</span></span>

## <span data-ttu-id="f5095-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5095-128">RELATED LINKS</span></span>

[<span data-ttu-id="f5095-129">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f5095-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f5095-130">Neu – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f5095-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f5095-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f5095-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


