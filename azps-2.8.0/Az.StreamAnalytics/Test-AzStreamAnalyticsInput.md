---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: b19a8359f3267d848d475028fe0cee2123949f7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824620"
---
# <span data-ttu-id="56b6d-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="56b6d-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="56b6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="56b6d-103">Testet den Verbindungsstatus einer Eingabe.</span><span class="sxs-lookup"><span data-stu-id="56b6d-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="56b6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56b6d-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56b6d-105">DESCRIPTION</span></span>
<span data-ttu-id="56b6d-106">Das Cmdlet **Test-AzStreamAnalyticsInput** testet die Möglichkeit von Datenstrom Analysen, eine Verbindung mit einer Eingabe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="56b6d-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="56b6d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56b6d-107">EXAMPLES</span></span>

### <span data-ttu-id="56b6d-108">Beispiel 1: Testen des Verbindungsstatus eines Eingabedatenstroms</span><span class="sxs-lookup"><span data-stu-id="56b6d-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="56b6d-109">Dadurch wird der Verbindungsstatus des Eingabe EntryStream in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="56b6d-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="56b6d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56b6d-110">PARAMETERS</span></span>

### <span data-ttu-id="56b6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b6d-111">-DefaultProfile</span></span>
<span data-ttu-id="56b6d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56b6d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56b6d-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="56b6d-113">-JobName</span></span>
<span data-ttu-id="56b6d-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="56b6d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="56b6d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="56b6d-115">-Name</span></span>
<span data-ttu-id="56b6d-116">Gibt den Namen der zu testenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="56b6d-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="56b6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="56b6d-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="56b6d-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="56b6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b6d-119">CommonParameters</span></span>
<span data-ttu-id="56b6d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b6d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b6d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b6d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56b6d-122">INPUTS</span></span>

### <span data-ttu-id="56b6d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="56b6d-123">System.String</span></span>

## <span data-ttu-id="56b6d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56b6d-124">OUTPUTS</span></span>

### <span data-ttu-id="56b6d-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56b6d-125">System.Boolean</span></span>

## <span data-ttu-id="56b6d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="56b6d-126">NOTES</span></span>

## <span data-ttu-id="56b6d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56b6d-127">RELATED LINKS</span></span>

[<span data-ttu-id="56b6d-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="56b6d-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="56b6d-129">Neu – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="56b6d-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="56b6d-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="56b6d-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


