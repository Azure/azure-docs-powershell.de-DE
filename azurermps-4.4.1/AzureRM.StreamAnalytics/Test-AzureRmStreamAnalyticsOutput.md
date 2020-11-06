---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5c961289267b0680a88cd16d58574c906a9f4408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499922"
---
# <span data-ttu-id="b30b1-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b30b1-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="b30b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b30b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b30b1-103">Testet den Verbindungsstatus einer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b30b1-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b30b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b30b1-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b30b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b30b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b30b1-106">Das Cmdlet **Test-AzureRmStreamAnalyticsOutput** testet, ob Datenstrom Analyse eine Verbindung mit einer Ausgabe herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="b30b1-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="b30b1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b30b1-107">EXAMPLES</span></span>

### <span data-ttu-id="b30b1-108">Beispiel 1: Testen des Verbindungsstatus einer Ausgabe</span><span class="sxs-lookup"><span data-stu-id="b30b1-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="b30b1-109">Dadurch wird der Verbindungsstatus der Ausgabe Ausgabe in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="b30b1-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="b30b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b30b1-110">PARAMETERS</span></span>

### <span data-ttu-id="b30b1-111">-Jobname</span><span class="sxs-lookup"><span data-stu-id="b30b1-111">-JobName</span></span>
<span data-ttu-id="b30b1-112">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die gewünschte Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="b30b1-112">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b30b1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b30b1-113">-Name</span></span>
<span data-ttu-id="b30b1-114">Gibt den Namen der zu testenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="b30b1-114">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="b30b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="b30b1-116">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="b30b1-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b30b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30b1-117">-DefaultProfile</span></span>
<span data-ttu-id="b30b1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b30b1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b30b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30b1-119">CommonParameters</span></span>
<span data-ttu-id="b30b1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30b1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30b1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30b1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b30b1-122">INPUTS</span></span>

## <span data-ttu-id="b30b1-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b30b1-123">OUTPUTS</span></span>

### <span data-ttu-id="b30b1-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="b30b1-124">System.Object</span></span>

## <span data-ttu-id="b30b1-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b30b1-125">NOTES</span></span>

## <span data-ttu-id="b30b1-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b30b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="b30b1-127">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b30b1-127">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b30b1-128">Neu – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b30b1-128">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b30b1-129">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b30b1-129">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


