---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: c77413f27bcde145334221465cbe792a5e1eaa5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661731"
---
# <span data-ttu-id="d45c0-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="d45c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d45c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d45c0-103">Entfernt eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="d45c0-103">Removes a runbook.</span></span>

## <span data-ttu-id="d45c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d45c0-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d45c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d45c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d45c0-106">Mit dem Cmdlet **Remove-AzAutomationRunbook** wird ein runbooks aus Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="d45c0-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="d45c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d45c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d45c0-108">Beispiel 1: Entfernen eines runbooks</span><span class="sxs-lookup"><span data-stu-id="d45c0-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d45c0-109">Dieser Befehl entfernt das runbooks mit dem Namen Runbook03 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d45c0-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d45c0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d45c0-110">PARAMETERS</span></span>

### <span data-ttu-id="d45c0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d45c0-111">-AutomationAccountName</span></span>
<span data-ttu-id="d45c0-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks entfernt.</span><span class="sxs-lookup"><span data-stu-id="d45c0-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="d45c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45c0-113">-DefaultProfile</span></span>
<span data-ttu-id="d45c0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d45c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d45c0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d45c0-115">-Force</span></span>
<span data-ttu-id="d45c0-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="d45c0-116">ps_force</span></span>

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

### <span data-ttu-id="d45c0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d45c0-117">-Name</span></span>
<span data-ttu-id="d45c0-118">Gibt den Namen der runbooks an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d45c0-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d45c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d45c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="d45c0-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d45c0-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="d45c0-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d45c0-121">-Confirm</span></span>
<span data-ttu-id="d45c0-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d45c0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d45c0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45c0-123">-WhatIf</span></span>
<span data-ttu-id="d45c0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d45c0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d45c0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d45c0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d45c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45c0-126">CommonParameters</span></span>
<span data-ttu-id="d45c0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d45c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45c0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45c0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d45c0-129">INPUTS</span></span>

### <span data-ttu-id="d45c0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d45c0-130">System.String</span></span>

## <span data-ttu-id="d45c0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d45c0-131">OUTPUTS</span></span>

### <span data-ttu-id="d45c0-132">System. void</span><span class="sxs-lookup"><span data-stu-id="d45c0-132">System.Void</span></span>

## <span data-ttu-id="d45c0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d45c0-133">NOTES</span></span>

## <span data-ttu-id="d45c0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d45c0-134">RELATED LINKS</span></span>

[<span data-ttu-id="d45c0-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="d45c0-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="d45c0-137">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="d45c0-138">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d45c0-139">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d45c0-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="d45c0-141">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="d45c0-142">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d45c0-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


