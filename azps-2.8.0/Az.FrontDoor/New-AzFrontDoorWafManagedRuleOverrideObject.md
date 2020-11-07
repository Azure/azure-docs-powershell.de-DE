---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 8bfab06686cdabcb801b51b11298bf717f748770
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651111"
---
# <span data-ttu-id="0f730-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="0f730-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="0f730-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f730-102">SYNOPSIS</span></span>
<span data-ttu-id="0f730-103">Erstellen eines verwalteten Regel Außerkraftsetzungs Objekts</span><span class="sxs-lookup"><span data-stu-id="0f730-103">Create managed rule override object</span></span>

## <span data-ttu-id="0f730-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f730-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f730-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f730-105">DESCRIPTION</span></span>
<span data-ttu-id="0f730-106">Erstellen eines PSAzureManagedRuleOverride-Objekts für verwaltete WAF-Regelgruppe außer Kraft setzen der Objekterstellung.</span><span class="sxs-lookup"><span data-stu-id="0f730-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="0f730-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f730-107">EXAMPLES</span></span>

### <span data-ttu-id="0f730-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f730-108">Example 1</span></span>
<span data-ttu-id="0f730-109">Erstellen eines verwalteten Regel Außerkraftsetzungs Objekts für Regel 942250 (in der SQLI-Gruppe)</span><span class="sxs-lookup"><span data-stu-id="0f730-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="0f730-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f730-110">PARAMETERS</span></span>

### <span data-ttu-id="0f730-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="0f730-111">-Action</span></span>
<span data-ttu-id="0f730-112">Aktion überschreiben</span><span class="sxs-lookup"><span data-stu-id="0f730-112">Override Action</span></span>

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

### <span data-ttu-id="0f730-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f730-113">-DefaultProfile</span></span>
<span data-ttu-id="0f730-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f730-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f730-115">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="0f730-115">-Disabled</span></span>
<span data-ttu-id="0f730-116">Deaktivierter Zustand</span><span class="sxs-lookup"><span data-stu-id="0f730-116">Disabled state</span></span>

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

### <span data-ttu-id="0f730-117">-Lineal</span><span class="sxs-lookup"><span data-stu-id="0f730-117">-RuleId</span></span>
<span data-ttu-id="0f730-118">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="0f730-118">Rule ID</span></span>

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

### <span data-ttu-id="0f730-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f730-119">CommonParameters</span></span>
<span data-ttu-id="0f730-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f730-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f730-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f730-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f730-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f730-122">INPUTS</span></span>

### <span data-ttu-id="0f730-123">Keine</span><span class="sxs-lookup"><span data-stu-id="0f730-123">None</span></span>

## <span data-ttu-id="0f730-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f730-124">OUTPUTS</span></span>

### <span data-ttu-id="0f730-125">Microsoft. Azure. Commands. Haustür. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0f730-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="0f730-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f730-126">NOTES</span></span>

## <span data-ttu-id="0f730-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f730-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f730-128">Neu – AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="0f730-128">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)