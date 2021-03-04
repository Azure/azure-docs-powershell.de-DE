---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 481105ca99a2bdc797a7a539f54ab69fd9935ebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932560"
---
# <span data-ttu-id="da00c-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="da00c-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="da00c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da00c-102">SYNOPSIS</span></span>
<span data-ttu-id="da00c-103">Erstellt eine E-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="da00c-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="da00c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da00c-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da00c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da00c-105">DESCRIPTION</span></span>
<span data-ttu-id="da00c-106">Das **Cmdlet New-AzAlertRuleEmail** erstellt eine E-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="da00c-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="da00c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da00c-107">EXAMPLES</span></span>

### <span data-ttu-id="da00c-108">Beispiel 1: Erstellen einer E-Mail-Aktion einer Warnungsregel für Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="da00c-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="da00c-109">Mit diesem Befehl wird eine Benachrichtigungsregel-E-Mail-Aktion erstellt, die an die Dienstbesitzer gesendet wird, wenn eine Warnungsregel ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="da00c-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="da00c-110">Beispiel 2: Erstellen einer E-Mail-Aktion einer Warnungsregel für Nicht-Dienst-Besitzer</span><span class="sxs-lookup"><span data-stu-id="da00c-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="da00c-111">Mit diesem Befehl wird eine Benachrichtigungsregel-E-Mail-Aktion für die angegebenen E-Mail-Adressen erstellt, jedoch nicht für die Dienstbesitzer.</span><span class="sxs-lookup"><span data-stu-id="da00c-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="da00c-112">Beispiel 3: Erstellen einer E-Mail-Aktion einer Warnungsregel für Dienstbesitzer und Nicht-Dienst-Besitzer</span><span class="sxs-lookup"><span data-stu-id="da00c-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="da00c-113">Mit diesem Befehl wird eine Benachrichtigungsregel-E-Mail-Aktion für die angegebene Adresse und für die Dienstbesitzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="da00c-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="da00c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="da00c-114">PARAMETERS</span></span>

### <span data-ttu-id="da00c-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="da00c-115">-CustomEmail</span></span>
<span data-ttu-id="da00c-116">Gibt eine Liste von durch Kommas getrennten E-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="da00c-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="da00c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da00c-117">-DefaultProfile</span></span>
<span data-ttu-id="da00c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="da00c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da00c-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="da00c-119">-SendToServiceOwner</span></span>
<span data-ttu-id="da00c-120">Gibt an, dass dieser Vorgang beim Löschen der Regel eine E-Mail an die Dienstbesitzer sendet.</span><span class="sxs-lookup"><span data-stu-id="da00c-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="da00c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da00c-121">CommonParameters</span></span>
<span data-ttu-id="da00c-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da00c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da00c-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da00c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da00c-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da00c-124">INPUTS</span></span>

### <span data-ttu-id="da00c-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="da00c-125">System.String[]</span></span>

### <span data-ttu-id="da00c-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da00c-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="da00c-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da00c-127">OUTPUTS</span></span>

### <span data-ttu-id="da00c-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="da00c-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="da00c-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="da00c-129">NOTES</span></span>

## <span data-ttu-id="da00c-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="da00c-130">RELATED LINKS</span></span>

[<span data-ttu-id="da00c-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="da00c-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="da00c-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="da00c-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="da00c-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="da00c-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="da00c-134">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="da00c-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


