---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373231"
---
# <span data-ttu-id="01222-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="01222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01222-102">SYNOPSIS</span></span>
<span data-ttu-id="01222-103">Entfernt ein Runbook.</span><span class="sxs-lookup"><span data-stu-id="01222-103">Removes a runbook.</span></span>

## <span data-ttu-id="01222-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01222-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01222-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01222-105">DESCRIPTION</span></span>
<span data-ttu-id="01222-106">Das **Cmdlet "Remove-AzAutomationRunbook"** entfernt ein Runbook aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="01222-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="01222-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01222-107">EXAMPLES</span></span>

### <span data-ttu-id="01222-108">Beispiel 1: Entfernen eines Runbooks</span><span class="sxs-lookup"><span data-stu-id="01222-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="01222-109">Mit diesem Befehl wird das Runbook "Runbook03" im Azure -Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="01222-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="01222-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01222-110">PARAMETERS</span></span>

### <span data-ttu-id="01222-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01222-111">-AutomationAccountName</span></span>
<span data-ttu-id="01222-112">Gibt den Namen des Automatisierungskontos an, in dem dieses Cmdlet ein Runbook entfernt.</span><span class="sxs-lookup"><span data-stu-id="01222-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="01222-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01222-113">-DefaultProfile</span></span>
<span data-ttu-id="01222-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="01222-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01222-115">-Force</span><span class="sxs-lookup"><span data-stu-id="01222-115">-Force</span></span>
<span data-ttu-id="01222-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="01222-116">ps_force</span></span>

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

### <span data-ttu-id="01222-117">-Name</span><span class="sxs-lookup"><span data-stu-id="01222-117">-Name</span></span>
<span data-ttu-id="01222-118">Gibt den Namen des Runbooks an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="01222-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="01222-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01222-119">-ResourceGroupName</span></span>
<span data-ttu-id="01222-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Runbook veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="01222-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="01222-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01222-121">-Confirm</span></span>
<span data-ttu-id="01222-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01222-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01222-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01222-123">-WhatIf</span></span>
<span data-ttu-id="01222-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01222-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01222-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01222-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01222-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01222-126">CommonParameters</span></span>
<span data-ttu-id="01222-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01222-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01222-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01222-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01222-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01222-129">INPUTS</span></span>

### <span data-ttu-id="01222-130">System.String</span><span class="sxs-lookup"><span data-stu-id="01222-130">System.String</span></span>

## <span data-ttu-id="01222-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01222-131">OUTPUTS</span></span>

### <span data-ttu-id="01222-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="01222-132">System.Void</span></span>

## <span data-ttu-id="01222-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01222-133">NOTES</span></span>

## <span data-ttu-id="01222-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01222-134">RELATED LINKS</span></span>

[<span data-ttu-id="01222-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="01222-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="01222-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="01222-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="01222-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="01222-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="01222-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="01222-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="01222-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


