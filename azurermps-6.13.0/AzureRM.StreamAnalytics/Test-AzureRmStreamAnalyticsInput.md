---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 6256fc57d4084a55b2288875b56c6c616b16f8b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502806"
---
# <span data-ttu-id="59c3c-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59c3c-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="59c3c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="59c3c-103">Testet den Verbindungsstatus einer Eingabe.</span><span class="sxs-lookup"><span data-stu-id="59c3c-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59c3c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59c3c-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c3c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="59c3c-106">Das Cmdlet **Test-AzureRmStreamAnalyticsInput** testet die Möglichkeit von Datenstrom Analysen, eine Verbindung mit einer Eingabe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="59c3c-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="59c3c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="59c3c-108">Beispiel 1: Testen des Verbindungsstatus eines Eingabedatenstroms</span><span class="sxs-lookup"><span data-stu-id="59c3c-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="59c3c-109">Dadurch wird der Verbindungsstatus des Eingabe EntryStream in StreamingJob getestet.</span><span class="sxs-lookup"><span data-stu-id="59c3c-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="59c3c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59c3c-110">PARAMETERS</span></span>

### <span data-ttu-id="59c3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c3c-111">-DefaultProfile</span></span>
<span data-ttu-id="59c3c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59c3c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59c3c-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="59c3c-113">-JobName</span></span>
<span data-ttu-id="59c3c-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="59c3c-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="59c3c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="59c3c-115">-Name</span></span>
<span data-ttu-id="59c3c-116">Gibt den Namen der zu testenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="59c3c-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="59c3c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c3c-117">-ResourceGroupName</span></span>
<span data-ttu-id="59c3c-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="59c3c-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="59c3c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c3c-119">CommonParameters</span></span>
<span data-ttu-id="59c3c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c3c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c3c-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59c3c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c3c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59c3c-122">INPUTS</span></span>

### <span data-ttu-id="59c3c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="59c3c-123">System.String</span></span>

## <span data-ttu-id="59c3c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59c3c-124">OUTPUTS</span></span>

### <span data-ttu-id="59c3c-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59c3c-125">System.Boolean</span></span>

## <span data-ttu-id="59c3c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="59c3c-126">NOTES</span></span>

## <span data-ttu-id="59c3c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59c3c-127">RELATED LINKS</span></span>

[<span data-ttu-id="59c3c-128">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59c3c-128">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="59c3c-129">Neu – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59c3c-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="59c3c-130">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59c3c-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


