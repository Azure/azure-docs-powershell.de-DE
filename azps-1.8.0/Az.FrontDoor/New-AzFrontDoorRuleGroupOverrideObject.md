---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 6175b99f5da139344c351189db5fbc5a13a137c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820016"
---
# <span data-ttu-id="a2858-101">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="a2858-101">New-AzFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="a2858-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2858-102">SYNOPSIS</span></span>
<span data-ttu-id="a2858-103">Erstellen eines RuleGroupOverride-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="a2858-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="a2858-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2858-104">SYNTAX</span></span>

```
New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2858-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2858-105">DESCRIPTION</span></span>
<span data-ttu-id="a2858-106">Erstellen eines RuleGroupOverride-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="a2858-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="a2858-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2858-107">EXAMPLES</span></span>

### <span data-ttu-id="a2858-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2858-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="a2858-109">Erstellen eines RuleGroupOverride-Objekts</span><span class="sxs-lookup"><span data-stu-id="a2858-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="a2858-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2858-110">PARAMETERS</span></span>

### <span data-ttu-id="a2858-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2858-111">-DefaultProfile</span></span>
<span data-ttu-id="a2858-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2858-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2858-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a2858-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="a2858-114">Regel Überschreibungs Liste</span><span class="sxs-lookup"><span data-stu-id="a2858-114">Rule override list</span></span>

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

### <span data-ttu-id="a2858-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="a2858-115">-RuleGroupName</span></span>
<span data-ttu-id="a2858-116">Regelgruppen Name, für den diese Außerkraftsetzungen gelten</span><span class="sxs-lookup"><span data-stu-id="a2858-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="a2858-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2858-117">CommonParameters</span></span>
<span data-ttu-id="a2858-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2858-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2858-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2858-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2858-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2858-120">INPUTS</span></span>

### <span data-ttu-id="a2858-121">Keine</span><span class="sxs-lookup"><span data-stu-id="a2858-121">None</span></span>

## <span data-ttu-id="a2858-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2858-122">OUTPUTS</span></span>

### <span data-ttu-id="a2858-123">Microsoft. Azure. Commands. Haustür. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a2858-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="a2858-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2858-124">NOTES</span></span>

## <span data-ttu-id="a2858-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2858-125">RELATED LINKS</span></span>

[<span data-ttu-id="a2858-126">Neu – AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a2858-126">New-AzFrontDoorManagedRuleObject</span></span>](./New-AzFrontDoorManagedRuleObject.md)
