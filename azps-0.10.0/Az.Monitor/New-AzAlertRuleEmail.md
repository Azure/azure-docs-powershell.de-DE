---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 3738e0d66c7dfb1a1aed56d5cfe8e1679e4e34e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842003"
---
# <span data-ttu-id="ac66e-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="ac66e-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="ac66e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac66e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac66e-103">Erstellt eine e-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="ac66e-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="ac66e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac66e-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac66e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac66e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac66e-106">Das Cmdlet **New-AzAlertRuleEmail** erstellt eine e-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="ac66e-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="ac66e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac66e-107">EXAMPLES</span></span>

### <span data-ttu-id="ac66e-108">Beispiel 1: Erstellen einer Warnungsregel-e-Mail-Aktion für Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="ac66e-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="ac66e-109">Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion erstellt, die den Dienstbesitzern beim Auslösen einer Warnungsregel gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac66e-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="ac66e-110">Beispiel 2: Erstellen einer Warnungsregel-e-Mail-Aktion für nicht-Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="ac66e-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="ac66e-111">Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion für die angegebenen e-Mail-Adressen erstellt, nicht jedoch für die Dienstbesitzer.</span><span class="sxs-lookup"><span data-stu-id="ac66e-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="ac66e-112">Beispiel 3: Erstellen einer e-Mail-Aktion für Warnungsregeln für Dienstbesitzer und nicht Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="ac66e-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="ac66e-113">Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion für die angegebene Adresse und ihre Dienstbesitzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="ac66e-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="ac66e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac66e-114">PARAMETERS</span></span>

### <span data-ttu-id="ac66e-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="ac66e-115">-CustomEmail</span></span>
<span data-ttu-id="ac66e-116">Gibt eine Liste mit durch Kommas getrennten e-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="ac66e-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="ac66e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac66e-117">-DefaultProfile</span></span>
<span data-ttu-id="ac66e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ac66e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac66e-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="ac66e-119">-SendToServiceOwner</span></span>
<span data-ttu-id="ac66e-120">Gibt an, dass dieser Vorgang eine e-Mail-Nachricht an die Dienstbesitzer sendet, wenn die Regel ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="ac66e-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="ac66e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac66e-121">CommonParameters</span></span>
<span data-ttu-id="ac66e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac66e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac66e-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac66e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac66e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac66e-124">INPUTS</span></span>

### <span data-ttu-id="ac66e-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="ac66e-125">System.String[]</span></span>

### <span data-ttu-id="ac66e-126">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ac66e-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac66e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac66e-127">OUTPUTS</span></span>

### <span data-ttu-id="ac66e-128">Microsoft. Azure. Management. Monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="ac66e-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="ac66e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac66e-129">NOTES</span></span>

## <span data-ttu-id="ac66e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac66e-130">RELATED LINKS</span></span>

[<span data-ttu-id="ac66e-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac66e-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="ac66e-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac66e-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="ac66e-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac66e-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="ac66e-134">Neu – AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ac66e-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


