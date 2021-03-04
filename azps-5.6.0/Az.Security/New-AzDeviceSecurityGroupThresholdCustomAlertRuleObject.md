---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 869512fb91e86d90381bbcba9e492198b9a51005
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934704"
---
# <span data-ttu-id="82e11-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="82e11-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="82e11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e11-102">SYNOPSIS</span></span>
<span data-ttu-id="82e11-103">Erstellen einer neuen benutzerdefinierten Benachrichtigungsregel für Gerätesicherheitsgruppe (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="82e11-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="82e11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82e11-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82e11-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82e11-105">DESCRIPTION</span></span>
<span data-ttu-id="82e11-106">Das New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject-Cmdlet erstellt eine neue Liste der benutzerdefinierten Schwellenwerte für Benachrichtigungsregeln für Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="82e11-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="82e11-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82e11-107">EXAMPLES</span></span>

### <span data-ttu-id="82e11-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82e11-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="82e11-109">Erstellen einer neuen benutzerdefinierten Schwellenwertwarnungsregel vom Typ "SomeRuleType" mit statusfähigen Antwerten für minimalen und maximalen Schwellenwert</span><span class="sxs-lookup"><span data-stu-id="82e11-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="82e11-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82e11-110">PARAMETERS</span></span>

### <span data-ttu-id="82e11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e11-111">-DefaultProfile</span></span>
<span data-ttu-id="82e11-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82e11-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e11-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="82e11-113">-Enabled</span></span>
<span data-ttu-id="82e11-114">Ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="82e11-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="82e11-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="82e11-115">-MaxThreshold</span></span>
<span data-ttu-id="82e11-116">Maximaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="82e11-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e11-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="82e11-117">-MinThreshold</span></span>
<span data-ttu-id="82e11-118">Mindestschwellenwert.</span><span class="sxs-lookup"><span data-stu-id="82e11-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e11-119">-Type</span><span class="sxs-lookup"><span data-stu-id="82e11-119">-Type</span></span>
<span data-ttu-id="82e11-120">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="82e11-120">Rule type.</span></span>

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

### <span data-ttu-id="82e11-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e11-121">CommonParameters</span></span>
<span data-ttu-id="82e11-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82e11-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e11-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82e11-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e11-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82e11-124">INPUTS</span></span>

### <span data-ttu-id="82e11-125">Keine</span><span class="sxs-lookup"><span data-stu-id="82e11-125">None</span></span>

## <span data-ttu-id="82e11-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82e11-126">OUTPUTS</span></span>

### <span data-ttu-id="82e11-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="82e11-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="82e11-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82e11-128">NOTES</span></span>

## <span data-ttu-id="82e11-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82e11-129">RELATED LINKS</span></span>
