---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296830"
---
# <span data-ttu-id="632ea-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="632ea-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="632ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="632ea-102">SYNOPSIS</span></span>
<span data-ttu-id="632ea-103">Erstellt einen Warnungsregel-Webhook.</span><span class="sxs-lookup"><span data-stu-id="632ea-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="632ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="632ea-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="632ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="632ea-105">DESCRIPTION</span></span>
<span data-ttu-id="632ea-106">Das **Cmdlet "New-AzAlertRuleWebhook"** erstellt einen Warnungsregel-Webhook.</span><span class="sxs-lookup"><span data-stu-id="632ea-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="632ea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="632ea-107">EXAMPLES</span></span>

### <span data-ttu-id="632ea-108">Beispiel 1: Erstellen eines Warnungsregel-Webhook</span><span class="sxs-lookup"><span data-stu-id="632ea-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="632ea-109">Dieser Befehl erstellt einen Warnungsregel-Webhook, indem nur der Dienst-URI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="632ea-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="632ea-110">Beispiel 2: Erstellen eines Webhook mit einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="632ea-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="632ea-111">Dieser Befehl erstellt einen Warnungsregelwebhook für Contoso.com eine Eigenschaft und speichert sie dann in der $Actual Variable.</span><span class="sxs-lookup"><span data-stu-id="632ea-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="632ea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="632ea-112">PARAMETERS</span></span>

### <span data-ttu-id="632ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632ea-113">-DefaultProfile</span></span>
<span data-ttu-id="632ea-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="632ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="632ea-115">-Property</span><span class="sxs-lookup"><span data-stu-id="632ea-115">-Property</span></span>
<span data-ttu-id="632ea-116">Gibt die Liste der Eigenschaften im Format @(Eigenschaft1 = 'Wert1',....) an.</span><span class="sxs-lookup"><span data-stu-id="632ea-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="632ea-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="632ea-117">-ServiceUri</span></span>
<span data-ttu-id="632ea-118">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="632ea-118">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="632ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632ea-119">CommonParameters</span></span>
<span data-ttu-id="632ea-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632ea-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="632ea-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632ea-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="632ea-122">INPUTS</span></span>

### <span data-ttu-id="632ea-123">System.String</span><span class="sxs-lookup"><span data-stu-id="632ea-123">System.String</span></span>

### <span data-ttu-id="632ea-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="632ea-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="632ea-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="632ea-125">OUTPUTS</span></span>

### <span data-ttu-id="632ea-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="632ea-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="632ea-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="632ea-127">NOTES</span></span>

## <span data-ttu-id="632ea-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="632ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="632ea-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="632ea-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="632ea-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="632ea-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="632ea-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="632ea-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="632ea-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="632ea-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="632ea-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="632ea-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


