---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298075"
---
# <span data-ttu-id="f47a7-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="f47a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f47a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f47a7-103">Exportiert ein Automatisierungs-Runbook.</span><span class="sxs-lookup"><span data-stu-id="f47a7-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="f47a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f47a7-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f47a7-105">DESCRIPTION</span></span>
<span data-ttu-id="f47a7-106">Das Cmdlet **"Export-AzAutomationRunbook"** exportiert ein Azure Automation-Runbook für grafische Runbooks in eine wps_2-Skriptdatei (PS1), für wps_2- oder wps_2 Workflow-Runbooks oder in eine grafische Runbookdatei (GRAPHRUNBOOK).</span><span class="sxs-lookup"><span data-stu-id="f47a7-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="f47a7-107">Der Name des Runbooks wird zum Namen der exportierten Datei.</span><span class="sxs-lookup"><span data-stu-id="f47a7-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="f47a7-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f47a7-108">EXAMPLES</span></span>

### <span data-ttu-id="f47a7-109">Beispiel 1: Exportieren eines Runbooks</span><span class="sxs-lookup"><span data-stu-id="f47a7-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="f47a7-110">Mit diesem Befehl wird die veröffentlichte Version eines Automatisierungs-Runbooks auf einen Benutzerdesktop exportiert.</span><span class="sxs-lookup"><span data-stu-id="f47a7-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="f47a7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f47a7-111">PARAMETERS</span></span>

### <span data-ttu-id="f47a7-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f47a7-112">-AutomationAccountName</span></span>
<span data-ttu-id="f47a7-113">Gibt den Namen des Automatisierungskontos an, in das dieses Cmdlet ein Runbook exportiert.</span><span class="sxs-lookup"><span data-stu-id="f47a7-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="f47a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47a7-114">-DefaultProfile</span></span>
<span data-ttu-id="f47a7-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f47a7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f47a7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f47a7-116">-Force</span></span>
<span data-ttu-id="f47a7-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="f47a7-117">ps_force</span></span>

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

### <span data-ttu-id="f47a7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f47a7-118">-Name</span></span>
<span data-ttu-id="f47a7-119">Gibt den Namen des Runbooks an, das von diesem Cmdlet exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="f47a7-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="f47a7-120">Der Name des Runbooks wird zum Namen der Exportdatei.</span><span class="sxs-lookup"><span data-stu-id="f47a7-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="f47a7-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="f47a7-121">-OutputFolder</span></span>
<span data-ttu-id="f47a7-122">Gibt den Pfad eines Ordners an, in dem dieses Cmdlet die Exportdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="f47a7-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="f47a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="f47a7-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Runbook exportiert.</span><span class="sxs-lookup"><span data-stu-id="f47a7-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="f47a7-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="f47a7-125">-Slot</span></span>
<span data-ttu-id="f47a7-126">Gibt an, ob dieses Cmdlet den Entwurf oder veröffentlichten Inhalt des Runbooks exportiert.</span><span class="sxs-lookup"><span data-stu-id="f47a7-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="f47a7-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f47a7-127">Valid values are:</span></span> 
- <span data-ttu-id="f47a7-128">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="f47a7-128">Published</span></span> 
- <span data-ttu-id="f47a7-129">Entwurf</span><span class="sxs-lookup"><span data-stu-id="f47a7-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47a7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f47a7-130">-Confirm</span></span>
<span data-ttu-id="f47a7-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f47a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47a7-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f47a7-132">-WhatIf</span></span>
<span data-ttu-id="f47a7-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f47a7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f47a7-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f47a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47a7-135">CommonParameters</span></span>
<span data-ttu-id="f47a7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f47a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47a7-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47a7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47a7-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f47a7-138">INPUTS</span></span>

### <span data-ttu-id="f47a7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f47a7-139">System.String</span></span>

## <span data-ttu-id="f47a7-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f47a7-140">OUTPUTS</span></span>

### <span data-ttu-id="f47a7-141">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="f47a7-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="f47a7-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f47a7-142">NOTES</span></span>

## <span data-ttu-id="f47a7-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f47a7-143">RELATED LINKS</span></span>

[<span data-ttu-id="f47a7-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="f47a7-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="f47a7-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f47a7-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f47a7-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="f47a7-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="f47a7-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="f47a7-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f47a7-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


