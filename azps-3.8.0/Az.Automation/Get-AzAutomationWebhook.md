---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005194"
---
# <span data-ttu-id="c3a2d-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c3a2d-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="c3a2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a2d-103">Ruft webhooks aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="c3a2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a2d-104">SYNTAX</span></span>

### <span data-ttu-id="c3a2d-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3a2d-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3a2d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c3a2d-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3a2d-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c3a2d-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3a2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3a2d-108">DESCRIPTION</span></span>
<span data-ttu-id="c3a2d-109">Das Cmdlet " **Get-AzAutomationWebhook** " ruft webhooks ab.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="c3a2d-110">Wenn Sie bestimmte webhooks abrufen möchten, geben Sie einen webhook-Namen an, oder geben Sie den Namen eines Azure Automation-runbooks an, um die damit verbundenen webhooks zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="c3a2d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3a2d-111">EXAMPLES</span></span>

### <span data-ttu-id="c3a2d-112">Beispiel 1: Abrufen aller webhooks für ein runbooks</span><span class="sxs-lookup"><span data-stu-id="c3a2d-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="c3a2d-113">Dieser Befehl ruft alle webhooks für einen runbooks mit dem Namen Runbook03 im Automatisierungs Konto mit dem Namen AutomationAccount01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c3a2d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3a2d-114">PARAMETERS</span></span>

### <span data-ttu-id="c3a2d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c3a2d-115">-AutomationAccountName</span></span>
<span data-ttu-id="c3a2d-116">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen webhook erhält.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="c3a2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a2d-117">-DefaultProfile</span></span>
<span data-ttu-id="c3a2d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c3a2d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3a2d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c3a2d-119">-Name</span></span>
<span data-ttu-id="c3a2d-120">Gibt den Namen des webhooks an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3a2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3a2d-122">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet webhooks erhält.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="c3a2d-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c3a2d-123">-RunbookName</span></span>
<span data-ttu-id="c3a2d-124">Gibt den Namen einer runbooks an, für die dieses Cmdlet webhooks erhält.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="c3a2d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a2d-125">CommonParameters</span></span>
<span data-ttu-id="c3a2d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a2d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a2d-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a2d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a2d-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3a2d-128">INPUTS</span></span>

### <span data-ttu-id="c3a2d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a2d-129">System.String</span></span>

## <span data-ttu-id="c3a2d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3a2d-130">OUTPUTS</span></span>

### <span data-ttu-id="c3a2d-131">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="c3a2d-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="c3a2d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3a2d-132">NOTES</span></span>

## <span data-ttu-id="c3a2d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3a2d-133">RELATED LINKS</span></span>

[<span data-ttu-id="c3a2d-134">Neu – AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c3a2d-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="c3a2d-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c3a2d-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="c3a2d-136">Satz-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c3a2d-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


