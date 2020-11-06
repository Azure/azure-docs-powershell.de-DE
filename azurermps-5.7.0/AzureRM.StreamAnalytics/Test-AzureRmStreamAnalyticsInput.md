---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 34e1c2813292801d29a93a6914abf11b2725ec14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478153"
---
# <span data-ttu-id="a7298-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a7298-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="a7298-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7298-102">SYNOPSIS</span></span>
<span data-ttu-id="a7298-103">Testet den Verbindungsstatus einer Eingabe.</span><span class="sxs-lookup"><span data-stu-id="a7298-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7298-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7298-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7298-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7298-105">DESCRIPTION</span></span>
<span data-ttu-id="a7298-106">Das Cmdlet **Test-AzureRmStreamAnalyticsInput** testet die Möglichkeit von Datenstrom Analysen, eine Verbindung mit einer Eingabe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a7298-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="a7298-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7298-107">EXAMPLES</span></span>

### <span data-ttu-id="a7298-108">Beispiel 1: Testen des Verbindungsstatus eines Eingabedatenstroms</span><span class="sxs-lookup"><span data-stu-id="a7298-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="a7298-109">Dadurch wird der Verbindungsstatus des Eingabe EntryStream in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="a7298-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="a7298-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7298-110">PARAMETERS</span></span>

### <span data-ttu-id="a7298-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7298-111">-DefaultProfile</span></span>
<span data-ttu-id="a7298-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7298-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7298-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="a7298-113">-JobName</span></span>
<span data-ttu-id="a7298-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="a7298-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a7298-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a7298-115">-Name</span></span>
<span data-ttu-id="a7298-116">Gibt den Namen der zu testenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="a7298-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="a7298-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7298-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7298-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="a7298-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a7298-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7298-119">CommonParameters</span></span>
<span data-ttu-id="a7298-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7298-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7298-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7298-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7298-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7298-122">INPUTS</span></span>

### <span data-ttu-id="a7298-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a7298-123">None</span></span>
<span data-ttu-id="a7298-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a7298-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7298-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7298-125">OUTPUTS</span></span>

### <span data-ttu-id="a7298-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="a7298-126">System.Object</span></span>

## <span data-ttu-id="a7298-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7298-127">NOTES</span></span>

## <span data-ttu-id="a7298-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7298-128">RELATED LINKS</span></span>

[<span data-ttu-id="a7298-129">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a7298-129">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="a7298-130">Neu – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a7298-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="a7298-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a7298-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


