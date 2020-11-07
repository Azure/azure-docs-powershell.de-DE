---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 6d0af3f0d991d8d6b1f73c3277f9f86ac8dd0dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658084"
---
# <span data-ttu-id="1c6fa-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="1c6fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6fa-103">Exportiert eine Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="1c6fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c6fa-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c6fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c6fa-105">DESCRIPTION</span></span>
<span data-ttu-id="1c6fa-106">Das Cmdlet **Export-AzAutomationRunbook** exportiert eine Azure Automation-runbooks in eine wps_2-Skriptdatei (ps1) für wps_2 oder wps_2 Workflow-runbooks oder in eine grafische runbooks-Datei (graphrunbook) für grafische runbooks.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="1c6fa-107">Der Name des runbooks wird zum Namen der exportierten Datei.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="1c6fa-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c6fa-108">EXAMPLES</span></span>

### <span data-ttu-id="1c6fa-109">Beispiel 1: Exportieren einer runbooks</span><span class="sxs-lookup"><span data-stu-id="1c6fa-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1c6fa-110">Dieser Befehl exportiert die veröffentlichte Version eines Automatisierungs runbooks auf einen Benutzerdesktop.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="1c6fa-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c6fa-111">PARAMETERS</span></span>

### <span data-ttu-id="1c6fa-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1c6fa-112">-AutomationAccountName</span></span>
<span data-ttu-id="1c6fa-113">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks exportiert.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="1c6fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6fa-114">-DefaultProfile</span></span>
<span data-ttu-id="1c6fa-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1c6fa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c6fa-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1c6fa-116">-Force</span></span>
<span data-ttu-id="1c6fa-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="1c6fa-117">ps_force</span></span>

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

### <span data-ttu-id="1c6fa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1c6fa-118">-Name</span></span>
<span data-ttu-id="1c6fa-119">Gibt den Namen des vom Cmdlet exportierten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="1c6fa-120">Der Name des runbooks wird zum Namen der Exportdatei.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="1c6fa-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1c6fa-121">-OutputFolder</span></span>
<span data-ttu-id="1c6fa-122">Gibt den Pfad eines Ordners an, in dem dieses Cmdlet die Exportdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="1c6fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c6fa-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks exportiert.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="1c6fa-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="1c6fa-125">-Slot</span></span>
<span data-ttu-id="1c6fa-126">Gibt an, ob das Cmdlet den Entwurf oder veröffentlichten Inhalt des runbooks exportiert.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="1c6fa-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1c6fa-127">Valid values are:</span></span> 
- <span data-ttu-id="1c6fa-128">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="1c6fa-128">Published</span></span> 
- <span data-ttu-id="1c6fa-129">Entwurf</span><span class="sxs-lookup"><span data-stu-id="1c6fa-129">Draft</span></span>

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

### <span data-ttu-id="1c6fa-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c6fa-130">-Confirm</span></span>
<span data-ttu-id="1c6fa-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6fa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6fa-132">-WhatIf</span></span>
<span data-ttu-id="1c6fa-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c6fa-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6fa-135">CommonParameters</span></span>
<span data-ttu-id="1c6fa-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c6fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6fa-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6fa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6fa-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c6fa-138">INPUTS</span></span>

### <span data-ttu-id="1c6fa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1c6fa-139">System.String</span></span>

## <span data-ttu-id="1c6fa-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c6fa-140">OUTPUTS</span></span>

### <span data-ttu-id="1c6fa-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1c6fa-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1c6fa-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c6fa-142">NOTES</span></span>

## <span data-ttu-id="1c6fa-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c6fa-143">RELATED LINKS</span></span>

[<span data-ttu-id="1c6fa-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="1c6fa-145">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="1c6fa-146">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1c6fa-147">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1c6fa-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="1c6fa-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="1c6fa-150">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="1c6fa-151">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1c6fa-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


