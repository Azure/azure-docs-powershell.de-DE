---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373426"
---
# <span data-ttu-id="805f6-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="805f6-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="805f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="805f6-102">SYNOPSIS</span></span>
<span data-ttu-id="805f6-103">Erstellt einen Webhook für ein Automatisierungs-Runbook.</span><span class="sxs-lookup"><span data-stu-id="805f6-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="805f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="805f6-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="805f6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="805f6-105">DESCRIPTION</span></span>
<span data-ttu-id="805f6-106">Das **Cmdlet "New-AzAutomationWebhook"** erstellt einen Webhook für ein Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="805f6-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="805f6-107">Achten Sie darauf, die Webhook-URL zu speichern, die dieses Cmdlet zurückgibt, da sie nicht erneut abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="805f6-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="805f6-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="805f6-108">EXAMPLES</span></span>

### <span data-ttu-id="805f6-109">Beispiel 1: Erstellen eines Webhook</span><span class="sxs-lookup"><span data-stu-id="805f6-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="805f6-110">Mit diesem Befehl wird ein Webhook namens Webhook06 für das Runbook "ContosoRunbook" im Automatisierungskonto namens "AutomationAccount01" erstellt.</span><span class="sxs-lookup"><span data-stu-id="805f6-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="805f6-111">Der Befehl speichert den Webhook in der $Webhook Variable.</span><span class="sxs-lookup"><span data-stu-id="805f6-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="805f6-112">Der Webhook ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="805f6-112">The webhook is enabled.</span></span>
<span data-ttu-id="805f6-113">Der Webhook läuft zum angegebenen Zeitpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="805f6-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="805f6-114">Dieser Befehl enthält keine Werte für Webhook-Parameter.</span><span class="sxs-lookup"><span data-stu-id="805f6-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="805f6-115">Dieser Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="805f6-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="805f6-116">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="805f6-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="805f6-117">Beispiel 2: Erstellen eines Webhook mit Parametern</span><span class="sxs-lookup"><span data-stu-id="805f6-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="805f6-118">Der erste Befehl erstellt ein Parameterwörterbuch und speichert sie in der $Params Variable.</span><span class="sxs-lookup"><span data-stu-id="805f6-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="805f6-119">Mit dem zweiten Befehl wird ein Webhook namens Webhook11 für das Runbook "ContosoRunbook" im Automatisierungskonto namens "AutomationAccount01" erstellt.</span><span class="sxs-lookup"><span data-stu-id="805f6-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="805f6-120">Der Befehl weist dem Webhook die $Params in "Webhook" zu.</span><span class="sxs-lookup"><span data-stu-id="805f6-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="805f6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="805f6-121">PARAMETERS</span></span>

### <span data-ttu-id="805f6-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="805f6-122">-AutomationAccountName</span></span>
<span data-ttu-id="805f6-123">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen Webhook erstellt.</span><span class="sxs-lookup"><span data-stu-id="805f6-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="805f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="805f6-124">-DefaultProfile</span></span>
<span data-ttu-id="805f6-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="805f6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="805f6-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="805f6-126">-ExpiryTime</span></span>
<span data-ttu-id="805f6-127">Gibt die Ablaufzeit für den Webhook als **"DateTimeOffset"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="805f6-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="805f6-128">Sie können eine Zeichenfolge oder einen **DateTime-Wert** angeben, der in ein gültiges **DateTimeOffset konvertiert werden kann.**</span><span class="sxs-lookup"><span data-stu-id="805f6-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805f6-129">-Force</span><span class="sxs-lookup"><span data-stu-id="805f6-129">-Force</span></span>
<span data-ttu-id="805f6-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="805f6-130">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805f6-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="805f6-131">-IsEnabled</span></span>
<span data-ttu-id="805f6-132">Gibt an, ob der Webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="805f6-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805f6-133">-Name</span><span class="sxs-lookup"><span data-stu-id="805f6-133">-Name</span></span>
<span data-ttu-id="805f6-134">Gibt einen Namen für den Webhook an.</span><span class="sxs-lookup"><span data-stu-id="805f6-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="805f6-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="805f6-135">-Parameters</span></span>
<span data-ttu-id="805f6-136">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="805f6-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="805f6-137">Bei den Schlüsseln handelt es sich um die Namen der Runbook-Parameter.</span><span class="sxs-lookup"><span data-stu-id="805f6-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="805f6-138">Die Werte sind die Runbook-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="805f6-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="805f6-139">Wenn das Runbook als Reaktion auf einen Webhook gestartet wird, werden diese Parameter an das Runbook übergeben.</span><span class="sxs-lookup"><span data-stu-id="805f6-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805f6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="805f6-140">-ResourceGroupName</span></span>
<span data-ttu-id="805f6-141">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet einen Webhook erstellt.</span><span class="sxs-lookup"><span data-stu-id="805f6-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="805f6-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="805f6-142">-RunbookName</span></span>
<span data-ttu-id="805f6-143">Gibt den Namen des Runbooks an, das dem Webhook zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="805f6-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805f6-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="805f6-144">-RunOn</span></span>
<span data-ttu-id="805f6-145">Optionaler Name der Hybrid-Workergruppe, die das Runbook ausführen soll</span><span class="sxs-lookup"><span data-stu-id="805f6-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="805f6-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="805f6-146">-Confirm</span></span>
<span data-ttu-id="805f6-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="805f6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="805f6-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="805f6-148">-WhatIf</span></span>
<span data-ttu-id="805f6-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="805f6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="805f6-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="805f6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="805f6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805f6-151">CommonParameters</span></span>
<span data-ttu-id="805f6-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="805f6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805f6-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805f6-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805f6-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="805f6-154">INPUTS</span></span>

### <span data-ttu-id="805f6-155">System.String</span><span class="sxs-lookup"><span data-stu-id="805f6-155">System.String</span></span>

### <span data-ttu-id="805f6-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="805f6-156">System.Boolean</span></span>

### <span data-ttu-id="805f6-157">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="805f6-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="805f6-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="805f6-158">OUTPUTS</span></span>

### <span data-ttu-id="805f6-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="805f6-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="805f6-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="805f6-160">NOTES</span></span>

## <span data-ttu-id="805f6-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="805f6-161">RELATED LINKS</span></span>

[<span data-ttu-id="805f6-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="805f6-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="805f6-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="805f6-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="805f6-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="805f6-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


