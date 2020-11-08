---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177034"
---
# <span data-ttu-id="809ab-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="809ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="809ab-102">SYNOPSIS</span></span>
<span data-ttu-id="809ab-103">Entfernt eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="809ab-103">Removes a runbook.</span></span>

## <span data-ttu-id="809ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="809ab-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="809ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809ab-105">DESCRIPTION</span></span>
<span data-ttu-id="809ab-106">Mit dem Cmdlet **Remove-AzAutomationRunbook** wird ein runbooks aus Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="809ab-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="809ab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="809ab-107">EXAMPLES</span></span>

### <span data-ttu-id="809ab-108">Beispiel 1: Entfernen eines runbooks</span><span class="sxs-lookup"><span data-stu-id="809ab-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="809ab-109">Dieser Befehl entfernt das runbooks mit dem Namen Runbook03 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="809ab-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="809ab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="809ab-110">PARAMETERS</span></span>

### <span data-ttu-id="809ab-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="809ab-111">-AutomationAccountName</span></span>
<span data-ttu-id="809ab-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks entfernt.</span><span class="sxs-lookup"><span data-stu-id="809ab-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="809ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809ab-113">-DefaultProfile</span></span>
<span data-ttu-id="809ab-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="809ab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="809ab-115">-Force</span><span class="sxs-lookup"><span data-stu-id="809ab-115">-Force</span></span>
<span data-ttu-id="809ab-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="809ab-116">ps_force</span></span>

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

### <span data-ttu-id="809ab-117">-Name</span><span class="sxs-lookup"><span data-stu-id="809ab-117">-Name</span></span>
<span data-ttu-id="809ab-118">Gibt den Namen der runbooks an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="809ab-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="809ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="809ab-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="809ab-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="809ab-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="809ab-121">-Confirm</span></span>
<span data-ttu-id="809ab-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="809ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="809ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="809ab-123">-WhatIf</span></span>
<span data-ttu-id="809ab-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="809ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="809ab-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="809ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="809ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809ab-126">CommonParameters</span></span>
<span data-ttu-id="809ab-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="809ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809ab-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="809ab-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809ab-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="809ab-129">INPUTS</span></span>

### <span data-ttu-id="809ab-130">System. String</span><span class="sxs-lookup"><span data-stu-id="809ab-130">System.String</span></span>

## <span data-ttu-id="809ab-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="809ab-131">OUTPUTS</span></span>

### <span data-ttu-id="809ab-132">System. void</span><span class="sxs-lookup"><span data-stu-id="809ab-132">System.Void</span></span>

## <span data-ttu-id="809ab-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="809ab-133">NOTES</span></span>

## <span data-ttu-id="809ab-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="809ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="809ab-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="809ab-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="809ab-137">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="809ab-138">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="809ab-139">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="809ab-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="809ab-141">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="809ab-142">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="809ab-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


