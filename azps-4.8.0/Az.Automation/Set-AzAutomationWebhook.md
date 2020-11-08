---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173926"
---
# <span data-ttu-id="9034f-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9034f-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="9034f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9034f-102">SYNOPSIS</span></span>
<span data-ttu-id="9034f-103">Ändert einen webhook für ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="9034f-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="9034f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9034f-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9034f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9034f-105">DESCRIPTION</span></span>
<span data-ttu-id="9034f-106">Das Cmdlet " **Satz-AzAutomationWebhook** " ändert einen webhook für ein Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="9034f-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="9034f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9034f-107">EXAMPLES</span></span>

### <span data-ttu-id="9034f-108">Beispiel 1: Deaktivieren eines webhooks</span><span class="sxs-lookup"><span data-stu-id="9034f-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="9034f-109">Dieser Befehl deaktiviert einen webhook mit dem Namen Webhook01 im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="9034f-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="9034f-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9034f-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="9034f-111">Mit diesem Befehl wird der Run on-Wert für den webhook festgelegt und die runbooks-Funktion für eine Hybrid Arbeitskraft Gruppe mit dem Namen Windows erzwungen.</span><span class="sxs-lookup"><span data-stu-id="9034f-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="9034f-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9034f-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="9034f-113">Dieser Befehl aktualisiert den Run on-Wert für den webhook und erzwingt, dass die runbooks auf einem Azure runbooks-Worker ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9034f-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="9034f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9034f-114">PARAMETERS</span></span>

### <span data-ttu-id="9034f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9034f-115">-AutomationAccountName</span></span>
<span data-ttu-id="9034f-116">Gibt den Namen eines Automatisierungs Kontos an, in dem mit diesem Cmdlet ein webhook geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9034f-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9034f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9034f-117">-DefaultProfile</span></span>
<span data-ttu-id="9034f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9034f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9034f-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="9034f-119">-IsEnabled</span></span>
<span data-ttu-id="9034f-120">Gibt an, ob der webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9034f-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="9034f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9034f-121">-Name</span></span>
<span data-ttu-id="9034f-122">Gibt den Namen des webhooks an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9034f-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9034f-123">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9034f-123">-Parameters</span></span>
<span data-ttu-id="9034f-124">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="9034f-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="9034f-125">Die Schlüssel sind die runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="9034f-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="9034f-126">Die Werte sind die runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="9034f-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="9034f-127">Wenn der runbooks als Antwort auf einen webhook gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="9034f-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="9034f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9034f-128">-ResourceGroupName</span></span>
<span data-ttu-id="9034f-129">Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein webhook geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9034f-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9034f-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="9034f-130">-RunOn</span></span>
<span data-ttu-id="9034f-131">Optionaler Name des Hybrid-Agents, der die runbooks ausführen soll</span><span class="sxs-lookup"><span data-stu-id="9034f-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="9034f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9034f-132">CommonParameters</span></span>
<span data-ttu-id="9034f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9034f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9034f-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9034f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9034f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9034f-135">INPUTS</span></span>

### <span data-ttu-id="9034f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9034f-136">System.String</span></span>

### <span data-ttu-id="9034f-137">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9034f-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9034f-138">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9034f-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="9034f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9034f-139">OUTPUTS</span></span>

### <span data-ttu-id="9034f-140">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="9034f-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="9034f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9034f-141">NOTES</span></span>

## <span data-ttu-id="9034f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9034f-142">RELATED LINKS</span></span>

[<span data-ttu-id="9034f-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9034f-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="9034f-144">Neu – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9034f-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="9034f-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9034f-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


