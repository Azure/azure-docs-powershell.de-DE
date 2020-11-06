---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480598"
---
# <span data-ttu-id="190a0-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="190a0-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="190a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="190a0-102">SYNOPSIS</span></span>
<span data-ttu-id="190a0-103">Entfernt eine Azure-Automatisierungssoftware-Update-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="190a0-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="190a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="190a0-104">SYNTAX</span></span>

### <span data-ttu-id="190a0-105">BySucName (Standard)</span><span class="sxs-lookup"><span data-stu-id="190a0-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="190a0-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="190a0-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="190a0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="190a0-107">DESCRIPTION</span></span>
<span data-ttu-id="190a0-108">Dieses Cmdlet hat eine Azure Automation Software Update-Konfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="190a0-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="190a0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="190a0-109">EXAMPLES</span></span>

### <span data-ttu-id="190a0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="190a0-110">Example 1</span></span>
<span data-ttu-id="190a0-111">Dieses Beispiel zeigt, wie Sie "MyUpdateConfiguration" aus dem Automatisierungs Konto entfernen.</span><span class="sxs-lookup"><span data-stu-id="190a0-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="190a0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="190a0-112">PARAMETERS</span></span>

### <span data-ttu-id="190a0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="190a0-113">-AutomationAccountName</span></span>
<span data-ttu-id="190a0-114">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="190a0-114">The automation account name.</span></span>

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

### <span data-ttu-id="190a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190a0-115">-DefaultProfile</span></span>
<span data-ttu-id="190a0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="190a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190a0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="190a0-117">-Name</span></span>
<span data-ttu-id="190a0-118">Der Name der zu entfernenden Software Update Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="190a0-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="190a0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="190a0-119">-PassThru</span></span>
<span data-ttu-id="190a0-120">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="190a0-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="190a0-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="190a0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="190a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="190a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="190a0-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="190a0-123">The resource group name.</span></span>

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

### <span data-ttu-id="190a0-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="190a0-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="190a0-125">Die zu entfernende Software Update-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="190a0-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="190a0-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="190a0-126">-Confirm</span></span>
<span data-ttu-id="190a0-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="190a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190a0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190a0-128">-WhatIf</span></span>
<span data-ttu-id="190a0-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="190a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="190a0-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="190a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190a0-131">CommonParameters</span></span>
<span data-ttu-id="190a0-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190a0-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190a0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190a0-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="190a0-134">INPUTS</span></span>

### <span data-ttu-id="190a0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="190a0-135">System.String</span></span>

### <span data-ttu-id="190a0-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="190a0-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="190a0-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="190a0-137">OUTPUTS</span></span>

### <span data-ttu-id="190a0-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="190a0-138">System.Object</span></span>
## <span data-ttu-id="190a0-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="190a0-139">NOTES</span></span>

## <span data-ttu-id="190a0-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="190a0-140">RELATED LINKS</span></span>
