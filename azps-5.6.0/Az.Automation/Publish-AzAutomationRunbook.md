---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: fa10c44186de06de758e4f7878bb7c8da61c4d6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945388"
---
# <span data-ttu-id="b9132-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="b9132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9132-102">SYNOPSIS</span></span>
<span data-ttu-id="b9132-103">Veröffentlicht ein Runbook.</span><span class="sxs-lookup"><span data-stu-id="b9132-103">Publishes a runbook.</span></span>

## <span data-ttu-id="b9132-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9132-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9132-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9132-105">DESCRIPTION</span></span>
<span data-ttu-id="b9132-106">Das **Cmdlet Publish-AzAutomationRunbook** veröffentlicht ein Runbook für die Verwendung in der Produktionsumgebung von Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b9132-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="b9132-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9132-107">EXAMPLES</span></span>

### <span data-ttu-id="b9132-108">Beispiel 1: Veröffentlichen eines Runbooks</span><span class="sxs-lookup"><span data-stu-id="b9132-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b9132-109">Mit diesem Befehl wird das Runbook "Runbk01" im Azure Automation-Konto namens Contoso17 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b9132-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b9132-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b9132-110">PARAMETERS</span></span>

### <span data-ttu-id="b9132-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b9132-111">-AutomationAccountName</span></span>
<span data-ttu-id="b9132-112">Gibt den Namen des Automatisierungskontos an, in dem dieses Cmdlet ein Runbook veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b9132-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="b9132-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9132-113">-DefaultProfile</span></span>
<span data-ttu-id="b9132-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b9132-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9132-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b9132-115">-Name</span></span>
<span data-ttu-id="b9132-116">Gibt den Namen des Runbooks an, das dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b9132-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9132-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9132-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9132-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Runbook veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b9132-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="b9132-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9132-119">CommonParameters</span></span>
<span data-ttu-id="b9132-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9132-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9132-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9132-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9132-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9132-122">INPUTS</span></span>

### <span data-ttu-id="b9132-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b9132-123">System.String</span></span>

## <span data-ttu-id="b9132-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9132-124">OUTPUTS</span></span>

### <span data-ttu-id="b9132-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="b9132-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="b9132-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b9132-126">NOTES</span></span>

## <span data-ttu-id="b9132-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b9132-127">RELATED LINKS</span></span>

[<span data-ttu-id="b9132-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="b9132-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="b9132-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="b9132-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b9132-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b9132-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="b9132-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="b9132-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b9132-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


