---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179516"
---
# <span data-ttu-id="83e37-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="83e37-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="83e37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83e37-102">SYNOPSIS</span></span>
<span data-ttu-id="83e37-103">Ruft Informationen zum Streaming Unit-Kontingent für einen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="83e37-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="83e37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83e37-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83e37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83e37-105">DESCRIPTION</span></span>
<span data-ttu-id="83e37-106">Das Cmdlet " **Get-AzStreamAnalyticsQuota** " Ruft Informationen zum Streaming Unit-Kontingent für einen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="83e37-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="83e37-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83e37-107">EXAMPLES</span></span>

### <span data-ttu-id="83e37-108">Beispiel 1: Abrufen von Informationen zum Streaming Unit-Kontingent für einen Bereich</span><span class="sxs-lookup"><span data-stu-id="83e37-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="83e37-109">Dieser Befehl gibt Informationen zur Datenstrom Kontingent-und-Auslastung in der Region West Amerika zurück.</span><span class="sxs-lookup"><span data-stu-id="83e37-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="83e37-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="83e37-110">PARAMETERS</span></span>

### <span data-ttu-id="83e37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e37-111">-DefaultProfile</span></span>
<span data-ttu-id="83e37-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83e37-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83e37-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="83e37-113">-Location</span></span>
<span data-ttu-id="83e37-114">Gibt den Namen eines Azure-Bereichs oder eines Datencenter-Speicherorts an, für den Datenstrom Einheiten Kontingentinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83e37-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="83e37-115"> http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#servicesEine Liste der unterstützten Azure-Bereiche finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="83e37-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="83e37-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e37-116">CommonParameters</span></span>
<span data-ttu-id="83e37-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e37-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e37-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e37-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e37-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83e37-119">INPUTS</span></span>

### <span data-ttu-id="83e37-120">System. String</span><span class="sxs-lookup"><span data-stu-id="83e37-120">System.String</span></span>

## <span data-ttu-id="83e37-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83e37-121">OUTPUTS</span></span>

### <span data-ttu-id="83e37-122">Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="83e37-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="83e37-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="83e37-123">NOTES</span></span>

## <span data-ttu-id="83e37-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83e37-124">RELATED LINKS</span></span>

[<span data-ttu-id="83e37-125">Azure Stream Analytics-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="83e37-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


