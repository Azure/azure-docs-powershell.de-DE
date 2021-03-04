---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 00125a7ad3d74d3e710b782d0be7fdb20004ef4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949672"
---
# <span data-ttu-id="87548-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="87548-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="87548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87548-102">SYNOPSIS</span></span>
<span data-ttu-id="87548-103">Ruft Webhooks aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="87548-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="87548-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87548-104">SYNTAX</span></span>

### <span data-ttu-id="87548-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="87548-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87548-106">ByName</span><span class="sxs-lookup"><span data-stu-id="87548-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87548-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="87548-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87548-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87548-108">DESCRIPTION</span></span>
<span data-ttu-id="87548-109">Das **Get-AzAutomationWebhook-Cmdlet** ruft Webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="87548-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="87548-110">Um bestimmte Webhooks zu erhalten, geben Sie einen Webhooknamen an, oder geben Sie den Namen eines Azure Automation-Runbooks an, um die webhooks mit diesem Zulauf zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="87548-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span><br>
<span data-ttu-id="87548-111">**Hinweis:** Der WebhookUri wird aus Sicherheitsgründen als leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87548-111">**Note:** The WebhookUri is returned as empty string due to security concerns.</span></span> <span data-ttu-id="87548-112">Speichern Sie unbedingt die Webhook-URL, die **das Cmdlet New-AzAutomationWebhook** zurückgibt, da sie nicht mithilfe von **Get-AzAutomationWebhook** abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="87548-112">Please make sure to save the webhook URL that **New-AzAutomationWebhook** cmdlet returns, because it cannot be retrieved by using **Get-AzAutomationWebhook**.</span></span>

## <span data-ttu-id="87548-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87548-113">EXAMPLES</span></span>

### <span data-ttu-id="87548-114">Beispiel 1: Alle Webhooks für ein Runbook herunterladen</span><span class="sxs-lookup"><span data-stu-id="87548-114">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="87548-115">Dieser Befehl ruft alle Webhooks für ein Runbook namens Runbook03 im Automatisierungskonto mit dem Namen AutomationAccount01 in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="87548-115">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="87548-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87548-116">PARAMETERS</span></span>

### <span data-ttu-id="87548-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87548-117">-AutomationAccountName</span></span>
<span data-ttu-id="87548-118">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen Webhook erhält.</span><span class="sxs-lookup"><span data-stu-id="87548-118">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="87548-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87548-119">-DefaultProfile</span></span>
<span data-ttu-id="87548-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="87548-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87548-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87548-121">-Name</span></span>
<span data-ttu-id="87548-122">Gibt den Namen des Webhooks an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="87548-122">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87548-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87548-123">-ResourceGroupName</span></span>
<span data-ttu-id="87548-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Webhooks erhält.</span><span class="sxs-lookup"><span data-stu-id="87548-124">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="87548-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="87548-125">-RunbookName</span></span>
<span data-ttu-id="87548-126">Gibt den Namen eines Runbooks an, für das dieses Cmdlet Webhooks erhält.</span><span class="sxs-lookup"><span data-stu-id="87548-126">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87548-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87548-127">CommonParameters</span></span>
<span data-ttu-id="87548-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87548-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87548-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87548-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87548-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87548-130">INPUTS</span></span>

### <span data-ttu-id="87548-131">System.String</span><span class="sxs-lookup"><span data-stu-id="87548-131">System.String</span></span>

## <span data-ttu-id="87548-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87548-132">OUTPUTS</span></span>

### <span data-ttu-id="87548-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="87548-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="87548-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87548-134">NOTES</span></span>

## <span data-ttu-id="87548-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87548-135">RELATED LINKS</span></span>

[<span data-ttu-id="87548-136">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="87548-136">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="87548-137">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="87548-137">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="87548-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="87548-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


