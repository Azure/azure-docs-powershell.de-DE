---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178770"
---
# <span data-ttu-id="1f0cf-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1f0cf-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1f0cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0cf-103">Erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f0cf-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1f0cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f0cf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f0cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f0cf-105">DESCRIPTION</span></span>
<span data-ttu-id="1f0cf-106">**Das Cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f0cf-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1f0cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f0cf-107">EXAMPLES</span></span>

### <span data-ttu-id="1f0cf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1f0cf-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="1f0cf-109">Dieser Befehl erstellt eine Integritäts Antwortübereinstimmung, die als Parameter an ProbeConfig übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f0cf-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="1f0cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f0cf-110">PARAMETERS</span></span>

### <span data-ttu-id="1f0cf-111">-Body</span><span class="sxs-lookup"><span data-stu-id="1f0cf-111">-Body</span></span>
<span data-ttu-id="1f0cf-112">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="1f0cf-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1f0cf-113">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="1f0cf-113">Default value is empty</span></span>

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

### <span data-ttu-id="1f0cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0cf-114">-DefaultProfile</span></span>
<span data-ttu-id="1f0cf-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f0cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f0cf-116">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="1f0cf-116">-StatusCode</span></span>
<span data-ttu-id="1f0cf-117">Zulässige Bereiche mit fehlerfreien Statuscodes. Der Standardbereich der fehlerfreien Statuscodes lautet 200-399.</span><span class="sxs-lookup"><span data-stu-id="1f0cf-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="1f0cf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0cf-118">CommonParameters</span></span>
<span data-ttu-id="1f0cf-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f0cf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0cf-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f0cf-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0cf-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f0cf-121">INPUTS</span></span>

### <span data-ttu-id="1f0cf-122">Keine</span><span class="sxs-lookup"><span data-stu-id="1f0cf-122">None</span></span>

## <span data-ttu-id="1f0cf-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f0cf-123">OUTPUTS</span></span>

### <span data-ttu-id="1f0cf-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1f0cf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1f0cf-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f0cf-125">NOTES</span></span>

## <span data-ttu-id="1f0cf-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f0cf-126">RELATED LINKS</span></span>
