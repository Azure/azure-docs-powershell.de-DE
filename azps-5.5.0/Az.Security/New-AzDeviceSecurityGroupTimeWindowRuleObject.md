---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165137"
---
# <span data-ttu-id="85659-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="85659-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="85659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85659-102">SYNOPSIS</span></span>
<span data-ttu-id="85659-103">Erstellen einer neuen Zeitfensterregel für die Gerätesicherheitsgruppe (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="85659-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="85659-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85659-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85659-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85659-105">DESCRIPTION</span></span>
<span data-ttu-id="85659-106">Das New-AzDeviceSecurityGroupTimeWindowRuleObject erstellt eine neue Liste von Warnungsregeln für Zeitfenster für die Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="85659-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="85659-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85659-107">EXAMPLES</span></span>

### <span data-ttu-id="85659-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85659-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="85659-109">Erstellen einer neuen Zeitfensterregel vom Typ "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="85659-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="85659-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85659-110">PARAMETERS</span></span>

### <span data-ttu-id="85659-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85659-111">-DefaultProfile</span></span>
<span data-ttu-id="85659-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85659-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85659-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="85659-113">-Enabled</span></span>
<span data-ttu-id="85659-114">Ist Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85659-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="85659-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="85659-115">-MaxThreshold</span></span>
<span data-ttu-id="85659-116">Maximaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="85659-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="85659-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="85659-117">-MinThreshold</span></span>
<span data-ttu-id="85659-118">Mindestschwellenwert.</span><span class="sxs-lookup"><span data-stu-id="85659-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="85659-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="85659-119">-TimeWindowSize</span></span>
<span data-ttu-id="85659-120">Zeitfenstergröße.</span><span class="sxs-lookup"><span data-stu-id="85659-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85659-121">-Type</span><span class="sxs-lookup"><span data-stu-id="85659-121">-Type</span></span>
<span data-ttu-id="85659-122">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="85659-122">Rule type.</span></span>

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

### <span data-ttu-id="85659-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85659-123">CommonParameters</span></span>
<span data-ttu-id="85659-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85659-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85659-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85659-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85659-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85659-126">INPUTS</span></span>

### <span data-ttu-id="85659-127">Keine</span><span class="sxs-lookup"><span data-stu-id="85659-127">None</span></span>

## <span data-ttu-id="85659-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85659-128">OUTPUTS</span></span>

### <span data-ttu-id="85659-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="85659-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="85659-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85659-130">NOTES</span></span>

## <span data-ttu-id="85659-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85659-131">RELATED LINKS</span></span>
