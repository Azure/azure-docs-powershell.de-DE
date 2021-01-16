---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296452"
---
# <span data-ttu-id="3b818-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="3b818-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="3b818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b818-102">SYNOPSIS</span></span>
<span data-ttu-id="3b818-103">Erstellen einer neuen benutzerdefinierten Warnungsregel für die Gerätesicherheitsgruppe (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="3b818-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="3b818-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b818-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b818-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b818-105">DESCRIPTION</span></span>
<span data-ttu-id="3b818-106">Das New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject erstellt eine neue Liste der verweigerten benutzerdefinierten Warnungsregeln für die Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="3b818-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="3b818-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b818-107">EXAMPLES</span></span>

### <span data-ttu-id="3b818-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b818-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="3b818-109">Erstellen einer neuen benutzerdefinierten Warnungsregel für die Benachrichtigungsliste mit dem Typ "SomeRuleType" und dem status set to desable</span><span class="sxs-lookup"><span data-stu-id="3b818-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="3b818-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b818-110">PARAMETERS</span></span>

### <span data-ttu-id="3b818-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b818-111">-DefaultProfile</span></span>
<span data-ttu-id="3b818-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b818-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b818-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="3b818-113">-DenylistValue</span></span>
<span data-ttu-id="3b818-114">Listenwerte verweigern.</span><span class="sxs-lookup"><span data-stu-id="3b818-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b818-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="3b818-115">-Enabled</span></span>
<span data-ttu-id="3b818-116">Ist Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b818-116">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b818-117">-Type</span><span class="sxs-lookup"><span data-stu-id="3b818-117">-Type</span></span>
<span data-ttu-id="3b818-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="3b818-118">Rule type.</span></span>

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

### <span data-ttu-id="3b818-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b818-119">CommonParameters</span></span>
<span data-ttu-id="3b818-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b818-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b818-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b818-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b818-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b818-122">INPUTS</span></span>

### <span data-ttu-id="3b818-123">Keine</span><span class="sxs-lookup"><span data-stu-id="3b818-123">None</span></span>

## <span data-ttu-id="3b818-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b818-124">OUTPUTS</span></span>

### <span data-ttu-id="3b818-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="3b818-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="3b818-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b818-126">NOTES</span></span>

## <span data-ttu-id="3b818-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b818-127">RELATED LINKS</span></span>
