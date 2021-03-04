---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 93c370eaefa83c5e1be4692cb41ea0793b8f4681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947536"
---
# <span data-ttu-id="824b3-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="824b3-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="824b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824b3-102">SYNOPSIS</span></span>
<span data-ttu-id="824b3-103">Entfernt einen Webhook aus einem Automatisierungslaufbuch.</span><span class="sxs-lookup"><span data-stu-id="824b3-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="824b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="824b3-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824b3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="824b3-105">DESCRIPTION</span></span>
<span data-ttu-id="824b3-106">Das **Cmdlet Remove-AzAutomationWebhook** entfernt einen Webhook aus einem Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="824b3-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="824b3-107">Der Webhook wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="824b3-107">The webhook is deleted.</span></span>

## <span data-ttu-id="824b3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="824b3-108">EXAMPLES</span></span>

### <span data-ttu-id="824b3-109">Beispiel 1: Entfernen eines Webhooks</span><span class="sxs-lookup"><span data-stu-id="824b3-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="824b3-110">Mit diesem Befehl wird ein Webhook namens Webhook11 im Automatisierungskonto mit dem Namen AutomationAccount01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="824b3-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="824b3-111">Der Befehl gibt den Parameter *"Erzwingen"* an.</span><span class="sxs-lookup"><span data-stu-id="824b3-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="824b3-112">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="824b3-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="824b3-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="824b3-113">PARAMETERS</span></span>

### <span data-ttu-id="824b3-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="824b3-114">-AutomationAccountName</span></span>
<span data-ttu-id="824b3-115">Gibt den Namen eines Automatisierungskontos an, aus dem dieses Cmdlet einen Webhook entfernt.</span><span class="sxs-lookup"><span data-stu-id="824b3-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824b3-116">-DefaultProfile</span></span>
<span data-ttu-id="824b3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="824b3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="824b3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="824b3-118">-Name</span></span>
<span data-ttu-id="824b3-119">Gibt den Namen des Webhooks an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="824b3-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824b3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824b3-120">-ResourceGroupName</span></span>
<span data-ttu-id="824b3-121">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet einen Webhook entfernt.</span><span class="sxs-lookup"><span data-stu-id="824b3-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="824b3-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="824b3-122">-Confirm</span></span>
<span data-ttu-id="824b3-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="824b3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824b3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824b3-124">-WhatIf</span></span>
<span data-ttu-id="824b3-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="824b3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824b3-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="824b3-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824b3-127">CommonParameters</span></span>
<span data-ttu-id="824b3-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824b3-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824b3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824b3-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="824b3-130">INPUTS</span></span>

### <span data-ttu-id="824b3-131">System.String</span><span class="sxs-lookup"><span data-stu-id="824b3-131">System.String</span></span>

## <span data-ttu-id="824b3-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="824b3-132">OUTPUTS</span></span>

### <span data-ttu-id="824b3-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="824b3-133">System.Void</span></span>

## <span data-ttu-id="824b3-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="824b3-134">NOTES</span></span>

## <span data-ttu-id="824b3-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="824b3-135">RELATED LINKS</span></span>

[<span data-ttu-id="824b3-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="824b3-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="824b3-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="824b3-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="824b3-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="824b3-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


