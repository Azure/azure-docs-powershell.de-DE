---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176401"
---
# <span data-ttu-id="8a850-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="8a850-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="8a850-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a850-102">SYNOPSIS</span></span>
<span data-ttu-id="8a850-103">Erstellen einer neuen Zeitfenster Regel für die Geräte Sicherheitsgruppe (viel Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="8a850-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="8a850-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a850-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a850-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a850-105">DESCRIPTION</span></span>
<span data-ttu-id="8a850-106">Das New-AzDeviceSecurityGroupTimeWindowRuleObject-Cmdlet erstellt eine neue Liste mit Warnungsregeln für das Zeitfenster in der Sicherheitslösung "Gerätesicherheit".</span><span class="sxs-lookup"><span data-stu-id="8a850-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="8a850-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a850-107">EXAMPLES</span></span>

### <span data-ttu-id="8a850-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a850-108">Example 1</span></span>
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

<span data-ttu-id="8a850-109">Erstellen einer neuen Zeitfenster Regel vom Typ "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="8a850-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="8a850-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a850-110">PARAMETERS</span></span>

### <span data-ttu-id="8a850-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a850-111">-DefaultProfile</span></span>
<span data-ttu-id="8a850-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a850-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a850-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="8a850-113">-Enabled</span></span>
<span data-ttu-id="8a850-114">Ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a850-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="8a850-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="8a850-115">-MaxThreshold</span></span>
<span data-ttu-id="8a850-116">Maximaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="8a850-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="8a850-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="8a850-117">-MinThreshold</span></span>
<span data-ttu-id="8a850-118">Minimaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="8a850-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="8a850-119">-Windows-Fenster</span><span class="sxs-lookup"><span data-stu-id="8a850-119">-TimeWindowSize</span></span>
<span data-ttu-id="8a850-120">Zeitfenster Größe</span><span class="sxs-lookup"><span data-stu-id="8a850-120">Time window size.</span></span>

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

### <span data-ttu-id="8a850-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="8a850-121">-Type</span></span>
<span data-ttu-id="8a850-122">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="8a850-122">Rule type.</span></span>

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

### <span data-ttu-id="8a850-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a850-123">CommonParameters</span></span>
<span data-ttu-id="8a850-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a850-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a850-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a850-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a850-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a850-126">INPUTS</span></span>

### <span data-ttu-id="8a850-127">Keine</span><span class="sxs-lookup"><span data-stu-id="8a850-127">None</span></span>

## <span data-ttu-id="8a850-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a850-128">OUTPUTS</span></span>

### <span data-ttu-id="8a850-129">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="8a850-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="8a850-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a850-130">NOTES</span></span>

## <span data-ttu-id="8a850-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a850-131">RELATED LINKS</span></span>
