---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176940"
---
# <span data-ttu-id="851f1-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="851f1-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="851f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="851f1-102">SYNOPSIS</span></span>
<span data-ttu-id="851f1-103">Erstellen einer benutzerdefinierten Warnungsregel für eine neue Verweigerungsliste für die Geräte Sicherheitsgruppe (viel Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="851f1-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="851f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="851f1-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="851f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="851f1-105">DESCRIPTION</span></span>
<span data-ttu-id="851f1-106">Das New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject-Cmdlet erstellt eine neue Liste der abgelehnten benutzerdefinierten Warnungsregeln für die Geräte Sicherheitsgruppe in einer viel Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="851f1-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="851f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="851f1-107">EXAMPLES</span></span>

### <span data-ttu-id="851f1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="851f1-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="851f1-109">Erstellen einer benutzerdefinierten Warnungsregel für eine Verweigerungsliste mit Rull Typ "SomeRuleType" und Status auf desable gesetzt</span><span class="sxs-lookup"><span data-stu-id="851f1-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="851f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="851f1-110">PARAMETERS</span></span>

### <span data-ttu-id="851f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851f1-111">-DefaultProfile</span></span>
<span data-ttu-id="851f1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="851f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="851f1-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="851f1-113">-DenylistValue</span></span>
<span data-ttu-id="851f1-114">Listenwerte ablehnen</span><span class="sxs-lookup"><span data-stu-id="851f1-114">Deny list values.</span></span>

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

### <span data-ttu-id="851f1-115">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="851f1-115">-Enabled</span></span>
<span data-ttu-id="851f1-116">Ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="851f1-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="851f1-117">-Typ</span><span class="sxs-lookup"><span data-stu-id="851f1-117">-Type</span></span>
<span data-ttu-id="851f1-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="851f1-118">Rule type.</span></span>

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

### <span data-ttu-id="851f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851f1-119">CommonParameters</span></span>
<span data-ttu-id="851f1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851f1-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="851f1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851f1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="851f1-122">INPUTS</span></span>

### <span data-ttu-id="851f1-123">Keine</span><span class="sxs-lookup"><span data-stu-id="851f1-123">None</span></span>

## <span data-ttu-id="851f1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="851f1-124">OUTPUTS</span></span>

### <span data-ttu-id="851f1-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="851f1-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="851f1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="851f1-126">NOTES</span></span>

## <span data-ttu-id="851f1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="851f1-127">RELATED LINKS</span></span>
