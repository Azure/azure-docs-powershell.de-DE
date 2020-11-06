---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: f1062f1e827e27ff891f5b2797fcda95e60f3427
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499254"
---
# <span data-ttu-id="066b8-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="066b8-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="066b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="066b8-102">SYNOPSIS</span></span>
<span data-ttu-id="066b8-103">Erstellt einen webhook für ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="066b8-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="066b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="066b8-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="066b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="066b8-105">DESCRIPTION</span></span>
<span data-ttu-id="066b8-106">Das Cmdlet **New-AzureRmAutomationWebhook** erstellt einen webhook für ein Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="066b8-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="066b8-107">Achten Sie darauf, die webhook-URL zu speichern, die dieses Cmdlet zurückgibt, da Sie nicht erneut abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="066b8-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="066b8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="066b8-108">EXAMPLES</span></span>

### <span data-ttu-id="066b8-109">Beispiel 1: Erstellen eines webhooks</span><span class="sxs-lookup"><span data-stu-id="066b8-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="066b8-110">Mit diesem Befehl wird ein webhook mit dem Namen Webhook06 für den runbooks namens ContosoRunbook im Automatisierungs Konto mit dem Namen AutomationAccount01 erstellt.</span><span class="sxs-lookup"><span data-stu-id="066b8-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="066b8-111">Der Befehl speichert den webhook in der $Webhook-Variablen.</span><span class="sxs-lookup"><span data-stu-id="066b8-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="066b8-112">Der webhook ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="066b8-112">The webhook is enabled.</span></span>
<span data-ttu-id="066b8-113">Der webhook läuft zum angegebenen Zeitpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="066b8-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="066b8-114">Dieser Befehl bietet keine Werte für webhook-Parameter.</span><span class="sxs-lookup"><span data-stu-id="066b8-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="066b8-115">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="066b8-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="066b8-116">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="066b8-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="066b8-117">Beispiel 2: Erstellen eines webhooks mit Parametern</span><span class="sxs-lookup"><span data-stu-id="066b8-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="066b8-118">Der erste Befehl erstellt ein Wörterbuch mit Parametern und speichert Sie in der $params-Variablen.</span><span class="sxs-lookup"><span data-stu-id="066b8-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="066b8-119">Der zweite Befehl erstellt einen webhook mit dem Namen "Webhook11" für den runbooks namens ContosoRunbook im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="066b8-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="066b8-120">Der Befehl weist dem webhook die Parameter in $params zu.</span><span class="sxs-lookup"><span data-stu-id="066b8-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="066b8-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="066b8-121">PARAMETERS</span></span>

### <span data-ttu-id="066b8-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="066b8-122">-AutomationAccountName</span></span>
<span data-ttu-id="066b8-123">Gibt den Namen eines Automatisierungs Kontos an, in dem mit diesem Cmdlet ein webhook erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="066b8-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="066b8-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="066b8-124">-ExpiryTime</span></span>
<span data-ttu-id="066b8-125">Gibt die Ablaufzeit für den webhook als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="066b8-125">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="066b8-126">Sie können eine Zeichenfolge oder eine **DateTime** angeben, die in einen gültigen **DateTimeOffset** -Datentyp konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="066b8-126">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="066b8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="066b8-127">-Force</span></span>
<span data-ttu-id="066b8-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="066b8-128">ps_force</span></span>

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

### <span data-ttu-id="066b8-129">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="066b8-129">-IsEnabled</span></span>
<span data-ttu-id="066b8-130">Gibt an, ob der webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="066b8-130">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="066b8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="066b8-131">-Name</span></span>
<span data-ttu-id="066b8-132">Gibt einen Namen für den webhook an.</span><span class="sxs-lookup"><span data-stu-id="066b8-132">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="066b8-133">-Parameter</span><span class="sxs-lookup"><span data-stu-id="066b8-133">-Parameters</span></span>
<span data-ttu-id="066b8-134">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="066b8-134">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="066b8-135">Die Schlüssel sind die runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="066b8-135">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="066b8-136">Die Werte sind die runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="066b8-136">The values are the runbook parameter values.</span></span>
<span data-ttu-id="066b8-137">Wenn der runbooks als Antwort auf einen webhook gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="066b8-137">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="066b8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="066b8-138">-ResourceGroupName</span></span>
<span data-ttu-id="066b8-139">Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein webhook erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="066b8-139">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="066b8-140">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="066b8-140">-RunbookName</span></span>
<span data-ttu-id="066b8-141">Gibt den Namen der runbooks an, die dem webhook zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="066b8-141">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="066b8-142">-RunOn</span><span class="sxs-lookup"><span data-stu-id="066b8-142">-RunOn</span></span>
<span data-ttu-id="066b8-143">Optionaler Name des Hybrid-Agents, der die runbooks ausführen soll</span><span class="sxs-lookup"><span data-stu-id="066b8-143">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="066b8-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="066b8-144">-Confirm</span></span>
<span data-ttu-id="066b8-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="066b8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066b8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="066b8-146">-WhatIf</span></span>
<span data-ttu-id="066b8-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="066b8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="066b8-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="066b8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066b8-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066b8-149">-DefaultProfile</span></span>
<span data-ttu-id="066b8-150">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="066b8-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="066b8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066b8-151">CommonParameters</span></span>
<span data-ttu-id="066b8-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066b8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066b8-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="066b8-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066b8-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="066b8-154">INPUTS</span></span>

## <span data-ttu-id="066b8-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="066b8-155">OUTPUTS</span></span>

### <span data-ttu-id="066b8-156">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="066b8-156">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="066b8-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="066b8-157">NOTES</span></span>

## <span data-ttu-id="066b8-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="066b8-158">RELATED LINKS</span></span>

[<span data-ttu-id="066b8-159">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="066b8-159">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="066b8-160">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="066b8-160">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="066b8-161">Satz-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="066b8-161">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


