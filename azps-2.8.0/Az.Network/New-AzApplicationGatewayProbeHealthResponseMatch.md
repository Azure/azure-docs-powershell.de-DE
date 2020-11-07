---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: c98d36e7f08d16f12581c340b875e26f5a393f1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822180"
---
# <span data-ttu-id="a14ec-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a14ec-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a14ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a14ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a14ec-103">Erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a14ec-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a14ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a14ec-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a14ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a14ec-106">**Das Cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a14ec-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a14ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a14ec-107">EXAMPLES</span></span>

### <span data-ttu-id="a14ec-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a14ec-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="a14ec-109">Dieser Befehl erstellt eine Integritäts Antwortübereinstimmung, die als Parameter an ProbeConfig übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a14ec-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="a14ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a14ec-110">PARAMETERS</span></span>

### <span data-ttu-id="a14ec-111">-Body</span><span class="sxs-lookup"><span data-stu-id="a14ec-111">-Body</span></span>
<span data-ttu-id="a14ec-112">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="a14ec-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="a14ec-113">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="a14ec-113">Default value is empty</span></span>

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

### <span data-ttu-id="a14ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14ec-114">-DefaultProfile</span></span>
<span data-ttu-id="a14ec-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a14ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a14ec-116">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="a14ec-116">-StatusCode</span></span>
<span data-ttu-id="a14ec-117">Zulässige Bereiche mit fehlerfreien Statuscodes. Der Standardbereich der fehlerfreien Statuscodes lautet 200-399.</span><span class="sxs-lookup"><span data-stu-id="a14ec-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="a14ec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14ec-118">CommonParameters</span></span>
<span data-ttu-id="a14ec-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14ec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14ec-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a14ec-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14ec-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a14ec-121">INPUTS</span></span>

### <span data-ttu-id="a14ec-122">Keine</span><span class="sxs-lookup"><span data-stu-id="a14ec-122">None</span></span>

## <span data-ttu-id="a14ec-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a14ec-123">OUTPUTS</span></span>

### <span data-ttu-id="a14ec-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a14ec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a14ec-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a14ec-125">NOTES</span></span>

## <span data-ttu-id="a14ec-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a14ec-126">RELATED LINKS</span></span>
