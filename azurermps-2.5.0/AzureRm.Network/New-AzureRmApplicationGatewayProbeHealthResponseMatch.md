---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
ms.openlocfilehash: 8781b52c3ed50a2a533b90815f1637ebcfe6df52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848132"
---
# <span data-ttu-id="7cedd-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7cedd-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7cedd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7cedd-102">SYNOPSIS</span></span>
<span data-ttu-id="7cedd-103">Erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cedd-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cedd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cedd-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cedd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cedd-105">DESCRIPTION</span></span>
<span data-ttu-id="7cedd-106">**Das Cmdlet Add-AzureRmApplicationGatewayProbeHealthResponseMatch** erstellt eine Antwortübereinstimmung für Integritätsprüfungen, die von der Integritätsprüfung für ein Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cedd-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="7cedd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cedd-107">EXAMPLES</span></span>

### <span data-ttu-id="7cedd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7cedd-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="7cedd-109">Dieser Befehl erstellt eine Integritäts Antwortübereinstimmung, die als Parameter an ProbeConfig übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="7cedd-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="7cedd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cedd-110">PARAMETERS</span></span>

### <span data-ttu-id="7cedd-111">-Body</span><span class="sxs-lookup"><span data-stu-id="7cedd-111">-Body</span></span>
<span data-ttu-id="7cedd-112">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="7cedd-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="7cedd-113">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="7cedd-113">Default value is empty</span></span>

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

### <span data-ttu-id="7cedd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cedd-114">-DefaultProfile</span></span>
<span data-ttu-id="7cedd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7cedd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cedd-116">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="7cedd-116">-StatusCode</span></span>
<span data-ttu-id="7cedd-117">Zulässige Bereiche mit fehlerfreien Statuscodes. Der Standardbereich der fehlerfreien Statuscodes lautet 200-399.</span><span class="sxs-lookup"><span data-stu-id="7cedd-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="7cedd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cedd-118">CommonParameters</span></span>
<span data-ttu-id="7cedd-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cedd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cedd-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cedd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cedd-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7cedd-121">INPUTS</span></span>

### <span data-ttu-id="7cedd-122">Keine</span><span class="sxs-lookup"><span data-stu-id="7cedd-122">None</span></span>

## <span data-ttu-id="7cedd-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7cedd-123">OUTPUTS</span></span>

### <span data-ttu-id="7cedd-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7cedd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7cedd-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7cedd-125">NOTES</span></span>

## <span data-ttu-id="7cedd-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7cedd-126">RELATED LINKS</span></span>

