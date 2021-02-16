---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175444"
---
# <span data-ttu-id="3b7ca-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3b7ca-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3b7ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7ca-103">Definitionen von verwalteten WAF-Regelsatz erhalten</span><span class="sxs-lookup"><span data-stu-id="3b7ca-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="3b7ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b7ca-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b7ca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b7ca-105">DESCRIPTION</span></span>
<span data-ttu-id="3b7ca-106">Ruft die Liste der Definitionen verwalteter WAF-Regelsatz ab, die als Referenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b7ca-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="3b7ca-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b7ca-107">EXAMPLES</span></span>

### <span data-ttu-id="3b7ca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b7ca-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="3b7ca-109">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="3b7ca-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3b7ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b7ca-110">PARAMETERS</span></span>

### <span data-ttu-id="3b7ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b7ca-111">-DefaultProfile</span></span>
<span data-ttu-id="3b7ca-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b7ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b7ca-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7ca-113">CommonParameters</span></span>
<span data-ttu-id="3b7ca-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b7ca-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b7ca-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b7ca-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7ca-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b7ca-116">INPUTS</span></span>

### <span data-ttu-id="3b7ca-117">Keine</span><span class="sxs-lookup"><span data-stu-id="3b7ca-117">None</span></span>

## <span data-ttu-id="3b7ca-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b7ca-118">OUTPUTS</span></span>

### <span data-ttu-id="3b7ca-119">Microsoft.Azure.Commands.FrontDando.Models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3b7ca-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3b7ca-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b7ca-120">NOTES</span></span>

## <span data-ttu-id="3b7ca-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b7ca-121">RELATED LINKS</span></span>

<span data-ttu-id="3b7ca-122">[New-AzFrontDullWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDullWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontD dannWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="3b7ca-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
