---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: f982c68c49d6a8a92bb06bf150e352626730f67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482585"
---
# <span data-ttu-id="32a76-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="32a76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32a76-102">SYNOPSIS</span></span>
<span data-ttu-id="32a76-103">Exportiert eine Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="32a76-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32a76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32a76-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32a76-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32a76-105">DESCRIPTION</span></span>
<span data-ttu-id="32a76-106">Das Cmdlet **Export-AzureRmAutomationRunbook** exportiert eine Azure Automation-runbooks in eine wps_2-Skriptdatei (ps1) für wps_2 oder wps_2 Workflow-runbooks oder in eine grafische runbooks-Datei (graphrunbook) für grafische runbooks.</span><span class="sxs-lookup"><span data-stu-id="32a76-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="32a76-107">Der Name des runbooks wird zum Namen der exportierten Datei.</span><span class="sxs-lookup"><span data-stu-id="32a76-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="32a76-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32a76-108">EXAMPLES</span></span>

### <span data-ttu-id="32a76-109">Beispiel 1: Exportieren einer runbooks</span><span class="sxs-lookup"><span data-stu-id="32a76-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="32a76-110">Dieser Befehl exportiert die veröffentlichte Version eines Automatisierungs runbooks auf einen Benutzerdesktop.</span><span class="sxs-lookup"><span data-stu-id="32a76-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="32a76-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="32a76-111">PARAMETERS</span></span>

### <span data-ttu-id="32a76-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="32a76-112">-AutomationAccountName</span></span>
<span data-ttu-id="32a76-113">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks exportiert.</span><span class="sxs-lookup"><span data-stu-id="32a76-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="32a76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a76-114">-DefaultProfile</span></span>
<span data-ttu-id="32a76-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="32a76-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32a76-116">-Force</span><span class="sxs-lookup"><span data-stu-id="32a76-116">-Force</span></span>
<span data-ttu-id="32a76-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="32a76-117">ps_force</span></span>

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

### <span data-ttu-id="32a76-118">-Name</span><span class="sxs-lookup"><span data-stu-id="32a76-118">-Name</span></span>
<span data-ttu-id="32a76-119">Gibt den Namen des vom Cmdlet exportierten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="32a76-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="32a76-120">Der Name des runbooks wird zum Namen der Exportdatei.</span><span class="sxs-lookup"><span data-stu-id="32a76-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="32a76-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="32a76-121">-OutputFolder</span></span>
<span data-ttu-id="32a76-122">Gibt den Pfad eines Ordners an, in dem dieses Cmdlet die Exportdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="32a76-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="32a76-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a76-123">-ResourceGroupName</span></span>
<span data-ttu-id="32a76-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks exportiert.</span><span class="sxs-lookup"><span data-stu-id="32a76-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="32a76-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="32a76-125">-Slot</span></span>
<span data-ttu-id="32a76-126">Gibt an, ob das Cmdlet den Entwurf oder veröffentlichten Inhalt des runbooks exportiert.</span><span class="sxs-lookup"><span data-stu-id="32a76-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="32a76-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="32a76-127">Valid values are:</span></span> 
- <span data-ttu-id="32a76-128">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="32a76-128">Published</span></span> 
- <span data-ttu-id="32a76-129">Entwurf</span><span class="sxs-lookup"><span data-stu-id="32a76-129">Draft</span></span>

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

### <span data-ttu-id="32a76-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32a76-130">-Confirm</span></span>
<span data-ttu-id="32a76-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32a76-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32a76-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32a76-132">-WhatIf</span></span>
<span data-ttu-id="32a76-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32a76-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32a76-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32a76-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32a76-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a76-135">CommonParameters</span></span>
<span data-ttu-id="32a76-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a76-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a76-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a76-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a76-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32a76-138">INPUTS</span></span>

### <span data-ttu-id="32a76-139">System. String</span><span class="sxs-lookup"><span data-stu-id="32a76-139">System.String</span></span>

## <span data-ttu-id="32a76-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32a76-140">OUTPUTS</span></span>

### <span data-ttu-id="32a76-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="32a76-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="32a76-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="32a76-142">NOTES</span></span>

## <span data-ttu-id="32a76-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32a76-143">RELATED LINKS</span></span>

[<span data-ttu-id="32a76-144">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-144">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32a76-145">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-145">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32a76-146">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32a76-147">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32a76-148">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-148">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32a76-149">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-149">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32a76-150">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-150">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32a76-151">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32a76-151">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


