---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180153"
---
# <span data-ttu-id="ba6bf-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="ba6bf-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="ba6bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6bf-103">Erstellen einer benutzerdefinierten Warnungsregel für eine neue Zulassungsliste für die Geräte Sicherheitsgruppe (viel Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="ba6bf-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="ba6bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba6bf-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba6bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ba6bf-106">Das New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject-Cmdlet erstellt eine neue Liste zulässiger benutzerdefinierter Warnungsregeln für die Geräte Sicherheitsgruppe in der Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="ba6bf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba6bf-107">EXAMPLES</span></span>

### <span data-ttu-id="ba6bf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba6bf-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="ba6bf-109">Erstellen einer benutzerdefinierten Warnungs Rull vom Typ "LocalUserNotAllowed" mit dem Status "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="ba6bf-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="ba6bf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba6bf-110">PARAMETERS</span></span>

### <span data-ttu-id="ba6bf-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="ba6bf-111">-AllowlistValue</span></span>
<span data-ttu-id="ba6bf-112">Listenwerte zulassen.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-112">Allow list values.</span></span>

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

### <span data-ttu-id="ba6bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6bf-113">-DefaultProfile</span></span>
<span data-ttu-id="ba6bf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba6bf-115">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ba6bf-115">-Enabled</span></span>
<span data-ttu-id="ba6bf-116">Ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="ba6bf-117">-Typ</span><span class="sxs-lookup"><span data-stu-id="ba6bf-117">-Type</span></span>
<span data-ttu-id="ba6bf-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-118">Rule type.</span></span>

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

### <span data-ttu-id="ba6bf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6bf-119">CommonParameters</span></span>
<span data-ttu-id="ba6bf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6bf-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba6bf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6bf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba6bf-122">INPUTS</span></span>

### <span data-ttu-id="ba6bf-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ba6bf-123">None</span></span>

## <span data-ttu-id="ba6bf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba6bf-124">OUTPUTS</span></span>

### <span data-ttu-id="ba6bf-125">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="ba6bf-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="ba6bf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba6bf-126">NOTES</span></span>

## <span data-ttu-id="ba6bf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba6bf-127">RELATED LINKS</span></span>
