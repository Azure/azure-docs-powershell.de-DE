---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009712"
---
# <span data-ttu-id="83e7e-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="83e7e-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="83e7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="83e7e-103">Ruft alle verfügbaren Webanwendungs-Firewallregel-Regelsätze ab.</span><span class="sxs-lookup"><span data-stu-id="83e7e-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="83e7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83e7e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83e7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="83e7e-106">Das Cmdlet " **Get-AzApplicationGatewayAvailableWafRuleSet** " ruft alle verfügbaren Firewall-Regelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="83e7e-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="83e7e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83e7e-107">EXAMPLES</span></span>

### <span data-ttu-id="83e7e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83e7e-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="83e7e-109">Diese Befehle gibt alle verfügbaren Firewall-Regelsätze für Webanwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="83e7e-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="83e7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="83e7e-110">PARAMETERS</span></span>

### <span data-ttu-id="83e7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e7e-111">-DefaultProfile</span></span>
<span data-ttu-id="83e7e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83e7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83e7e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e7e-113">CommonParameters</span></span>
<span data-ttu-id="83e7e-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e7e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e7e-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83e7e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e7e-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83e7e-116">INPUTS</span></span>

### <span data-ttu-id="83e7e-117">Keine</span><span class="sxs-lookup"><span data-stu-id="83e7e-117">None</span></span>

## <span data-ttu-id="83e7e-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83e7e-118">OUTPUTS</span></span>

### <span data-ttu-id="83e7e-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="83e7e-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="83e7e-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="83e7e-120">NOTES</span></span>
<span data-ttu-id="83e7e-121">**List-AzApplicationGatewayAvailableWafRuleSets** ist ein Alias für das Cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="83e7e-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="83e7e-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83e7e-122">RELATED LINKS</span></span>
