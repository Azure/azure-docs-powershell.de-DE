---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471259"
---
# <span data-ttu-id="c1254-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c1254-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="c1254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1254-102">SYNOPSIS</span></span>
<span data-ttu-id="c1254-103">Entfernt einen Webhook aus einem Automatisierungs-Runbook.</span><span class="sxs-lookup"><span data-stu-id="c1254-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="c1254-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1254-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1254-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1254-105">DESCRIPTION</span></span>
<span data-ttu-id="c1254-106">Das **Cmdlet "Remove-AzAutomationWebhook"** entfernt einen Webhook aus einem Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="c1254-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="c1254-107">Der Webhook wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c1254-107">The webhook is deleted.</span></span>

## <span data-ttu-id="c1254-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1254-108">EXAMPLES</span></span>

### <span data-ttu-id="c1254-109">Beispiel 1: Entfernen eines Webhook</span><span class="sxs-lookup"><span data-stu-id="c1254-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="c1254-110">Mit diesem Befehl wird ein Webhook namens "Webhook11" im Automatisierungskonto namens "AutomationAccount01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c1254-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="c1254-111">Der Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="c1254-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c1254-112">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c1254-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c1254-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1254-113">PARAMETERS</span></span>

### <span data-ttu-id="c1254-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c1254-114">-AutomationAccountName</span></span>
<span data-ttu-id="c1254-115">Gibt den Namen eines Automatisierungskontos an, aus dem dieses Cmdlet einen Webhook entfernt.</span><span class="sxs-lookup"><span data-stu-id="c1254-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="c1254-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1254-116">-DefaultProfile</span></span>
<span data-ttu-id="c1254-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c1254-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1254-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c1254-118">-Name</span></span>
<span data-ttu-id="c1254-119">Gibt den Namen des Webhook an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="c1254-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1254-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1254-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1254-121">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet einen Webhook entfernt.</span><span class="sxs-lookup"><span data-stu-id="c1254-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="c1254-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1254-122">-Confirm</span></span>
<span data-ttu-id="c1254-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1254-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1254-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c1254-124">-WhatIf</span></span>
<span data-ttu-id="c1254-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1254-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1254-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1254-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1254-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1254-127">CommonParameters</span></span>
<span data-ttu-id="c1254-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1254-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1254-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1254-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1254-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1254-130">INPUTS</span></span>

### <span data-ttu-id="c1254-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c1254-131">System.String</span></span>

## <span data-ttu-id="c1254-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1254-132">OUTPUTS</span></span>

### <span data-ttu-id="c1254-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="c1254-133">System.Void</span></span>

## <span data-ttu-id="c1254-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1254-134">NOTES</span></span>

## <span data-ttu-id="c1254-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1254-135">RELATED LINKS</span></span>

[<span data-ttu-id="c1254-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c1254-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="c1254-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c1254-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="c1254-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c1254-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


