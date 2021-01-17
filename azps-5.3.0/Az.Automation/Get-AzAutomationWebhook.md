---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471331"
---
# <span data-ttu-id="0a54c-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0a54c-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="0a54c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a54c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a54c-103">Ruft Webhooks aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="0a54c-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="0a54c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a54c-104">SYNTAX</span></span>

### <span data-ttu-id="0a54c-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a54c-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a54c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0a54c-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a54c-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="0a54c-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a54c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a54c-108">DESCRIPTION</span></span>
<span data-ttu-id="0a54c-109">Das **Cmdlet "Get-AzAutomationWebhook"** ruft Webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="0a54c-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="0a54c-110">Um bestimmte Webhooks zu erhalten, geben Sie einen Webhooknamen oder den Namen eines Azure Automation-Runbooks an, um die damit verbundenen Webhooks zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0a54c-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="0a54c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a54c-111">EXAMPLES</span></span>

### <span data-ttu-id="0a54c-112">Beispiel 1: Alle Webhooks für ein Runbook erhalten</span><span class="sxs-lookup"><span data-stu-id="0a54c-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0a54c-113">Dieser Befehl ruft alle Webhooks für ein Runbook mit dem Namen "Runbook03" im Automatisierungskonto namens "AutomationAccount01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="0a54c-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0a54c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a54c-114">PARAMETERS</span></span>

### <span data-ttu-id="0a54c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a54c-115">-AutomationAccountName</span></span>
<span data-ttu-id="0a54c-116">Gibt den Namen eines Automatisierungskontos an, bei dem dieses Cmdlet einen Webhook erhält.</span><span class="sxs-lookup"><span data-stu-id="0a54c-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="0a54c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a54c-117">-DefaultProfile</span></span>
<span data-ttu-id="0a54c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0a54c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a54c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0a54c-119">-Name</span></span>
<span data-ttu-id="0a54c-120">Gibt den Namen des Webhook an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0a54c-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a54c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a54c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a54c-122">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Webhooks erhält.</span><span class="sxs-lookup"><span data-stu-id="0a54c-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="0a54c-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="0a54c-123">-RunbookName</span></span>
<span data-ttu-id="0a54c-124">Gibt den Namen eines Runbooks an, für das dieses Cmdlet Webhooks erhält.</span><span class="sxs-lookup"><span data-stu-id="0a54c-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="0a54c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a54c-125">CommonParameters</span></span>
<span data-ttu-id="0a54c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a54c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a54c-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a54c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a54c-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a54c-128">INPUTS</span></span>

### <span data-ttu-id="0a54c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0a54c-129">System.String</span></span>

## <span data-ttu-id="0a54c-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a54c-130">OUTPUTS</span></span>

### <span data-ttu-id="0a54c-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="0a54c-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="0a54c-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a54c-132">NOTES</span></span>

## <span data-ttu-id="0a54c-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a54c-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a54c-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0a54c-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="0a54c-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0a54c-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="0a54c-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0a54c-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


