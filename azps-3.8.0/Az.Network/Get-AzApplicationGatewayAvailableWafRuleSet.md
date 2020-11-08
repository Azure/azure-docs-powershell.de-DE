---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003788"
---
# <span data-ttu-id="787e9-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="787e9-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="787e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="787e9-102">SYNOPSIS</span></span>
<span data-ttu-id="787e9-103">Ruft alle verfügbaren Webanwendungs-Firewallregel-Regelsätze ab.</span><span class="sxs-lookup"><span data-stu-id="787e9-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="787e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="787e9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="787e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="787e9-105">DESCRIPTION</span></span>
<span data-ttu-id="787e9-106">Das Cmdlet " **Get-AzApplicationGatewayAvailableWafRuleSet** " ruft alle verfügbaren Firewall-Regelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="787e9-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="787e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="787e9-107">EXAMPLES</span></span>

### <span data-ttu-id="787e9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="787e9-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="787e9-109">Diese Befehle gibt alle verfügbaren Firewall-Regelsätze für Webanwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="787e9-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="787e9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="787e9-110">PARAMETERS</span></span>

### <span data-ttu-id="787e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787e9-111">-DefaultProfile</span></span>
<span data-ttu-id="787e9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="787e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="787e9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787e9-113">CommonParameters</span></span>
<span data-ttu-id="787e9-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787e9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787e9-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="787e9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787e9-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="787e9-116">INPUTS</span></span>

### <span data-ttu-id="787e9-117">Keine</span><span class="sxs-lookup"><span data-stu-id="787e9-117">None</span></span>

## <span data-ttu-id="787e9-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="787e9-118">OUTPUTS</span></span>

### <span data-ttu-id="787e9-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="787e9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="787e9-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="787e9-120">NOTES</span></span>
<span data-ttu-id="787e9-121">**List-AzApplicationGatewayAvailableWafRuleSets** ist ein Alias für das Cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="787e9-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="787e9-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="787e9-122">RELATED LINKS</span></span>
