---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 3b608feb9ed496be72d1d74f4a5a2be0569714de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657964"
---
# <span data-ttu-id="13a23-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="13a23-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="13a23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13a23-102">SYNOPSIS</span></span>
<span data-ttu-id="13a23-103">Entfernt eine Azure-Automatisierungssoftware-Update-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="13a23-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="13a23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13a23-104">SYNTAX</span></span>

### <span data-ttu-id="13a23-105">BySucName (Standard)</span><span class="sxs-lookup"><span data-stu-id="13a23-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13a23-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="13a23-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a23-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13a23-107">DESCRIPTION</span></span>
<span data-ttu-id="13a23-108">Dieses Cmdlet hat eine Azure Automation Software Update-Konfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="13a23-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="13a23-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13a23-109">EXAMPLES</span></span>

### <span data-ttu-id="13a23-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13a23-110">Example 1</span></span>
<span data-ttu-id="13a23-111">Dieses Beispiel zeigt, wie Sie "MyUpdateConfiguration" aus dem Automatisierungs Konto entfernen.</span><span class="sxs-lookup"><span data-stu-id="13a23-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="13a23-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13a23-112">PARAMETERS</span></span>

### <span data-ttu-id="13a23-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13a23-113">-AutomationAccountName</span></span>
<span data-ttu-id="13a23-114">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="13a23-114">The automation account name.</span></span>

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

### <span data-ttu-id="13a23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a23-115">-DefaultProfile</span></span>
<span data-ttu-id="13a23-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13a23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13a23-117">-Name</span><span class="sxs-lookup"><span data-stu-id="13a23-117">-Name</span></span>
<span data-ttu-id="13a23-118">Der Name der zu entfernenden Software Update Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="13a23-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="13a23-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13a23-119">-PassThru</span></span>
<span data-ttu-id="13a23-120">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="13a23-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="13a23-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="13a23-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13a23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a23-122">-ResourceGroupName</span></span>
<span data-ttu-id="13a23-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13a23-123">The resource group name.</span></span>

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

### <span data-ttu-id="13a23-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="13a23-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="13a23-125">Die zu entfernende Software Update-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="13a23-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="13a23-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13a23-126">-Confirm</span></span>
<span data-ttu-id="13a23-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13a23-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a23-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a23-128">-WhatIf</span></span>
<span data-ttu-id="13a23-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13a23-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a23-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13a23-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a23-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a23-131">CommonParameters</span></span>
<span data-ttu-id="13a23-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a23-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a23-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a23-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a23-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13a23-134">INPUTS</span></span>

### <span data-ttu-id="13a23-135">System. String</span><span class="sxs-lookup"><span data-stu-id="13a23-135">System.String</span></span>

### <span data-ttu-id="13a23-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="13a23-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="13a23-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13a23-137">OUTPUTS</span></span>

### <span data-ttu-id="13a23-138">System. void</span><span class="sxs-lookup"><span data-stu-id="13a23-138">System.Void</span></span>

### <span data-ttu-id="13a23-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13a23-139">System.Boolean</span></span>

## <span data-ttu-id="13a23-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="13a23-140">NOTES</span></span>

## <span data-ttu-id="13a23-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13a23-141">RELATED LINKS</span></span>
