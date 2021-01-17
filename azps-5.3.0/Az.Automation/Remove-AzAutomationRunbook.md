---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471274"
---
# <span data-ttu-id="27095-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="27095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27095-102">SYNOPSIS</span></span>
<span data-ttu-id="27095-103">Entfernt ein Runbook.</span><span class="sxs-lookup"><span data-stu-id="27095-103">Removes a runbook.</span></span>

## <span data-ttu-id="27095-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27095-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27095-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27095-105">DESCRIPTION</span></span>
<span data-ttu-id="27095-106">Das **Cmdlet "Remove-AzAutomationRunbook"** entfernt ein Runbook aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="27095-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="27095-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27095-107">EXAMPLES</span></span>

### <span data-ttu-id="27095-108">Beispiel 1: Entfernen eines Runbooks</span><span class="sxs-lookup"><span data-stu-id="27095-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="27095-109">Mit diesem Befehl wird das Runbook "Runbook03" im Azure -Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="27095-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="27095-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27095-110">PARAMETERS</span></span>

### <span data-ttu-id="27095-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="27095-111">-AutomationAccountName</span></span>
<span data-ttu-id="27095-112">Gibt den Namen des Automatisierungskontos an, in dem dieses Cmdlet ein Runbook entfernt.</span><span class="sxs-lookup"><span data-stu-id="27095-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="27095-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27095-113">-DefaultProfile</span></span>
<span data-ttu-id="27095-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="27095-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27095-115">-Force</span><span class="sxs-lookup"><span data-stu-id="27095-115">-Force</span></span>
<span data-ttu-id="27095-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="27095-116">ps_force</span></span>

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

### <span data-ttu-id="27095-117">-Name</span><span class="sxs-lookup"><span data-stu-id="27095-117">-Name</span></span>
<span data-ttu-id="27095-118">Gibt den Namen des Runbooks an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="27095-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="27095-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27095-119">-ResourceGroupName</span></span>
<span data-ttu-id="27095-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Runbook veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="27095-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="27095-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27095-121">-Confirm</span></span>
<span data-ttu-id="27095-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27095-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27095-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27095-123">-WhatIf</span></span>
<span data-ttu-id="27095-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27095-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27095-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27095-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27095-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27095-126">CommonParameters</span></span>
<span data-ttu-id="27095-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27095-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27095-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27095-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27095-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27095-129">INPUTS</span></span>

### <span data-ttu-id="27095-130">System.String</span><span class="sxs-lookup"><span data-stu-id="27095-130">System.String</span></span>

## <span data-ttu-id="27095-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27095-131">OUTPUTS</span></span>

### <span data-ttu-id="27095-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="27095-132">System.Void</span></span>

## <span data-ttu-id="27095-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27095-133">NOTES</span></span>

## <span data-ttu-id="27095-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27095-134">RELATED LINKS</span></span>

[<span data-ttu-id="27095-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="27095-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="27095-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="27095-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="27095-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="27095-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="27095-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="27095-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27095-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


