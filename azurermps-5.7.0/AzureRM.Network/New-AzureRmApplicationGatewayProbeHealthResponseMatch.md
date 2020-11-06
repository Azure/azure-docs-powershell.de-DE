---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 3306bdeb37271072b5d7e1054286f5fd9d460403
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497542"
---
# <span data-ttu-id="f723a-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="f723a-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="f723a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f723a-102">SYNOPSIS</span></span>
<span data-ttu-id="f723a-103">Erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f723a-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f723a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f723a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f723a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f723a-105">DESCRIPTION</span></span>
<span data-ttu-id="f723a-106">**Das Cmdlet Add-AzureRmApplicationGatewayProbeHealthResponseMatch** erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f723a-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="f723a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f723a-107">EXAMPLES</span></span>

### <span data-ttu-id="f723a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f723a-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="f723a-109">Dieser Befehl erstellt eine Integritäts Antwortübereinstimmung, die als Parameter an ProbeConfig übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f723a-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="f723a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f723a-110">PARAMETERS</span></span>

### <span data-ttu-id="f723a-111">-Body</span><span class="sxs-lookup"><span data-stu-id="f723a-111">-Body</span></span>
<span data-ttu-id="f723a-112">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="f723a-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="f723a-113">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="f723a-113">Default value is empty</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f723a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f723a-114">-DefaultProfile</span></span>
<span data-ttu-id="f723a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f723a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f723a-116">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="f723a-116">-StatusCode</span></span>
<span data-ttu-id="f723a-117">Zulässige Bereiche mit fehlerfreien Statuscodes. Der Standardbereich der fehlerfreien Statuscodes lautet 200-399.</span><span class="sxs-lookup"><span data-stu-id="f723a-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f723a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f723a-118">CommonParameters</span></span>
<span data-ttu-id="f723a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f723a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f723a-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f723a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f723a-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f723a-121">INPUTS</span></span>

### <span data-ttu-id="f723a-122">Keine</span><span class="sxs-lookup"><span data-stu-id="f723a-122">None</span></span>

## <span data-ttu-id="f723a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f723a-123">OUTPUTS</span></span>

### <span data-ttu-id="f723a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="f723a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="f723a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="f723a-125">NOTES</span></span>

## <span data-ttu-id="f723a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f723a-126">RELATED LINKS</span></span>

