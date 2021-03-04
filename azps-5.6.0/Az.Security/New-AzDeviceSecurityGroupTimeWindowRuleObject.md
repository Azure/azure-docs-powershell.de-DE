---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: fb068adcf7a7775106714dce9d91d23ae5e2c240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934696"
---
# <span data-ttu-id="6efc3-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="6efc3-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="6efc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6efc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6efc3-103">Erstellen einer neuen Zeitfensterregel für gerätesicherheitsgruppe (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="6efc3-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="6efc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6efc3-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6efc3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6efc3-105">DESCRIPTION</span></span>
<span data-ttu-id="6efc3-106">Das New-AzDeviceSecurityGroupTimeWindowRuleObject-Cmdlet erstellt eine neue Liste der Zeitfensterbenachrichtigungsregeln für die Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="6efc3-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="6efc3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6efc3-107">EXAMPLES</span></span>

### <span data-ttu-id="6efc3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6efc3-108">Example 1</span></span>
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

<span data-ttu-id="6efc3-109">Erstellen einer neuen Zeitfensterregel vom Typ "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="6efc3-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="6efc3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6efc3-110">PARAMETERS</span></span>

### <span data-ttu-id="6efc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efc3-111">-DefaultProfile</span></span>
<span data-ttu-id="6efc3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6efc3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6efc3-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6efc3-113">-Enabled</span></span>
<span data-ttu-id="6efc3-114">Ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6efc3-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="6efc3-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="6efc3-115">-MaxThreshold</span></span>
<span data-ttu-id="6efc3-116">Maximaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="6efc3-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="6efc3-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="6efc3-117">-MinThreshold</span></span>
<span data-ttu-id="6efc3-118">Mindestschwellenwert.</span><span class="sxs-lookup"><span data-stu-id="6efc3-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="6efc3-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="6efc3-119">-TimeWindowSize</span></span>
<span data-ttu-id="6efc3-120">Größe des Zeitfensters.</span><span class="sxs-lookup"><span data-stu-id="6efc3-120">Time window size.</span></span>

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

### <span data-ttu-id="6efc3-121">-Type</span><span class="sxs-lookup"><span data-stu-id="6efc3-121">-Type</span></span>
<span data-ttu-id="6efc3-122">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="6efc3-122">Rule type.</span></span>

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

### <span data-ttu-id="6efc3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efc3-123">CommonParameters</span></span>
<span data-ttu-id="6efc3-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efc3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efc3-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6efc3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efc3-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6efc3-126">INPUTS</span></span>

### <span data-ttu-id="6efc3-127">Keine</span><span class="sxs-lookup"><span data-stu-id="6efc3-127">None</span></span>

## <span data-ttu-id="6efc3-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6efc3-128">OUTPUTS</span></span>

### <span data-ttu-id="6efc3-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="6efc3-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="6efc3-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6efc3-130">NOTES</span></span>

## <span data-ttu-id="6efc3-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6efc3-131">RELATED LINKS</span></span>
