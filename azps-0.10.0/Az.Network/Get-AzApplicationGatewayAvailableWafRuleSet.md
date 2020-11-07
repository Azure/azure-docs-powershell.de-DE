---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableWafRuleSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: f8f8411a40ddbc4d0e2f0e4b508385717e0c4173
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841759"
---
# <span data-ttu-id="55e90-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="55e90-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="55e90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55e90-102">SYNOPSIS</span></span>
<span data-ttu-id="55e90-103">Ruft alle verfügbaren Webanwendungs-Firewallregel-Regelsätze ab.</span><span class="sxs-lookup"><span data-stu-id="55e90-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="55e90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55e90-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55e90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55e90-105">DESCRIPTION</span></span>
<span data-ttu-id="55e90-106">Das Cmdlet " **Get-AzApplicationGatewayAvailableWafRuleSet** " ruft alle verfügbaren Firewall-Regelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="55e90-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="55e90-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55e90-107">EXAMPLES</span></span>

### <span data-ttu-id="55e90-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55e90-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="55e90-109">Diese Befehle gibt alle verfügbaren Firewall-Regelsätze für Webanwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="55e90-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="55e90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="55e90-110">PARAMETERS</span></span>

### <span data-ttu-id="55e90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e90-111">-DefaultProfile</span></span>
<span data-ttu-id="55e90-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55e90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e90-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e90-113">CommonParameters</span></span>
<span data-ttu-id="55e90-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55e90-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e90-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e90-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e90-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55e90-116">INPUTS</span></span>

### <span data-ttu-id="55e90-117">Keine</span><span class="sxs-lookup"><span data-stu-id="55e90-117">None</span></span>

## <span data-ttu-id="55e90-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55e90-118">OUTPUTS</span></span>

### <span data-ttu-id="55e90-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="55e90-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="55e90-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="55e90-120">NOTES</span></span>
<span data-ttu-id="55e90-121">**List-AzApplicationGatewayAvailableWafRuleSet** ist ein Alias für das Cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="55e90-121">**List-AzApplicationGatewayAvailableWafRuleSet** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="55e90-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55e90-122">RELATED LINKS</span></span>

