---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179262"
---
# <span data-ttu-id="3cd84-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3cd84-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3cd84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cd84-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd84-103">Abrufen WAF verwalteter Regel Satz Definitionen</span><span class="sxs-lookup"><span data-stu-id="3cd84-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="3cd84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cd84-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cd84-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cd84-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd84-106">Ruft die Liste der verwalteten WAF-Regel Satz Definitionen ab, die als Referenz verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3cd84-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="3cd84-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cd84-107">EXAMPLES</span></span>

### <span data-ttu-id="3cd84-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3cd84-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="3cd84-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="3cd84-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3cd84-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cd84-110">PARAMETERS</span></span>

### <span data-ttu-id="3cd84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd84-111">-DefaultProfile</span></span>
<span data-ttu-id="3cd84-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cd84-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd84-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd84-113">CommonParameters</span></span>
<span data-ttu-id="3cd84-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd84-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd84-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cd84-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd84-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cd84-116">INPUTS</span></span>

### <span data-ttu-id="3cd84-117">Keine</span><span class="sxs-lookup"><span data-stu-id="3cd84-117">None</span></span>

## <span data-ttu-id="3cd84-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cd84-118">OUTPUTS</span></span>

### <span data-ttu-id="3cd84-119">Microsoft. Azure. Commands. Haustür. Models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3cd84-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3cd84-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cd84-120">NOTES</span></span>

## <span data-ttu-id="3cd84-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cd84-121">RELATED LINKS</span></span>

<span data-ttu-id="3cd84-122">[Neu – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Neu – AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Neu – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="3cd84-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
