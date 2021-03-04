---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 200cc0b6312940606bb4e75f576c60928a84b33f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947515"
---
# <span data-ttu-id="e764b-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e764b-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="e764b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e764b-102">SYNOPSIS</span></span>
<span data-ttu-id="e764b-103">Ändert einen Webhook für ein Automatisierungslaufbuch.</span><span class="sxs-lookup"><span data-stu-id="e764b-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="e764b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e764b-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e764b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e764b-105">DESCRIPTION</span></span>
<span data-ttu-id="e764b-106">Das **Cmdlet Set-AzAutomationWebhook** ändert einen Webhook für ein Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="e764b-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="e764b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e764b-107">EXAMPLES</span></span>

### <span data-ttu-id="e764b-108">Beispiel 1: Deaktivieren eines Webhooks</span><span class="sxs-lookup"><span data-stu-id="e764b-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="e764b-109">Mit diesem Befehl wird ein Webhook namens Webhook01 im Automatisierungskonto mit dem Namen AutomationAccount01 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e764b-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="e764b-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e764b-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="e764b-111">Dieser Befehl legt den Wert für "Ausführen auf" für den Webhook fest und erzwingt die Ausführung des Runbooks in einer Hybrid worker-Gruppe namens Windows.</span><span class="sxs-lookup"><span data-stu-id="e764b-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="e764b-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e764b-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="e764b-113">Dieser Befehl aktualisiert den Wert für die Ausführung für den Webhook und erzwingt die Ausführung des Runbooks für einen Azure Runbook-Worker.</span><span class="sxs-lookup"><span data-stu-id="e764b-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="e764b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e764b-114">PARAMETERS</span></span>

### <span data-ttu-id="e764b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e764b-115">-AutomationAccountName</span></span>
<span data-ttu-id="e764b-116">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen Webhook ändert.</span><span class="sxs-lookup"><span data-stu-id="e764b-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e764b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e764b-117">-DefaultProfile</span></span>
<span data-ttu-id="e764b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e764b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e764b-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e764b-119">-IsEnabled</span></span>
<span data-ttu-id="e764b-120">Gibt an, ob der Webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e764b-120">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e764b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e764b-121">-Name</span></span>
<span data-ttu-id="e764b-122">Gibt einen Namen des Webhooks an, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="e764b-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e764b-123">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e764b-123">-Parameters</span></span>
<span data-ttu-id="e764b-124">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="e764b-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e764b-125">Die Schlüssel sind die Namen der Runbookparameter.</span><span class="sxs-lookup"><span data-stu-id="e764b-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e764b-126">Die Werte sind die Parameterwerte für das Runbook.</span><span class="sxs-lookup"><span data-stu-id="e764b-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e764b-127">Wenn das Runbook als Reaktion auf einen Webhook gestartet wird, werden diese Parameter an das Runbook übergeben.</span><span class="sxs-lookup"><span data-stu-id="e764b-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e764b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e764b-128">-ResourceGroupName</span></span>
<span data-ttu-id="e764b-129">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet einen Webhook ändert.</span><span class="sxs-lookup"><span data-stu-id="e764b-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e764b-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="e764b-130">-RunOn</span></span>
<span data-ttu-id="e764b-131">Optionaler Name des Hybrid-Agents, der das Runbook ausführen soll</span><span class="sxs-lookup"><span data-stu-id="e764b-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e764b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e764b-132">CommonParameters</span></span>
<span data-ttu-id="e764b-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e764b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e764b-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e764b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e764b-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e764b-135">INPUTS</span></span>

### <span data-ttu-id="e764b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e764b-136">System.String</span></span>

### <span data-ttu-id="e764b-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e764b-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e764b-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="e764b-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="e764b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e764b-139">OUTPUTS</span></span>

### <span data-ttu-id="e764b-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="e764b-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e764b-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e764b-141">NOTES</span></span>

## <span data-ttu-id="e764b-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e764b-142">RELATED LINKS</span></span>

[<span data-ttu-id="e764b-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e764b-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="e764b-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e764b-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="e764b-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e764b-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


