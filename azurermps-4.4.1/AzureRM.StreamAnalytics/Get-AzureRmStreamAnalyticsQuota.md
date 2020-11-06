---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478838"
---
# <span data-ttu-id="ed1c0-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="ed1c0-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="ed1c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1c0-103">Ruft Informationen zum Streaming Unit-Kontingent für einen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="ed1c0-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed1c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed1c0-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed1c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="ed1c0-106">Das Cmdlet " **Get-AzureRmStreamAnalyticsQuota** " Ruft Informationen zum Streaming Unit-Kontingent für einen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="ed1c0-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="ed1c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed1c0-107">EXAMPLES</span></span>

### <span data-ttu-id="ed1c0-108">Beispiel 1: Abrufen von Informationen zum Streaming Unit-Kontingent für einen Bereich</span><span class="sxs-lookup"><span data-stu-id="ed1c0-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="ed1c0-109">Dieser Befehl gibt Informationen zur Datenstrom Kontingent-und-Auslastung in der Region West Amerika zurück.</span><span class="sxs-lookup"><span data-stu-id="ed1c0-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="ed1c0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed1c0-110">PARAMETERS</span></span>

### <span data-ttu-id="ed1c0-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="ed1c0-111">-Location</span></span>
<span data-ttu-id="ed1c0-112">Gibt den Namen eines Azure-Bereichs oder eines Datencenter-Speicherorts an, für den Datenstrom Einheiten Kontingentinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed1c0-112">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="ed1c0-113"> https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#servicesEine Liste der unterstützten Azure-Bereiche finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="ed1c0-113">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="ed1c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1c0-114">-DefaultProfile</span></span>
<span data-ttu-id="ed1c0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed1c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed1c0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1c0-116">CommonParameters</span></span>
<span data-ttu-id="ed1c0-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed1c0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1c0-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed1c0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1c0-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed1c0-119">INPUTS</span></span>

## <span data-ttu-id="ed1c0-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed1c0-120">OUTPUTS</span></span>

### <span data-ttu-id="ed1c0-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="ed1c0-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="ed1c0-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed1c0-122">NOTES</span></span>

## <span data-ttu-id="ed1c0-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed1c0-123">RELATED LINKS</span></span>

[<span data-ttu-id="ed1c0-124">Azure Stream Analytics-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ed1c0-124">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


