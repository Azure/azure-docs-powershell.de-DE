---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 5f90f80c9ec0ebcb506e1a7f7a506a000224c142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663388"
---
# <span data-ttu-id="6a990-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a990-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="6a990-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a990-102">SYNOPSIS</span></span>
<span data-ttu-id="6a990-103">Entfernt einen webhook aus einem Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="6a990-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a990-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a990-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a990-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a990-105">DESCRIPTION</span></span>
<span data-ttu-id="6a990-106">Das Cmdlet **Remove-AzureRmAutomationWebhook** entfernt einen webhook aus einem Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="6a990-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="6a990-107">Der webhook wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6a990-107">The webhook is deleted.</span></span>

## <span data-ttu-id="6a990-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a990-108">EXAMPLES</span></span>

### <span data-ttu-id="6a990-109">Beispiel 1: Entfernen eines webhooks</span><span class="sxs-lookup"><span data-stu-id="6a990-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="6a990-110">Dieser Befehl entfernt einen webhook mit dem Namen Webhook11 im Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6a990-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="6a990-111">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="6a990-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6a990-112">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6a990-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6a990-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a990-113">PARAMETERS</span></span>

### <span data-ttu-id="6a990-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6a990-114">-AutomationAccountName</span></span>
<span data-ttu-id="6a990-115">Gibt den Namen eines Automatisierungs Kontos an, von dem dieses Cmdlet einen webhook entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a990-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="6a990-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a990-116">-DefaultProfile</span></span>
<span data-ttu-id="6a990-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6a990-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a990-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6a990-118">-Name</span></span>
<span data-ttu-id="6a990-119">Gibt den Namen des webhooks an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a990-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a990-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a990-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a990-121">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet einen webhook entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a990-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="6a990-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a990-122">-Confirm</span></span>
<span data-ttu-id="6a990-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a990-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a990-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a990-124">-WhatIf</span></span>
<span data-ttu-id="6a990-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a990-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a990-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a990-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a990-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a990-127">CommonParameters</span></span>
<span data-ttu-id="6a990-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a990-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a990-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a990-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a990-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a990-130">INPUTS</span></span>

### <span data-ttu-id="6a990-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6a990-131">System.String</span></span>

## <span data-ttu-id="6a990-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a990-132">OUTPUTS</span></span>

### <span data-ttu-id="6a990-133">System. void</span><span class="sxs-lookup"><span data-stu-id="6a990-133">System.Void</span></span>

## <span data-ttu-id="6a990-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a990-134">NOTES</span></span>

## <span data-ttu-id="6a990-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a990-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a990-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a990-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="6a990-137">Neu – AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a990-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="6a990-138">Satz-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6a990-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


