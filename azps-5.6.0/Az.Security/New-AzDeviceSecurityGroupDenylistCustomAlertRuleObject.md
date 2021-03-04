---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0b915176858c0641ca3076ea10022ae193718807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932251"
---
# <span data-ttu-id="b1517-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="b1517-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="b1517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1517-102">SYNOPSIS</span></span>
<span data-ttu-id="b1517-103">Erstellen einer neuen benutzerdefinierten Warnungsregel für die Benachrichtigungsliste für Gerätesicherheit (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="b1517-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="b1517-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1517-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1517-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1517-105">DESCRIPTION</span></span>
<span data-ttu-id="b1517-106">Das New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject-Cmdlet erstellt eine neue Liste der verweigerten benutzerdefinierten Benachrichtigungsregeln für Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="b1517-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="b1517-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1517-107">EXAMPLES</span></span>

### <span data-ttu-id="b1517-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1517-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="b1517-109">Erstellen einer neuen benutzerdefinierten Warnungsregel für die Benachrichtigungsliste mit dem Typ "SomeRuleType" und status set to desable</span><span class="sxs-lookup"><span data-stu-id="b1517-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="b1517-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b1517-110">PARAMETERS</span></span>

### <span data-ttu-id="b1517-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1517-111">-DefaultProfile</span></span>
<span data-ttu-id="b1517-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1517-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1517-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="b1517-113">-DenylistValue</span></span>
<span data-ttu-id="b1517-114">Verweigern Sie Listenwerte.</span><span class="sxs-lookup"><span data-stu-id="b1517-114">Deny list values.</span></span>

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

### <span data-ttu-id="b1517-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b1517-115">-Enabled</span></span>
<span data-ttu-id="b1517-116">Ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b1517-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="b1517-117">-Type</span><span class="sxs-lookup"><span data-stu-id="b1517-117">-Type</span></span>
<span data-ttu-id="b1517-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="b1517-118">Rule type.</span></span>

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

### <span data-ttu-id="b1517-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1517-119">CommonParameters</span></span>
<span data-ttu-id="b1517-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1517-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1517-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1517-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1517-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1517-122">INPUTS</span></span>

### <span data-ttu-id="b1517-123">Keine</span><span class="sxs-lookup"><span data-stu-id="b1517-123">None</span></span>

## <span data-ttu-id="b1517-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1517-124">OUTPUTS</span></span>

### <span data-ttu-id="b1517-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="b1517-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="b1517-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b1517-126">NOTES</span></span>

## <span data-ttu-id="b1517-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b1517-127">RELATED LINKS</span></span>
