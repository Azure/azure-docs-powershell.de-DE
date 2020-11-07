---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845527"
---
# <span data-ttu-id="fd5f2-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="fd5f2-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="fd5f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5f2-103">Abrufen WAF verwalteter Regel Satz Definitionen</span><span class="sxs-lookup"><span data-stu-id="fd5f2-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="fd5f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd5f2-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd5f2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd5f2-105">DESCRIPTION</span></span>
<span data-ttu-id="fd5f2-106">Ruft die Liste der verwalteten WAF-Regel Satz Definitionen ab, die als Referenz verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fd5f2-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="fd5f2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd5f2-107">EXAMPLES</span></span>

### <span data-ttu-id="fd5f2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd5f2-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="fd5f2-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="fd5f2-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="fd5f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd5f2-110">PARAMETERS</span></span>

### <span data-ttu-id="fd5f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5f2-111">-DefaultProfile</span></span>
<span data-ttu-id="fd5f2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd5f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd5f2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5f2-113">CommonParameters</span></span>
<span data-ttu-id="fd5f2-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd5f2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5f2-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd5f2-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5f2-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd5f2-116">INPUTS</span></span>

### <span data-ttu-id="fd5f2-117">Keine</span><span class="sxs-lookup"><span data-stu-id="fd5f2-117">None</span></span>

## <span data-ttu-id="fd5f2-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd5f2-118">OUTPUTS</span></span>

### <span data-ttu-id="fd5f2-119">Microsoft. Azure. Commands. Haustür. Models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="fd5f2-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="fd5f2-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd5f2-120">NOTES</span></span>

## <span data-ttu-id="fd5f2-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd5f2-121">RELATED LINKS</span></span>

<span data-ttu-id="fd5f2-122">[Neu – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Neu – AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Neu – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="fd5f2-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
