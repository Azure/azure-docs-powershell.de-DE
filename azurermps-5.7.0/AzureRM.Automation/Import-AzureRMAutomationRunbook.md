---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477022"
---
# <span data-ttu-id="25297-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="25297-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25297-102">SYNOPSIS</span></span>
<span data-ttu-id="25297-103">Importiert ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="25297-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25297-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25297-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25297-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25297-105">DESCRIPTION</span></span>
<span data-ttu-id="25297-106">Mit dem Cmdlet " **Import-AzureRmAutomationRunbook** " wird ein Azure Automation-runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="25297-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="25297-107">Geben Sie den Pfad zu einer wps_2-Skriptdatei (. ps1) an, die für wps_2 und wps_2 Workflow-runbooks (graphrunbook) für die grafische runbooks oder (. py)-Datei für python 2 runbooks importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="25297-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="25297-108">Für wps_2 Workflow-runbooks muss das Skript eine einzelne wps_2 Workflowdefinition enthalten, die dem Namen der Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="25297-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="25297-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25297-109">EXAMPLES</span></span>

### <span data-ttu-id="25297-110">Beispiel 1: Importieren einer runbooks aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="25297-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="25297-111">Der erste Befehl weist der $Tags-Variablen zwei Schlüssel-Wert-Paare zu.</span><span class="sxs-lookup"><span data-stu-id="25297-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="25297-112">Der zweite Befehl importiert eine grafische runbooks namens GraphicalRunbook06 in das Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="25297-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="25297-113">Der Befehl weist auch die in $Tags gespeicherten Tags zu.</span><span class="sxs-lookup"><span data-stu-id="25297-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="25297-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="25297-114">PARAMETERS</span></span>

### <span data-ttu-id="25297-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25297-115">-AutomationAccountName</span></span>
<span data-ttu-id="25297-116">Gibt den Namen des Automatisierungs Kontos an, in das dieses Cmdlet eine runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="25297-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25297-117">-DefaultProfile</span></span>
<span data-ttu-id="25297-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="25297-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25297-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25297-119">-Description</span></span>
<span data-ttu-id="25297-120">Gibt eine Beschreibung für den importierten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="25297-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-121">-Force</span><span class="sxs-lookup"><span data-stu-id="25297-121">-Force</span></span>
<span data-ttu-id="25297-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="25297-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25297-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="25297-123">-LogProgress</span></span>
<span data-ttu-id="25297-124">Gibt an, ob der runbooks Fortschrittsinformationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="25297-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="25297-125">-LogVerbose</span></span>
<span data-ttu-id="25297-126">Gibt an, ob die runbooks detaillierte Informationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="25297-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-127">-Name</span><span class="sxs-lookup"><span data-stu-id="25297-127">-Name</span></span>
<span data-ttu-id="25297-128">Gibt den Namen der runbooks an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="25297-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-129">-Path</span><span class="sxs-lookup"><span data-stu-id="25297-129">-Path</span></span>
<span data-ttu-id="25297-130">Gibt den Pfad einer PS1-oder graphrunbook-Datei an, die von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="25297-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-131">– Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="25297-131">-Published</span></span>
<span data-ttu-id="25297-132">Gibt an, dass dieses Cmdlet die runbooks veröffentlicht, die es importiert.</span><span class="sxs-lookup"><span data-stu-id="25297-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25297-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25297-133">-ResourceGroupName</span></span>
<span data-ttu-id="25297-134">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="25297-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-135">-Tags</span><span class="sxs-lookup"><span data-stu-id="25297-135">-Tags</span></span>
<span data-ttu-id="25297-136">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="25297-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="25297-137">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="25297-137">For example:</span></span>

<span data-ttu-id="25297-138">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="25297-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25297-139">-Typ</span><span class="sxs-lookup"><span data-stu-id="25297-139">-Type</span></span>
<span data-ttu-id="25297-140">Gibt den Typ der runbooks an, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="25297-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="25297-141">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="25297-141">Valid values are:</span></span>

- <span data-ttu-id="25297-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="25297-142">PowerShell</span></span>
- <span data-ttu-id="25297-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="25297-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="25297-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="25297-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="25297-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="25297-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="25297-146">Diagramm</span><span class="sxs-lookup"><span data-stu-id="25297-146">Graph</span></span>
- <span data-ttu-id="25297-147">Python2</span><span class="sxs-lookup"><span data-stu-id="25297-147">Python2</span></span>

<span data-ttu-id="25297-148">Der Wert Graph ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="25297-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="25297-149">Sie entspricht GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="25297-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25297-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25297-150">-Confirm</span></span>
<span data-ttu-id="25297-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25297-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25297-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25297-152">-WhatIf</span></span>
<span data-ttu-id="25297-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25297-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25297-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25297-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25297-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25297-155">CommonParameters</span></span>
<span data-ttu-id="25297-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25297-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25297-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25297-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25297-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25297-158">INPUTS</span></span>

### <span data-ttu-id="25297-159">Keine</span><span class="sxs-lookup"><span data-stu-id="25297-159">None</span></span>
<span data-ttu-id="25297-160">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="25297-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25297-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25297-161">OUTPUTS</span></span>

### <span data-ttu-id="25297-162">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="25297-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="25297-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="25297-163">NOTES</span></span>

## <span data-ttu-id="25297-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25297-164">RELATED LINKS</span></span>

[<span data-ttu-id="25297-165">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="25297-166">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="25297-167">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="25297-168">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="25297-169">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="25297-170">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="25297-171">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="25297-172">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25297-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
