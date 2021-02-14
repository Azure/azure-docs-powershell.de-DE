---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169896"
---
# <span data-ttu-id="65ba5-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="65ba5-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="65ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="65ba5-103">Erstellt eine Übereinstimmung mit der Integritätstestantwort, die von Health Probe für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65ba5-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="65ba5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65ba5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ba5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="65ba5-106">**Das Cmdlet "Add-AzApplicationGatewayProbeHealthResponseMatch"** erstellt eine Übereinstimmung mit der Integritätstestantwort, die von Health Probe für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65ba5-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="65ba5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65ba5-107">EXAMPLES</span></span>

### <span data-ttu-id="65ba5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65ba5-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="65ba5-109">Dieser Befehl erstellt eine Übereinstimmung mit der Integritätsantwort, die als Parameter an ProbeConfig übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="65ba5-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="65ba5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65ba5-110">PARAMETERS</span></span>

### <span data-ttu-id="65ba5-111">-Body</span><span class="sxs-lookup"><span data-stu-id="65ba5-111">-Body</span></span>
<span data-ttu-id="65ba5-112">Text, der in der Gesundheitsantwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="65ba5-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="65ba5-113">Der Standardwert ist leer.</span><span class="sxs-lookup"><span data-stu-id="65ba5-113">Default value is empty</span></span>

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

### <span data-ttu-id="65ba5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ba5-114">-DefaultProfile</span></span>
<span data-ttu-id="65ba5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65ba5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ba5-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="65ba5-116">-StatusCode</span></span>
<span data-ttu-id="65ba5-117">Zulässige Bereiche mit fehlerfreien Statuscodes. Der Standardbereich fehlerfreier Statuscodes ist 200 bis 399.</span><span class="sxs-lookup"><span data-stu-id="65ba5-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="65ba5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ba5-118">CommonParameters</span></span>
<span data-ttu-id="65ba5-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ba5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ba5-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ba5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ba5-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65ba5-121">INPUTS</span></span>

### <span data-ttu-id="65ba5-122">Keine</span><span class="sxs-lookup"><span data-stu-id="65ba5-122">None</span></span>

## <span data-ttu-id="65ba5-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65ba5-123">OUTPUTS</span></span>

### <span data-ttu-id="65ba5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="65ba5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="65ba5-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="65ba5-125">NOTES</span></span>

## <span data-ttu-id="65ba5-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="65ba5-126">RELATED LINKS</span></span>
