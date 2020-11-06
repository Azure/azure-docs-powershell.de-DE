---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: 27e5715f32b631fff3f185f0925d0b2a85967ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479121"
---
# <span data-ttu-id="fd937-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="fd937-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="fd937-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd937-102">SYNOPSIS</span></span>
<span data-ttu-id="fd937-103">Ruft alle verfügbaren Webanwendungs-Firewallregel-Regelsätze ab.</span><span class="sxs-lookup"><span data-stu-id="fd937-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd937-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd937-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd937-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd937-105">DESCRIPTION</span></span>
<span data-ttu-id="fd937-106">Das Cmdlet " **Get-AzureRmApplicationGatewayAvailableWafRuleSets** " ruft alle verfügbaren Firewall-Regelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="fd937-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="fd937-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd937-107">EXAMPLES</span></span>

### <span data-ttu-id="fd937-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd937-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="fd937-109">Diese Befehle gibt alle verfügbaren Firewall-Regelsätze für Webanwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="fd937-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="fd937-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd937-110">PARAMETERS</span></span>

### <span data-ttu-id="fd937-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd937-111">-DefaultProfile</span></span>
<span data-ttu-id="fd937-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd937-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd937-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd937-113">CommonParameters</span></span>
<span data-ttu-id="fd937-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd937-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd937-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd937-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd937-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd937-116">INPUTS</span></span>

### <span data-ttu-id="fd937-117">Keine</span><span class="sxs-lookup"><span data-stu-id="fd937-117">None</span></span>

## <span data-ttu-id="fd937-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd937-118">OUTPUTS</span></span>

### <span data-ttu-id="fd937-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="fd937-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="fd937-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd937-120">NOTES</span></span>
<span data-ttu-id="fd937-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** ist ein Alias für das Cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="fd937-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="fd937-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd937-122">RELATED LINKS</span></span>

