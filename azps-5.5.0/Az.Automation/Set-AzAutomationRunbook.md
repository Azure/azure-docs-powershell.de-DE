---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149353"
---
# <span data-ttu-id="640c4-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="640c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="640c4-102">SYNOPSIS</span></span>
<span data-ttu-id="640c4-103">Ändert ein Runbook.</span><span class="sxs-lookup"><span data-stu-id="640c4-103">Modifies a runbook.</span></span>

## <span data-ttu-id="640c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="640c4-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="640c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="640c4-105">DESCRIPTION</span></span>
<span data-ttu-id="640c4-106">Das **Cmdlet "Set-AzAutomationRunbook"** ändert die Konfiguration eines Azure Automation Runbook in APS.</span><span class="sxs-lookup"><span data-stu-id="640c4-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="640c4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="640c4-107">EXAMPLES</span></span>

### <span data-ttu-id="640c4-108">Beispiel 1: Aktivieren der ausführlichen Protokollierung für ein Runbook</span><span class="sxs-lookup"><span data-stu-id="640c4-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="640c4-109">Dieser Befehl ermöglicht eine ausführliche Protokollierung für die Aufträge des angegebenen Runbooks im Azure-Automatisierungskonto namens "Contoso17".</span><span class="sxs-lookup"><span data-stu-id="640c4-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="640c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="640c4-110">PARAMETERS</span></span>

### <span data-ttu-id="640c4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="640c4-111">-AutomationAccountName</span></span>
<span data-ttu-id="640c4-112">Gibt den Namen des Automatisierungskontos an, in dem dieses Cmdlet ein Runbook ändert.</span><span class="sxs-lookup"><span data-stu-id="640c4-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="640c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640c4-113">-DefaultProfile</span></span>
<span data-ttu-id="640c4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="640c4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="640c4-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="640c4-115">-Description</span></span>
<span data-ttu-id="640c4-116">Gibt eine Beschreibung für das Runbook an.</span><span class="sxs-lookup"><span data-stu-id="640c4-116">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640c4-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="640c4-117">-LogProgress</span></span>
<span data-ttu-id="640c4-118">Gibt an, ob das Runbook den Fortschritt protokolliert.</span><span class="sxs-lookup"><span data-stu-id="640c4-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640c4-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="640c4-119">-LogVerbose</span></span>
<span data-ttu-id="640c4-120">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="640c4-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640c4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="640c4-121">-Name</span></span>
<span data-ttu-id="640c4-122">Gibt den Namen des Runbooks an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="640c4-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="640c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="640c4-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Runbook ändert.</span><span class="sxs-lookup"><span data-stu-id="640c4-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="640c4-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="640c4-125">-Tag</span></span>
<span data-ttu-id="640c4-126">Die Runbooktags.</span><span class="sxs-lookup"><span data-stu-id="640c4-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640c4-127">CommonParameters</span></span>
<span data-ttu-id="640c4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640c4-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="640c4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640c4-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="640c4-130">INPUTS</span></span>

### <span data-ttu-id="640c4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="640c4-131">System.String</span></span>

### <span data-ttu-id="640c4-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="640c4-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="640c4-133">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="640c4-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="640c4-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="640c4-134">OUTPUTS</span></span>

### <span data-ttu-id="640c4-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="640c4-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="640c4-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="640c4-136">NOTES</span></span>

## <span data-ttu-id="640c4-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="640c4-137">RELATED LINKS</span></span>

[<span data-ttu-id="640c4-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="640c4-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="640c4-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="640c4-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="640c4-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="640c4-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="640c4-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="640c4-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="640c4-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


