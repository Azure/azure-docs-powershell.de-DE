---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373202"
---
# <span data-ttu-id="cd7f3-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd7f3-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="cd7f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7f3-103">Entfernt eine Updatekonfiguration für die Azure-Automatisierungssoftware.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="cd7f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd7f3-104">SYNTAX</span></span>

### <span data-ttu-id="cd7f3-105">BySucName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd7f3-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd7f3-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="cd7f3-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd7f3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd7f3-107">DESCRIPTION</span></span>
<span data-ttu-id="cd7f3-108">Dieses Cmdlet hat eine Konfiguration für das Aktualisieren von Softwareupdates für die Azure-Automatisierung entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="cd7f3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd7f3-109">EXAMPLES</span></span>

### <span data-ttu-id="cd7f3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cd7f3-110">Example 1</span></span>
<span data-ttu-id="cd7f3-111">In diesem Beispiel wird gezeigt, wie Sie "MyUpdateConfiguration" aus einem Automatisierungskonto entfernen.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="cd7f3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd7f3-112">PARAMETERS</span></span>

### <span data-ttu-id="cd7f3-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd7f3-113">-AutomationAccountName</span></span>
<span data-ttu-id="cd7f3-114">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-114">The automation account name.</span></span>

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

### <span data-ttu-id="cd7f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7f3-115">-DefaultProfile</span></span>
<span data-ttu-id="cd7f3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7f3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cd7f3-117">-Name</span></span>
<span data-ttu-id="cd7f3-118">Name der softwareupdatekonfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7f3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd7f3-119">-PassThru</span></span>
<span data-ttu-id="cd7f3-120">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cd7f3-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd7f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd7f3-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-123">The resource group name.</span></span>

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

### <span data-ttu-id="cd7f3-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd7f3-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="cd7f3-125">Die zu entfernende Softwareupdatekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7f3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd7f3-126">-Confirm</span></span>
<span data-ttu-id="cd7f3-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7f3-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cd7f3-128">-WhatIf</span></span>
<span data-ttu-id="cd7f3-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7f3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7f3-131">CommonParameters</span></span>
<span data-ttu-id="cd7f3-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7f3-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd7f3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7f3-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd7f3-134">INPUTS</span></span>

### <span data-ttu-id="cd7f3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="cd7f3-135">System.String</span></span>

### <span data-ttu-id="cd7f3-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd7f3-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="cd7f3-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd7f3-137">OUTPUTS</span></span>

### <span data-ttu-id="cd7f3-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="cd7f3-138">System.Void</span></span>

### <span data-ttu-id="cd7f3-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd7f3-139">System.Boolean</span></span>

## <span data-ttu-id="cd7f3-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cd7f3-140">NOTES</span></span>

## <span data-ttu-id="cd7f3-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cd7f3-141">RELATED LINKS</span></span>
