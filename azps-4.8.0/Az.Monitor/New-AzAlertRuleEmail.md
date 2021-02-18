---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415919"
---
# <span data-ttu-id="3d197-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="3d197-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="3d197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d197-102">SYNOPSIS</span></span>
<span data-ttu-id="3d197-103">Erstellt eine E-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="3d197-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="3d197-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d197-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d197-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d197-105">DESCRIPTION</span></span>
<span data-ttu-id="3d197-106">Das **Cmdlet "New-AzAlertRuleEmail"** erstellt eine E-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="3d197-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="3d197-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d197-107">EXAMPLES</span></span>

### <span data-ttu-id="3d197-108">Beispiel 1: Erstellen einer E-Mail-Aktion einer Warnungsregel für Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="3d197-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="3d197-109">Mit diesem Befehl wird eine E-Mail-Aktion für eine Warnungsregel erstellt, die an die Dienstbesitzer gesendet wird, wenn eine Warnungsregel ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3d197-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="3d197-110">Beispiel 2: Erstellen einer E-Mail-Aktion einer Warnungsregel für Nicht-Dienst-Besitzer</span><span class="sxs-lookup"><span data-stu-id="3d197-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="3d197-111">Mit diesem Befehl wird eine E-Mail-Aktion der Warnungsregel für die angegebenen E-Mail-Adressen erstellt, jedoch nicht für die Dienstbesitzer.</span><span class="sxs-lookup"><span data-stu-id="3d197-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="3d197-112">Beispiel 3: Erstellen einer E-Mail-Aktion mit einer Warnungsregel für Dienstbesitzer und Nicht-Dienst-Besitzer</span><span class="sxs-lookup"><span data-stu-id="3d197-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="3d197-113">Mit diesem Befehl wird eine E-Mail-Aktion für eine Warnungsregel für die angegebene Adresse und für die Dienstbesitzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d197-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="3d197-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d197-114">PARAMETERS</span></span>

### <span data-ttu-id="3d197-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="3d197-115">-CustomEmail</span></span>
<span data-ttu-id="3d197-116">Gibt eine Liste von durch Kommas getrennten E-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="3d197-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d197-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d197-117">-DefaultProfile</span></span>
<span data-ttu-id="3d197-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3d197-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d197-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="3d197-119">-SendToServiceOwner</span></span>
<span data-ttu-id="3d197-120">Gibt an, dass durch diesen Vorgang eine E-Mail an die Dienstbesitzer gesendet wird, wenn die Regel ausgibt.</span><span class="sxs-lookup"><span data-stu-id="3d197-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d197-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d197-121">CommonParameters</span></span>
<span data-ttu-id="3d197-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d197-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d197-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d197-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d197-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d197-124">INPUTS</span></span>

### <span data-ttu-id="3d197-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3d197-125">System.String[]</span></span>

### <span data-ttu-id="3d197-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d197-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d197-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d197-127">OUTPUTS</span></span>

### <span data-ttu-id="3d197-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="3d197-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="3d197-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3d197-129">NOTES</span></span>

## <span data-ttu-id="3d197-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3d197-130">RELATED LINKS</span></span>


[<span data-ttu-id="3d197-131">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="3d197-131">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="3d197-132">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="3d197-132">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="3d197-133">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="3d197-133">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


