---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03a1ca397fb67daf4b7cf73700f54d6642dd9f2d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399361"
---
# <span data-ttu-id="172fe-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="172fe-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="172fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="172fe-102">SYNOPSIS</span></span>
<span data-ttu-id="172fe-103">Erstellt einen Warnungsregel-Webhook.</span><span class="sxs-lookup"><span data-stu-id="172fe-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="172fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="172fe-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="172fe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="172fe-105">DESCRIPTION</span></span>
<span data-ttu-id="172fe-106">Das **Cmdlet "New-AzAlertRuleWebhook"** erstellt einen Warnungsregel-Webhook.</span><span class="sxs-lookup"><span data-stu-id="172fe-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="172fe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="172fe-107">EXAMPLES</span></span>

### <span data-ttu-id="172fe-108">Beispiel 1: Erstellen eines Webhook einer Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="172fe-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="172fe-109">Dieser Befehl erstellt einen Warnungsregel-Webhook, indem nur der Dienst-URI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="172fe-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="172fe-110">Beispiel 2: Erstellen eines Webhook mit einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="172fe-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="172fe-111">Dieser Befehl erstellt einen Warnungsregelwebhook für Contoso.com eine Eigenschaft und speichert sie dann in der $Actual Variable.</span><span class="sxs-lookup"><span data-stu-id="172fe-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="172fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="172fe-112">PARAMETERS</span></span>

### <span data-ttu-id="172fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172fe-113">-DefaultProfile</span></span>
<span data-ttu-id="172fe-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="172fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="172fe-115">-Property</span><span class="sxs-lookup"><span data-stu-id="172fe-115">-Property</span></span>
<span data-ttu-id="172fe-116">Gibt die Liste der Eigenschaften im Format @(Eigenschaft1 = 'Wert1',....) an.</span><span class="sxs-lookup"><span data-stu-id="172fe-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="172fe-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="172fe-117">-ServiceUri</span></span>
<span data-ttu-id="172fe-118">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="172fe-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="172fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172fe-119">CommonParameters</span></span>
<span data-ttu-id="172fe-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172fe-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="172fe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172fe-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="172fe-122">INPUTS</span></span>

### <span data-ttu-id="172fe-123">System.String</span><span class="sxs-lookup"><span data-stu-id="172fe-123">System.String</span></span>

### <span data-ttu-id="172fe-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="172fe-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="172fe-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="172fe-125">OUTPUTS</span></span>

### <span data-ttu-id="172fe-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="172fe-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="172fe-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="172fe-127">NOTES</span></span>

## <span data-ttu-id="172fe-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="172fe-128">RELATED LINKS</span></span>


[<span data-ttu-id="172fe-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="172fe-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="172fe-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="172fe-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="172fe-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="172fe-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="172fe-132">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="172fe-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


