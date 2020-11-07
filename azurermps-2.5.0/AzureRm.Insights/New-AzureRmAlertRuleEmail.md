---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
ms.openlocfilehash: 20134cc0f2eef927361439fb431bc4ab9308a9a1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850827"
---
# <span data-ttu-id="89732-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="89732-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="89732-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89732-102">SYNOPSIS</span></span>
<span data-ttu-id="89732-103">Erstellt eine e-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="89732-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89732-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89732-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89732-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89732-105">DESCRIPTION</span></span>
<span data-ttu-id="89732-106">Das Cmdlet **New-AzureRmAlertRuleEmail** erstellt eine e-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="89732-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="89732-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89732-107">EXAMPLES</span></span>

### <span data-ttu-id="89732-108">Beispiel 1: Erstellen einer Warnungsregel-e-Mail-Aktion für Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="89732-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="89732-109">Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion erstellt, die den Dienstbesitzern beim Auslösen einer Warnungsregel gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89732-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="89732-110">Beispiel 2: Erstellen einer Warnungsregel-e-Mail-Aktion für nicht-Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="89732-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="89732-111">Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion für die angegebenen e-Mail-Adressen erstellt, nicht jedoch für die Dienstbesitzer.</span><span class="sxs-lookup"><span data-stu-id="89732-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="89732-112">Beispiel 3: Erstellen einer e-Mail-Aktion für Warnungsregeln für Dienstbesitzer und nicht Dienstbesitzer</span><span class="sxs-lookup"><span data-stu-id="89732-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="89732-113">Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion für die angegebene Adresse und ihre Dienstbesitzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="89732-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="89732-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="89732-114">PARAMETERS</span></span>

### <span data-ttu-id="89732-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="89732-115">-CustomEmail</span></span>
<span data-ttu-id="89732-116">Gibt eine Liste mit durch Kommas getrennten e-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="89732-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="89732-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89732-117">-DefaultProfile</span></span>
<span data-ttu-id="89732-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="89732-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89732-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="89732-119">-SendToServiceOwner</span></span>
<span data-ttu-id="89732-120">Gibt an, dass dieser Vorgang eine e-Mail-Nachricht an die Dienstbesitzer sendet, wenn die Regel ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="89732-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="89732-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89732-121">CommonParameters</span></span>
<span data-ttu-id="89732-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89732-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89732-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89732-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89732-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89732-124">INPUTS</span></span>

### <span data-ttu-id="89732-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="89732-125">System.String[]</span></span>

### <span data-ttu-id="89732-126">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="89732-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89732-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89732-127">OUTPUTS</span></span>

### <span data-ttu-id="89732-128">Microsoft. Azure. Management. Monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="89732-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="89732-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="89732-129">NOTES</span></span>

## <span data-ttu-id="89732-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89732-130">RELATED LINKS</span></span>



[<span data-ttu-id="89732-131">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="89732-131">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="89732-132">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="89732-132">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="89732-133">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="89732-133">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


