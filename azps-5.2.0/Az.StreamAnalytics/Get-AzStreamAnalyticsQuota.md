---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366399"
---
# <span data-ttu-id="158e9-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="158e9-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="158e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158e9-102">SYNOPSIS</span></span>
<span data-ttu-id="158e9-103">Ruft Informationen zum Kontingent der Streamingeinheit für eine Region ab.</span><span class="sxs-lookup"><span data-stu-id="158e9-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="158e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="158e9-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158e9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="158e9-105">DESCRIPTION</span></span>
<span data-ttu-id="158e9-106">Das **Cmdlet "Get-AzStreamAnalyticsQuota"** ruft Informationen zum Kontingent "Streaming Unit" für eine Region ab.</span><span class="sxs-lookup"><span data-stu-id="158e9-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="158e9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="158e9-107">EXAMPLES</span></span>

### <span data-ttu-id="158e9-108">BEISPIEL 1: Informationen zum Kontingent der Streamingeinheit für eine Region</span><span class="sxs-lookup"><span data-stu-id="158e9-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="158e9-109">Dieser Befehl gibt Informationen zum Kontingent "Streaming Unit" und zur Nutzung in der Region "USA, Westen" zurück.</span><span class="sxs-lookup"><span data-stu-id="158e9-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="158e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="158e9-110">PARAMETERS</span></span>

### <span data-ttu-id="158e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158e9-111">-DefaultProfile</span></span>
<span data-ttu-id="158e9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="158e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158e9-113">-Location</span><span class="sxs-lookup"><span data-stu-id="158e9-113">-Location</span></span>
<span data-ttu-id="158e9-114">Gibt den Namen des Standorts einer Azure-Region oder eines Rechenzentrums an, für den Kontingentinformationen für Streamingeinheiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="158e9-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="158e9-115">Hier http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services finden Sie eine Liste der unterstützten Azure-Regionen.</span><span class="sxs-lookup"><span data-stu-id="158e9-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="158e9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158e9-116">CommonParameters</span></span>
<span data-ttu-id="158e9-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158e9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158e9-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158e9-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158e9-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="158e9-119">INPUTS</span></span>

### <span data-ttu-id="158e9-120">System.String</span><span class="sxs-lookup"><span data-stu-id="158e9-120">System.String</span></span>

## <span data-ttu-id="158e9-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="158e9-121">OUTPUTS</span></span>

### <span data-ttu-id="158e9-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="158e9-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="158e9-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="158e9-123">NOTES</span></span>

## <span data-ttu-id="158e9-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="158e9-124">RELATED LINKS</span></span>

[<span data-ttu-id="158e9-125">Azure Stream Analytics-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="158e9-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


