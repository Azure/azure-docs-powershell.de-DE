---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165153"
---
# <span data-ttu-id="d4719-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4719-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="d4719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4719-102">SYNOPSIS</span></span>
<span data-ttu-id="d4719-103">Erstellen eines neuen benutzerdefinierten Warnungsschwellenwerts für die Gerätesicherheitsgruppe (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="d4719-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d4719-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4719-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4719-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4719-105">DESCRIPTION</span></span>
<span data-ttu-id="d4719-106">Das New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject erstellt eine neue Liste der benutzerdefinierten Schwellenwerte für Warnungsregeln für die Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="d4719-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d4719-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4719-107">EXAMPLES</span></span>

### <span data-ttu-id="d4719-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4719-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="d4719-109">Erstellen eines neuen benutzerdefinierten Warnungsschwellenwerts vom Typ "SomeRuleType" mit statusfähigen Ant-Werten für den Minimal- und Maximalschwellenwert</span><span class="sxs-lookup"><span data-stu-id="d4719-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="d4719-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4719-110">PARAMETERS</span></span>

### <span data-ttu-id="d4719-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4719-111">-DefaultProfile</span></span>
<span data-ttu-id="d4719-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4719-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4719-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d4719-113">-Enabled</span></span>
<span data-ttu-id="d4719-114">Ist Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d4719-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="d4719-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="d4719-115">-MaxThreshold</span></span>
<span data-ttu-id="d4719-116">Maximaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="d4719-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="d4719-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="d4719-117">-MinThreshold</span></span>
<span data-ttu-id="d4719-118">Mindestschwellenwert.</span><span class="sxs-lookup"><span data-stu-id="d4719-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="d4719-119">-Type</span><span class="sxs-lookup"><span data-stu-id="d4719-119">-Type</span></span>
<span data-ttu-id="d4719-120">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="d4719-120">Rule type.</span></span>

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

### <span data-ttu-id="d4719-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4719-121">CommonParameters</span></span>
<span data-ttu-id="d4719-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4719-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4719-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4719-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4719-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4719-124">INPUTS</span></span>

### <span data-ttu-id="d4719-125">Keine</span><span class="sxs-lookup"><span data-stu-id="d4719-125">None</span></span>

## <span data-ttu-id="d4719-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4719-126">OUTPUTS</span></span>

### <span data-ttu-id="d4719-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="d4719-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="d4719-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d4719-128">NOTES</span></span>

## <span data-ttu-id="d4719-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d4719-129">RELATED LINKS</span></span>
