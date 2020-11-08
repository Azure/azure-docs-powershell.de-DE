---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008478"
---
# <span data-ttu-id="1b26f-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="1b26f-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="1b26f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b26f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b26f-103">Erstellen eines RuleGroupOverride-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="1b26f-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="1b26f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b26f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b26f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b26f-105">DESCRIPTION</span></span>
<span data-ttu-id="1b26f-106">Erstellen eines RuleGroupOverride-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="1b26f-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="1b26f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b26f-107">EXAMPLES</span></span>

### <span data-ttu-id="1b26f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b26f-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="1b26f-109">Erstellen eines RuleGroupOverride-Objekts</span><span class="sxs-lookup"><span data-stu-id="1b26f-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="1b26f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b26f-110">PARAMETERS</span></span>

### <span data-ttu-id="1b26f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b26f-111">-DefaultProfile</span></span>
<span data-ttu-id="1b26f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b26f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b26f-113">– Ausschluss</span><span class="sxs-lookup"><span data-stu-id="1b26f-113">-Exclusion</span></span>
<span data-ttu-id="1b26f-114">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="1b26f-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b26f-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="1b26f-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="1b26f-116">Regel Überschreibungs Liste</span><span class="sxs-lookup"><span data-stu-id="1b26f-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b26f-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="1b26f-117">-RuleGroupName</span></span>
<span data-ttu-id="1b26f-118">Regelgruppen Name, für den diese Außerkraftsetzungen gelten</span><span class="sxs-lookup"><span data-stu-id="1b26f-118">Rule Group Name for which these overrides apply</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b26f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b26f-119">CommonParameters</span></span>
<span data-ttu-id="1b26f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b26f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b26f-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b26f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b26f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b26f-122">INPUTS</span></span>

### <span data-ttu-id="1b26f-123">Keine</span><span class="sxs-lookup"><span data-stu-id="1b26f-123">None</span></span>

## <span data-ttu-id="1b26f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b26f-124">OUTPUTS</span></span>

### <span data-ttu-id="1b26f-125">Microsoft. Azure. Commands. Haustür. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1b26f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="1b26f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b26f-126">NOTES</span></span>

## <span data-ttu-id="1b26f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b26f-127">RELATED LINKS</span></span>

[<span data-ttu-id="1b26f-128">Neu – AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1b26f-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
