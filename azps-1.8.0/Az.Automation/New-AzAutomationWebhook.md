---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 94bc498caa5052df5aa9a9e7724ecb87d253d9f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661758"
---
# <span data-ttu-id="70da0-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="70da0-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="70da0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70da0-102">SYNOPSIS</span></span>
<span data-ttu-id="70da0-103">Erstellt einen webhook für ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="70da0-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="70da0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70da0-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70da0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70da0-105">DESCRIPTION</span></span>
<span data-ttu-id="70da0-106">Das Cmdlet **New-AzAutomationWebhook** erstellt einen webhook für ein Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="70da0-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="70da0-107">Achten Sie darauf, die webhook-URL zu speichern, die dieses Cmdlet zurückgibt, da Sie nicht erneut abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="70da0-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="70da0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70da0-108">EXAMPLES</span></span>

### <span data-ttu-id="70da0-109">Beispiel 1: Erstellen eines webhooks</span><span class="sxs-lookup"><span data-stu-id="70da0-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="70da0-110">Mit diesem Befehl wird ein webhook mit dem Namen Webhook06 für den runbooks namens ContosoRunbook im Automatisierungs Konto mit dem Namen AutomationAccount01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="70da0-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="70da0-111">Der Befehl speichert den webhook in der $Webhook-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70da0-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="70da0-112">Der webhook ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="70da0-112">The webhook is enabled.</span></span>
<span data-ttu-id="70da0-113">Der webhook läuft zum angegebenen Zeitpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="70da0-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="70da0-114">Dieser Befehl bietet keine Werte für webhook-Parameter.</span><span class="sxs-lookup"><span data-stu-id="70da0-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="70da0-115">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="70da0-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="70da0-116">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="70da0-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="70da0-117">Beispiel 2: Erstellen eines webhooks mit Parametern</span><span class="sxs-lookup"><span data-stu-id="70da0-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="70da0-118">Der erste Befehl erstellt ein Wörterbuch mit Parametern und speichert Sie in der $params-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70da0-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="70da0-119">Der zweite Befehl erstellt einen webhook mit dem Namen "Webhook11" für den runbooks namens ContosoRunbook im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="70da0-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="70da0-120">Der Befehl weist dem webhook die Parameter in $params zu.</span><span class="sxs-lookup"><span data-stu-id="70da0-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="70da0-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="70da0-121">PARAMETERS</span></span>

### <span data-ttu-id="70da0-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70da0-122">-AutomationAccountName</span></span>
<span data-ttu-id="70da0-123">Gibt den Namen eines Automatisierungs Kontos an, in dem mit diesem Cmdlet ein webhook erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="70da0-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="70da0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70da0-124">-DefaultProfile</span></span>
<span data-ttu-id="70da0-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="70da0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70da0-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="70da0-126">-ExpiryTime</span></span>
<span data-ttu-id="70da0-127">Gibt die Ablaufzeit für den webhook als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="70da0-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="70da0-128">Sie können eine Zeichenfolge oder eine **DateTime** angeben, die in einen gültigen **DateTimeOffset** -Datentyp konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="70da0-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="70da0-129">-Force</span><span class="sxs-lookup"><span data-stu-id="70da0-129">-Force</span></span>
<span data-ttu-id="70da0-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="70da0-130">ps_force</span></span>

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

### <span data-ttu-id="70da0-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="70da0-131">-IsEnabled</span></span>
<span data-ttu-id="70da0-132">Gibt an, ob der webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="70da0-132">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="70da0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="70da0-133">-Name</span></span>
<span data-ttu-id="70da0-134">Gibt einen Namen für den webhook an.</span><span class="sxs-lookup"><span data-stu-id="70da0-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="70da0-135">-Parameter</span><span class="sxs-lookup"><span data-stu-id="70da0-135">-Parameters</span></span>
<span data-ttu-id="70da0-136">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="70da0-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="70da0-137">Die Schlüssel sind die runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="70da0-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="70da0-138">Die Werte sind die runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="70da0-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="70da0-139">Wenn der runbooks als Antwort auf einen webhook gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="70da0-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="70da0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70da0-140">-ResourceGroupName</span></span>
<span data-ttu-id="70da0-141">Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein webhook erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="70da0-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="70da0-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="70da0-142">-RunbookName</span></span>
<span data-ttu-id="70da0-143">Gibt den Namen der runbooks an, die dem webhook zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70da0-143">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="70da0-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="70da0-144">-RunOn</span></span>
<span data-ttu-id="70da0-145">Optionaler Name der Hybrid Arbeitskraft Gruppe, die die runbooks ausführen soll</span><span class="sxs-lookup"><span data-stu-id="70da0-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="70da0-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70da0-146">-Confirm</span></span>
<span data-ttu-id="70da0-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70da0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70da0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70da0-148">-WhatIf</span></span>
<span data-ttu-id="70da0-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70da0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70da0-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70da0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70da0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70da0-151">CommonParameters</span></span>
<span data-ttu-id="70da0-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70da0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70da0-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70da0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70da0-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70da0-154">INPUTS</span></span>

### <span data-ttu-id="70da0-155">System. String</span><span class="sxs-lookup"><span data-stu-id="70da0-155">System.String</span></span>

### <span data-ttu-id="70da0-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70da0-156">System.Boolean</span></span>

### <span data-ttu-id="70da0-157">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="70da0-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="70da0-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70da0-158">OUTPUTS</span></span>

### <span data-ttu-id="70da0-159">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="70da0-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="70da0-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="70da0-160">NOTES</span></span>

## <span data-ttu-id="70da0-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70da0-161">RELATED LINKS</span></span>

[<span data-ttu-id="70da0-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="70da0-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="70da0-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="70da0-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="70da0-164">Satz-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="70da0-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


