---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 49fe9e11bb11131f8270c53afc0fc9fb6ab6dae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824619"
---
# <span data-ttu-id="0daa3-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0daa3-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0daa3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0daa3-102">SYNOPSIS</span></span>
<span data-ttu-id="0daa3-103">Testet den Verbindungsstatus einer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0daa3-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="0daa3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0daa3-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0daa3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0daa3-105">DESCRIPTION</span></span>
<span data-ttu-id="0daa3-106">Das Cmdlet **Test-AzStreamAnalyticsOutput** testet, ob Datenstrom Analyse eine Verbindung mit einer Ausgabe herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0daa3-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="0daa3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0daa3-107">EXAMPLES</span></span>

### <span data-ttu-id="0daa3-108">Beispiel 1: Testen des Verbindungsstatus einer Ausgabe</span><span class="sxs-lookup"><span data-stu-id="0daa3-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0daa3-109">Dadurch wird der Verbindungsstatus der Ausgabe Ausgabe in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="0daa3-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="0daa3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0daa3-110">PARAMETERS</span></span>

### <span data-ttu-id="0daa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daa3-111">-DefaultProfile</span></span>
<span data-ttu-id="0daa3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0daa3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0daa3-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="0daa3-113">-JobName</span></span>
<span data-ttu-id="0daa3-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die gewünschte Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="0daa3-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0daa3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0daa3-115">-Name</span></span>
<span data-ttu-id="0daa3-116">Gibt den Namen der zu testenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="0daa3-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="0daa3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0daa3-117">-ResourceGroupName</span></span>
<span data-ttu-id="0daa3-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="0daa3-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0daa3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daa3-119">CommonParameters</span></span>
<span data-ttu-id="0daa3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0daa3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daa3-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0daa3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daa3-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0daa3-122">INPUTS</span></span>

### <span data-ttu-id="0daa3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0daa3-123">System.String</span></span>

## <span data-ttu-id="0daa3-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0daa3-124">OUTPUTS</span></span>

### <span data-ttu-id="0daa3-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0daa3-125">System.Boolean</span></span>

## <span data-ttu-id="0daa3-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0daa3-126">NOTES</span></span>

## <span data-ttu-id="0daa3-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0daa3-127">RELATED LINKS</span></span>

[<span data-ttu-id="0daa3-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0daa3-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0daa3-129">Neu – AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0daa3-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0daa3-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0daa3-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


