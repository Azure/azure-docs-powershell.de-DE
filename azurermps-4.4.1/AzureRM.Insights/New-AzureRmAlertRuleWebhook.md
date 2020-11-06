---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504158"
---
# <span data-ttu-id="8b7cf-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="8b7cf-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="8b7cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7cf-103">Erstellt eine Benachrichtigungsregel webhook.</span><span class="sxs-lookup"><span data-stu-id="8b7cf-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b7cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b7cf-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b7cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b7cf-105">DESCRIPTION</span></span>
<span data-ttu-id="8b7cf-106">Das Cmdlet **New-AzureRmAlertRuleWebhook** erstellt eine Warnungsregel webhook.</span><span class="sxs-lookup"><span data-stu-id="8b7cf-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="8b7cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b7cf-107">EXAMPLES</span></span>

### <span data-ttu-id="8b7cf-108">Beispiel 1: Erstellen einer Warnungsregel webhook</span><span class="sxs-lookup"><span data-stu-id="8b7cf-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="8b7cf-109">Mit diesem Befehl wird ein webhook für Warnungsregeln erstellt, indem nur der Dienst-URI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b7cf-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="8b7cf-110">Beispiel 2: Erstellen eines webhooks mit einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8b7cf-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="8b7cf-111">Dieser Befehl erstellt einen Warnungsregel-webhook für contoso.com mit einer Eigenschaft und speichert ihn dann in der $Actual-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b7cf-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="8b7cf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b7cf-112">PARAMETERS</span></span>

### <span data-ttu-id="8b7cf-113">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b7cf-113">-Properties</span></span>
<span data-ttu-id="8b7cf-114">Gibt die Liste der Eigenschaften im Format @ an (Property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="8b7cf-114">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="8b7cf-115">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="8b7cf-115">-ServiceUri</span></span>
<span data-ttu-id="8b7cf-116">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="8b7cf-116">Specifies the service URI.</span></span>

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

### <span data-ttu-id="8b7cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7cf-117">-DefaultProfile</span></span>
<span data-ttu-id="8b7cf-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b7cf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b7cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7cf-119">CommonParameters</span></span>
<span data-ttu-id="8b7cf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b7cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7cf-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b7cf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7cf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b7cf-122">INPUTS</span></span>

## <span data-ttu-id="8b7cf-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b7cf-123">OUTPUTS</span></span>

### <span data-ttu-id="8b7cf-124">Microsoft. Azure. Management. Monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="8b7cf-124">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="8b7cf-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b7cf-125">NOTES</span></span>

## <span data-ttu-id="8b7cf-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b7cf-126">RELATED LINKS</span></span>

[<span data-ttu-id="8b7cf-127">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="8b7cf-127">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="8b7cf-128">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="8b7cf-128">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="8b7cf-129">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="8b7cf-129">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="8b7cf-130">Neu – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="8b7cf-130">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="8b7cf-131">Neu – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="8b7cf-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


