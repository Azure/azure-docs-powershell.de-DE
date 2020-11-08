---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004043"
---
# <span data-ttu-id="3e6c9-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="3e6c9-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="3e6c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6c9-103">Erstellen eines verwalteten Regel Außerkraftsetzungs Objekts</span><span class="sxs-lookup"><span data-stu-id="3e6c9-103">Create managed rule override object</span></span>

## <span data-ttu-id="3e6c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e6c9-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e6c9-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6c9-106">Erstellen eines PSAzureManagedRuleOverride-Objekts für verwaltete WAF-Regelgruppe außer Kraft setzen der Objekterstellung.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="3e6c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e6c9-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6c9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e6c9-108">Example 1</span></span>
<span data-ttu-id="3e6c9-109">Erstellen eines verwalteten Regel Außerkraftsetzungs Objekts für Regel 942250 (in der SQLI-Gruppe)</span><span class="sxs-lookup"><span data-stu-id="3e6c9-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="3e6c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e6c9-110">PARAMETERS</span></span>

### <span data-ttu-id="3e6c9-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="3e6c9-111">-Action</span></span>
<span data-ttu-id="3e6c9-112">Aktion überschreiben</span><span class="sxs-lookup"><span data-stu-id="3e6c9-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6c9-113">-DefaultProfile</span></span>
<span data-ttu-id="3e6c9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e6c9-115">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="3e6c9-115">-Disabled</span></span>
<span data-ttu-id="3e6c9-116">Deaktivierter Zustand</span><span class="sxs-lookup"><span data-stu-id="3e6c9-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6c9-117">– Ausschluss</span><span class="sxs-lookup"><span data-stu-id="3e6c9-117">-Exclusion</span></span>
<span data-ttu-id="3e6c9-118">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="3e6c9-118">Exclusion</span></span>

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

### <span data-ttu-id="3e6c9-119">-Lineal</span><span class="sxs-lookup"><span data-stu-id="3e6c9-119">-RuleId</span></span>
<span data-ttu-id="3e6c9-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="3e6c9-120">Rule ID</span></span>

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

### <span data-ttu-id="3e6c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6c9-121">CommonParameters</span></span>
<span data-ttu-id="3e6c9-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6c9-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e6c9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6c9-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e6c9-124">INPUTS</span></span>

### <span data-ttu-id="3e6c9-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3e6c9-125">None</span></span>

## <span data-ttu-id="3e6c9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e6c9-126">OUTPUTS</span></span>

### <span data-ttu-id="3e6c9-127">Microsoft. Azure. Commands. Haustür. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="3e6c9-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="3e6c9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e6c9-128">NOTES</span></span>

## <span data-ttu-id="3e6c9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e6c9-129">RELATED LINKS</span></span>

[<span data-ttu-id="3e6c9-130">Neu – AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="3e6c9-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)