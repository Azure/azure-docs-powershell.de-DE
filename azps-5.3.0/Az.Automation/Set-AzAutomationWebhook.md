---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471234"
---
# <span data-ttu-id="0dedf-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0dedf-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="0dedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dedf-102">SYNOPSIS</span></span>
<span data-ttu-id="0dedf-103">Ändert einen Webhook für ein Automatisierungs-Runbook.</span><span class="sxs-lookup"><span data-stu-id="0dedf-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="0dedf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dedf-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dedf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dedf-105">DESCRIPTION</span></span>
<span data-ttu-id="0dedf-106">Das **Cmdlet "Set-AzAutomationWebhook"** ändert einen Webhook für ein Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="0dedf-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="0dedf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0dedf-107">EXAMPLES</span></span>

### <span data-ttu-id="0dedf-108">Beispiel 1: Deaktivieren eines Webhook</span><span class="sxs-lookup"><span data-stu-id="0dedf-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="0dedf-109">Mit diesem Befehl wird ein Webhook namens "Webhook01" im Automatisierungskonto mit dem Namen "AutomationAccount01" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0dedf-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="0dedf-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0dedf-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="0dedf-111">Dieser Befehl legt den Wert für "Run on" für den Webhook fest und erzwingt die Ausführung des Runbooks in einer Hybrid-Worker-Gruppe namens Windows.</span><span class="sxs-lookup"><span data-stu-id="0dedf-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="0dedf-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0dedf-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="0dedf-113">Dieser Befehl aktualisiert den Run on-Wert für den Webhook und erzwingt die Ausführung des Runbook für einen Azure Runbook-Worker.</span><span class="sxs-lookup"><span data-stu-id="0dedf-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="0dedf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dedf-114">PARAMETERS</span></span>

### <span data-ttu-id="0dedf-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0dedf-115">-AutomationAccountName</span></span>
<span data-ttu-id="0dedf-116">Gibt den Namen eines Automatisierungskontos an, bei dem dieses Cmdlet einen Webhook ändert.</span><span class="sxs-lookup"><span data-stu-id="0dedf-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="0dedf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dedf-117">-DefaultProfile</span></span>
<span data-ttu-id="0dedf-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0dedf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dedf-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="0dedf-119">-IsEnabled</span></span>
<span data-ttu-id="0dedf-120">Gibt an, ob der Webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0dedf-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="0dedf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0dedf-121">-Name</span></span>
<span data-ttu-id="0dedf-122">Gibt einen Namen des Webhook an, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="0dedf-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0dedf-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="0dedf-123">-Parameters</span></span>
<span data-ttu-id="0dedf-124">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="0dedf-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="0dedf-125">Bei den Schlüsseln handelt es sich um die Namen der Runbook-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0dedf-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="0dedf-126">Die Werte sind die Runbook-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="0dedf-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="0dedf-127">Wenn das Runbook als Reaktion auf einen Webhook gestartet wird, werden diese Parameter an das Runbook übergeben.</span><span class="sxs-lookup"><span data-stu-id="0dedf-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="0dedf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dedf-128">-ResourceGroupName</span></span>
<span data-ttu-id="0dedf-129">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet einen Webhook ändert.</span><span class="sxs-lookup"><span data-stu-id="0dedf-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="0dedf-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="0dedf-130">-RunOn</span></span>
<span data-ttu-id="0dedf-131">Optionaler Name des Hybrid-Agents, der das Runbook ausführen soll</span><span class="sxs-lookup"><span data-stu-id="0dedf-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="0dedf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dedf-132">CommonParameters</span></span>
<span data-ttu-id="0dedf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dedf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dedf-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dedf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dedf-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0dedf-135">INPUTS</span></span>

### <span data-ttu-id="0dedf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0dedf-136">System.String</span></span>

### <span data-ttu-id="0dedf-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0dedf-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0dedf-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="0dedf-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="0dedf-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0dedf-139">OUTPUTS</span></span>

### <span data-ttu-id="0dedf-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="0dedf-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="0dedf-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0dedf-141">NOTES</span></span>

## <span data-ttu-id="0dedf-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0dedf-142">RELATED LINKS</span></span>

[<span data-ttu-id="0dedf-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0dedf-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="0dedf-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0dedf-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="0dedf-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0dedf-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


