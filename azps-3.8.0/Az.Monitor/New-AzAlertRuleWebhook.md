---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995815"
---
# <span data-ttu-id="80fb4-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="80fb4-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="80fb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="80fb4-103">Erstellt eine Benachrichtigungsregel webhook.</span><span class="sxs-lookup"><span data-stu-id="80fb4-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="80fb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80fb4-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80fb4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80fb4-105">DESCRIPTION</span></span>
<span data-ttu-id="80fb4-106">Das Cmdlet **New-AzAlertRuleWebhook** erstellt eine Warnungsregel webhook.</span><span class="sxs-lookup"><span data-stu-id="80fb4-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="80fb4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80fb4-107">EXAMPLES</span></span>

### <span data-ttu-id="80fb4-108">Beispiel 1: Erstellen einer Warnungsregel webhook</span><span class="sxs-lookup"><span data-stu-id="80fb4-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="80fb4-109">Mit diesem Befehl wird ein webhook für Warnungsregeln erstellt, indem nur der Dienst-URI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="80fb4-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="80fb4-110">Beispiel 2: Erstellen eines webhooks mit einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="80fb4-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="80fb4-111">Dieser Befehl erstellt einen Warnungsregel-webhook für contoso.com mit einer Eigenschaft und speichert ihn dann in der $Actual-Variablen.</span><span class="sxs-lookup"><span data-stu-id="80fb4-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="80fb4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="80fb4-112">PARAMETERS</span></span>

### <span data-ttu-id="80fb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fb4-113">-DefaultProfile</span></span>
<span data-ttu-id="80fb4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80fb4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80fb4-115">-Property</span><span class="sxs-lookup"><span data-stu-id="80fb4-115">-Property</span></span>
<span data-ttu-id="80fb4-116">Gibt die Liste der Eigenschaften im Format @ an (Property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="80fb4-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="80fb4-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="80fb4-117">-ServiceUri</span></span>
<span data-ttu-id="80fb4-118">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="80fb4-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="80fb4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fb4-119">CommonParameters</span></span>
<span data-ttu-id="80fb4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80fb4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fb4-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80fb4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fb4-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80fb4-122">INPUTS</span></span>

### <span data-ttu-id="80fb4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="80fb4-123">System.String</span></span>

### <span data-ttu-id="80fb4-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="80fb4-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80fb4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80fb4-125">OUTPUTS</span></span>

### <span data-ttu-id="80fb4-126">Microsoft. Azure. Management. Monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="80fb4-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="80fb4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="80fb4-127">NOTES</span></span>

## <span data-ttu-id="80fb4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80fb4-128">RELATED LINKS</span></span>

[<span data-ttu-id="80fb4-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="80fb4-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="80fb4-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="80fb4-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="80fb4-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="80fb4-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="80fb4-132">Neu – AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="80fb4-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="80fb4-133">Neu – AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="80fb4-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


