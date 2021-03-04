---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 04da18bcd50fa547f1a59142682c93b4e3e5ab62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930008"
---
# <span data-ttu-id="9ff16-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="9ff16-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="9ff16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ff16-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff16-103">Erstellt eine Vom Integritätstest für ein Anwendungsgateway verwendete Übereinstimmung mit der Integritätsprobe.</span><span class="sxs-lookup"><span data-stu-id="9ff16-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="9ff16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ff16-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ff16-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ff16-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff16-106">**Das Add-AzApplicationGatewayProbeHealthResponseMatch-Cmdlet** erstellt eine Antwortübereinstimmung der Integritätssonde, die von Health Probe für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ff16-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="9ff16-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ff16-107">EXAMPLES</span></span>

### <span data-ttu-id="9ff16-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ff16-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="9ff16-109">Mit diesem Befehl wird eine Übereinstimmung mit der Integritätsantwort erstellt, die als Parameter an ProbeConfig übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ff16-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="9ff16-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ff16-110">PARAMETERS</span></span>

### <span data-ttu-id="9ff16-111">-Body</span><span class="sxs-lookup"><span data-stu-id="9ff16-111">-Body</span></span>
<span data-ttu-id="9ff16-112">Textkörper, der in der Integritätsantwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="9ff16-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="9ff16-113">Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="9ff16-113">Default value is empty</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff16-114">-DefaultProfile</span></span>
<span data-ttu-id="9ff16-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ff16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ff16-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9ff16-116">-StatusCode</span></span>
<span data-ttu-id="9ff16-117">Zulässige Bereiche mit fehlerfreien Statuscodes. Der Standardbereich der fehlerfreien Statuscodes ist 200 - 399</span><span class="sxs-lookup"><span data-stu-id="9ff16-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff16-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff16-118">CommonParameters</span></span>
<span data-ttu-id="9ff16-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff16-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff16-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff16-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff16-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ff16-121">INPUTS</span></span>

### <span data-ttu-id="9ff16-122">Keine</span><span class="sxs-lookup"><span data-stu-id="9ff16-122">None</span></span>

## <span data-ttu-id="9ff16-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ff16-123">OUTPUTS</span></span>

### <span data-ttu-id="9ff16-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="9ff16-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="9ff16-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ff16-125">NOTES</span></span>

## <span data-ttu-id="9ff16-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ff16-126">RELATED LINKS</span></span>
