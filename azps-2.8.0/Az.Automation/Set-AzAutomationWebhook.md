---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657930"
---
# <span data-ttu-id="a8567-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a8567-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="a8567-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8567-102">SYNOPSIS</span></span>
<span data-ttu-id="a8567-103">Ändert einen webhook für ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="a8567-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="a8567-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8567-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8567-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8567-105">DESCRIPTION</span></span>
<span data-ttu-id="a8567-106">Das Cmdlet " **Satz-AzAutomationWebhook** " ändert einen webhook für ein Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="a8567-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="a8567-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8567-107">EXAMPLES</span></span>

### <span data-ttu-id="a8567-108">Beispiel 1: Deaktivieren eines webhooks</span><span class="sxs-lookup"><span data-stu-id="a8567-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="a8567-109">Dieser Befehl deaktiviert einen webhook mit dem Namen Webhook01 im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a8567-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="a8567-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8567-110">PARAMETERS</span></span>

### <span data-ttu-id="a8567-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8567-111">-AutomationAccountName</span></span>
<span data-ttu-id="a8567-112">Gibt den Namen eines Automatisierungs Kontos an, in dem mit diesem Cmdlet ein webhook geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a8567-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="a8567-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8567-113">-DefaultProfile</span></span>
<span data-ttu-id="a8567-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a8567-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8567-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a8567-115">-IsEnabled</span></span>
<span data-ttu-id="a8567-116">Gibt an, ob der webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a8567-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="a8567-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a8567-117">-Name</span></span>
<span data-ttu-id="a8567-118">Gibt den Namen des webhooks an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a8567-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a8567-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a8567-119">-Parameters</span></span>
<span data-ttu-id="a8567-120">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="a8567-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="a8567-121">Die Schlüssel sind die runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="a8567-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="a8567-122">Die Werte sind die runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="a8567-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="a8567-123">Wenn der runbooks als Antwort auf einen webhook gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="a8567-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="a8567-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8567-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8567-125">Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein webhook geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a8567-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="a8567-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8567-126">CommonParameters</span></span>
<span data-ttu-id="a8567-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8567-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8567-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8567-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8567-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8567-129">INPUTS</span></span>

### <span data-ttu-id="a8567-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a8567-130">System.String</span></span>

### <span data-ttu-id="a8567-131">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8567-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a8567-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="a8567-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="a8567-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8567-133">OUTPUTS</span></span>

### <span data-ttu-id="a8567-134">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="a8567-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="a8567-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8567-135">NOTES</span></span>

## <span data-ttu-id="a8567-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8567-136">RELATED LINKS</span></span>

[<span data-ttu-id="a8567-137">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a8567-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="a8567-138">Neu – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a8567-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="a8567-139">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a8567-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


