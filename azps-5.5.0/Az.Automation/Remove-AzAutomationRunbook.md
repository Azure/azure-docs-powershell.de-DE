---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171660"
---
# <span data-ttu-id="cc860-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="cc860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc860-102">SYNOPSIS</span></span>
<span data-ttu-id="cc860-103">Entfernt ein Runbook.</span><span class="sxs-lookup"><span data-stu-id="cc860-103">Removes a runbook.</span></span>

## <span data-ttu-id="cc860-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc860-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc860-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc860-105">DESCRIPTION</span></span>
<span data-ttu-id="cc860-106">Das **Cmdlet "Remove-AzAutomationRunbook"** entfernt ein Runbook aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="cc860-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="cc860-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc860-107">EXAMPLES</span></span>

### <span data-ttu-id="cc860-108">Beispiel 1: Entfernen eines Runbooks</span><span class="sxs-lookup"><span data-stu-id="cc860-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cc860-109">Mit diesem Befehl wird das Runbook "Runbook03" im Azure -Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc860-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cc860-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc860-110">PARAMETERS</span></span>

### <span data-ttu-id="cc860-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc860-111">-AutomationAccountName</span></span>
<span data-ttu-id="cc860-112">Gibt den Namen des Automatisierungskontos an, in dem dieses Cmdlet ein Runbook entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc860-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="cc860-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc860-113">-DefaultProfile</span></span>
<span data-ttu-id="cc860-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cc860-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc860-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc860-115">-Force</span></span>
<span data-ttu-id="cc860-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="cc860-116">ps_force</span></span>

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

### <span data-ttu-id="cc860-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cc860-117">-Name</span></span>
<span data-ttu-id="cc860-118">Gibt den Namen des Runbooks an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="cc860-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cc860-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc860-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc860-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Runbook veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cc860-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="cc860-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc860-121">-Confirm</span></span>
<span data-ttu-id="cc860-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc860-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc860-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cc860-123">-WhatIf</span></span>
<span data-ttu-id="cc860-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc860-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc860-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc860-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc860-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc860-126">CommonParameters</span></span>
<span data-ttu-id="cc860-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc860-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc860-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc860-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc860-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc860-129">INPUTS</span></span>

### <span data-ttu-id="cc860-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cc860-130">System.String</span></span>

## <span data-ttu-id="cc860-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc860-131">OUTPUTS</span></span>

### <span data-ttu-id="cc860-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="cc860-132">System.Void</span></span>

## <span data-ttu-id="cc860-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc860-133">NOTES</span></span>

## <span data-ttu-id="cc860-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc860-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc860-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="cc860-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="cc860-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="cc860-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="cc860-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="cc860-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="cc860-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="cc860-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cc860-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


