---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479973"
---
# <span data-ttu-id="31c62-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="31c62-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="31c62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31c62-102">SYNOPSIS</span></span>
<span data-ttu-id="31c62-103">Ändert einen webhook für ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="31c62-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31c62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31c62-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31c62-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31c62-105">DESCRIPTION</span></span>
<span data-ttu-id="31c62-106">Das Cmdlet " **Satz-AzureRmAutomationWebhook** " ändert einen webhook für ein Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="31c62-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="31c62-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31c62-107">EXAMPLES</span></span>

### <span data-ttu-id="31c62-108">Beispiel 1: Deaktivieren eines webhooks</span><span class="sxs-lookup"><span data-stu-id="31c62-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="31c62-109">Dieser Befehl deaktiviert einen webhook mit dem Namen Webhook01 im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="31c62-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="31c62-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="31c62-110">PARAMETERS</span></span>

### <span data-ttu-id="31c62-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="31c62-111">-AutomationAccountName</span></span>
<span data-ttu-id="31c62-112">Gibt den Namen eines Automatisierungs Kontos an, in dem mit diesem Cmdlet ein webhook geändert wird.</span><span class="sxs-lookup"><span data-stu-id="31c62-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="31c62-113">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="31c62-113">-IsEnabled</span></span>
<span data-ttu-id="31c62-114">Gibt an, ob der webhook aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="31c62-114">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="31c62-115">-Name</span><span class="sxs-lookup"><span data-stu-id="31c62-115">-Name</span></span>
<span data-ttu-id="31c62-116">Gibt den Namen des webhooks an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="31c62-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31c62-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="31c62-117">-Parameters</span></span>
<span data-ttu-id="31c62-118">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="31c62-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="31c62-119">Die Schlüssel sind die runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="31c62-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="31c62-120">Die Werte sind die runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="31c62-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="31c62-121">Wenn der runbooks als Antwort auf einen webhook gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="31c62-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="31c62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c62-122">-ResourceGroupName</span></span>
<span data-ttu-id="31c62-123">Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein webhook geändert wird.</span><span class="sxs-lookup"><span data-stu-id="31c62-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="31c62-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c62-124">-DefaultProfile</span></span>
<span data-ttu-id="31c62-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31c62-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31c62-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c62-126">CommonParameters</span></span>
<span data-ttu-id="31c62-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c62-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c62-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c62-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c62-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31c62-129">INPUTS</span></span>

## <span data-ttu-id="31c62-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31c62-130">OUTPUTS</span></span>

### <span data-ttu-id="31c62-131">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="31c62-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="31c62-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="31c62-132">NOTES</span></span>

## <span data-ttu-id="31c62-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31c62-133">RELATED LINKS</span></span>

[<span data-ttu-id="31c62-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="31c62-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="31c62-135">Neu – AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="31c62-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="31c62-136">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="31c62-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


