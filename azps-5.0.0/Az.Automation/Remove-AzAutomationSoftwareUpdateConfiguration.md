---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177031"
---
# <span data-ttu-id="937a7-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="937a7-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="937a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="937a7-102">SYNOPSIS</span></span>
<span data-ttu-id="937a7-103">Entfernt eine Azure-Automatisierungssoftware-Update-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="937a7-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="937a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="937a7-104">SYNTAX</span></span>

### <span data-ttu-id="937a7-105">BySucName (Standard)</span><span class="sxs-lookup"><span data-stu-id="937a7-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="937a7-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="937a7-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="937a7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="937a7-107">DESCRIPTION</span></span>
<span data-ttu-id="937a7-108">Dieses Cmdlet hat eine Azure Automation Software Update-Konfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="937a7-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="937a7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="937a7-109">EXAMPLES</span></span>

### <span data-ttu-id="937a7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="937a7-110">Example 1</span></span>
<span data-ttu-id="937a7-111">Dieses Beispiel zeigt, wie Sie "MyUpdateConfiguration" aus dem Automatisierungs Konto entfernen.</span><span class="sxs-lookup"><span data-stu-id="937a7-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="937a7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="937a7-112">PARAMETERS</span></span>

### <span data-ttu-id="937a7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="937a7-113">-AutomationAccountName</span></span>
<span data-ttu-id="937a7-114">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="937a7-114">The automation account name.</span></span>

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

### <span data-ttu-id="937a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937a7-115">-DefaultProfile</span></span>
<span data-ttu-id="937a7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="937a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="937a7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="937a7-117">-Name</span></span>
<span data-ttu-id="937a7-118">Der Name der zu entfernenden Software Update Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="937a7-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="937a7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="937a7-119">-PassThru</span></span>
<span data-ttu-id="937a7-120">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="937a7-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="937a7-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="937a7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="937a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="937a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="937a7-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="937a7-123">The resource group name.</span></span>

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

### <span data-ttu-id="937a7-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="937a7-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="937a7-125">Die zu entfernende Software Update-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="937a7-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="937a7-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="937a7-126">-Confirm</span></span>
<span data-ttu-id="937a7-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="937a7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937a7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937a7-128">-WhatIf</span></span>
<span data-ttu-id="937a7-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="937a7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="937a7-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="937a7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="937a7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937a7-131">CommonParameters</span></span>
<span data-ttu-id="937a7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937a7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937a7-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937a7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937a7-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="937a7-134">INPUTS</span></span>

### <span data-ttu-id="937a7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="937a7-135">System.String</span></span>

### <span data-ttu-id="937a7-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="937a7-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="937a7-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="937a7-137">OUTPUTS</span></span>

### <span data-ttu-id="937a7-138">System. void</span><span class="sxs-lookup"><span data-stu-id="937a7-138">System.Void</span></span>

### <span data-ttu-id="937a7-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="937a7-139">System.Boolean</span></span>

## <span data-ttu-id="937a7-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="937a7-140">NOTES</span></span>

## <span data-ttu-id="937a7-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="937a7-141">RELATED LINKS</span></span>
