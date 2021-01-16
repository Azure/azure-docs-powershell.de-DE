---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296447"
---
# <span data-ttu-id="ad9ee-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="ad9ee-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="ad9ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9ee-103">Erstellen einer neuen benutzerdefinierten Warnungsregel für die Liste "Zulassen" für gerätesicherheitsgruppe (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="ad9ee-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="ad9ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad9ee-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad9ee-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad9ee-105">DESCRIPTION</span></span>
<span data-ttu-id="ad9ee-106">Das New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject erstellt eine neue Liste zulässiger benutzerdefinierter Warnungsregeln für die Gerätesicherheitsgruppe in der IoT-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="ad9ee-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="ad9ee-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ad9ee-107">EXAMPLES</span></span>

### <span data-ttu-id="ad9ee-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad9ee-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="ad9ee-109">Erstellen einer neuen benutzerdefinierten Benachrichtigungsliste vom Typ "LocalUserNotAllowed" mit status set to disable</span><span class="sxs-lookup"><span data-stu-id="ad9ee-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="ad9ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad9ee-110">PARAMETERS</span></span>

### <span data-ttu-id="ad9ee-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="ad9ee-111">-AllowlistValue</span></span>
<span data-ttu-id="ad9ee-112">Listenwerte zulassen.</span><span class="sxs-lookup"><span data-stu-id="ad9ee-112">Allow list values.</span></span>

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

### <span data-ttu-id="ad9ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9ee-113">-DefaultProfile</span></span>
<span data-ttu-id="ad9ee-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad9ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad9ee-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="ad9ee-115">-Enabled</span></span>
<span data-ttu-id="ad9ee-116">Ist Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ad9ee-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="ad9ee-117">-Type</span><span class="sxs-lookup"><span data-stu-id="ad9ee-117">-Type</span></span>
<span data-ttu-id="ad9ee-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="ad9ee-118">Rule type.</span></span>

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

### <span data-ttu-id="ad9ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9ee-119">CommonParameters</span></span>
<span data-ttu-id="ad9ee-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad9ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9ee-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad9ee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9ee-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ad9ee-122">INPUTS</span></span>

### <span data-ttu-id="ad9ee-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ad9ee-123">None</span></span>

## <span data-ttu-id="ad9ee-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ad9ee-124">OUTPUTS</span></span>

### <span data-ttu-id="ad9ee-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="ad9ee-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="ad9ee-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ad9ee-126">NOTES</span></span>

## <span data-ttu-id="ad9ee-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ad9ee-127">RELATED LINKS</span></span>
