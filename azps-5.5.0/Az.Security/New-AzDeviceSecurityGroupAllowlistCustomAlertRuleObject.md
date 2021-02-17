---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165148"
---
# <span data-ttu-id="43254-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="43254-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="43254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43254-102">SYNOPSIS</span></span>
<span data-ttu-id="43254-103">Erstellen einer neuen benutzerdefinierten Warnungsregel für die Liste "Zulassen" für gerätesicherheitsgruppe (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="43254-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="43254-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43254-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43254-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43254-105">DESCRIPTION</span></span>
<span data-ttu-id="43254-106">Das New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject erstellt eine neue Liste zulässiger benutzerdefinierter Warnungsregeln für die Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="43254-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="43254-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43254-107">EXAMPLES</span></span>

### <span data-ttu-id="43254-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43254-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="43254-109">Erstellen einer neuen benutzerdefinierten Benachrichtigungsliste vom Typ "LocalUserNotAllowed" mit status set to disable</span><span class="sxs-lookup"><span data-stu-id="43254-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="43254-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43254-110">PARAMETERS</span></span>

### <span data-ttu-id="43254-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="43254-111">-AllowlistValue</span></span>
<span data-ttu-id="43254-112">Listenwerte zulassen.</span><span class="sxs-lookup"><span data-stu-id="43254-112">Allow list values.</span></span>

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

### <span data-ttu-id="43254-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43254-113">-DefaultProfile</span></span>
<span data-ttu-id="43254-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43254-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43254-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="43254-115">-Enabled</span></span>
<span data-ttu-id="43254-116">Ist Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="43254-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="43254-117">-Type</span><span class="sxs-lookup"><span data-stu-id="43254-117">-Type</span></span>
<span data-ttu-id="43254-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="43254-118">Rule type.</span></span>

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

### <span data-ttu-id="43254-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43254-119">CommonParameters</span></span>
<span data-ttu-id="43254-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43254-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43254-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43254-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43254-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43254-122">INPUTS</span></span>

### <span data-ttu-id="43254-123">Keine</span><span class="sxs-lookup"><span data-stu-id="43254-123">None</span></span>

## <span data-ttu-id="43254-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43254-124">OUTPUTS</span></span>

### <span data-ttu-id="43254-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="43254-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="43254-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="43254-126">NOTES</span></span>

## <span data-ttu-id="43254-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="43254-127">RELATED LINKS</span></span>
