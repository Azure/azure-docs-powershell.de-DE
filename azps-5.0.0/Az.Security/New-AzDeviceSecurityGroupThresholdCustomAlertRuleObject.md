---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178219"
---
# <span data-ttu-id="3cd9c-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="3cd9c-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="3cd9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cd9c-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd9c-103">Neue Schwelle für benutzerdefinierte Warnungsregel für Geräte Sicherheitsgruppe erstellen (viel Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="3cd9c-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="3cd9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cd9c-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cd9c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cd9c-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd9c-106">Das New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject-Cmdlet erstellt eine neue Liste mit benutzerdefinierten Schwellenwert-Warnungsregeln für die Geräte Sicherheitsgruppe in der Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="3cd9c-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="3cd9c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cd9c-107">EXAMPLES</span></span>

### <span data-ttu-id="3cd9c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3cd9c-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="3cd9c-109">Erstellen einer benutzerdefinierten Warnungsregel für den Schwellenwert vom Typ "SomeRuleType" mit aktiviertem Status für Ant-Werte für minimale und maximale Schwelle</span><span class="sxs-lookup"><span data-stu-id="3cd9c-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="3cd9c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cd9c-110">PARAMETERS</span></span>

### <span data-ttu-id="3cd9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd9c-111">-DefaultProfile</span></span>
<span data-ttu-id="3cd9c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cd9c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd9c-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="3cd9c-113">-Enabled</span></span>
<span data-ttu-id="3cd9c-114">Ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3cd9c-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="3cd9c-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="3cd9c-115">-MaxThreshold</span></span>
<span data-ttu-id="3cd9c-116">Maximaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="3cd9c-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="3cd9c-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="3cd9c-117">-MinThreshold</span></span>
<span data-ttu-id="3cd9c-118">Minimaler Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="3cd9c-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="3cd9c-119">-Typ</span><span class="sxs-lookup"><span data-stu-id="3cd9c-119">-Type</span></span>
<span data-ttu-id="3cd9c-120">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="3cd9c-120">Rule type.</span></span>

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

### <span data-ttu-id="3cd9c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd9c-121">CommonParameters</span></span>
<span data-ttu-id="3cd9c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd9c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd9c-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cd9c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd9c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cd9c-124">INPUTS</span></span>

### <span data-ttu-id="3cd9c-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3cd9c-125">None</span></span>

## <span data-ttu-id="3cd9c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cd9c-126">OUTPUTS</span></span>

### <span data-ttu-id="3cd9c-127">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="3cd9c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="3cd9c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cd9c-128">NOTES</span></span>

## <span data-ttu-id="3cd9c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cd9c-129">RELATED LINKS</span></span>
