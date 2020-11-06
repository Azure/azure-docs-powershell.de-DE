---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497974"
---
# <span data-ttu-id="1577f-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="1577f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1577f-102">SYNOPSIS</span></span>
<span data-ttu-id="1577f-103">Importiert ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="1577f-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1577f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1577f-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1577f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1577f-105">DESCRIPTION</span></span>
<span data-ttu-id="1577f-106">Mit dem Cmdlet " **Import-AzureRmAutomationRunbook** " wird ein Azure Automation-runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="1577f-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="1577f-107">Geben Sie den Pfad zu einer wps_2-Skriptdatei (ps1) an, die für wps_2-und wps_2 Workflow-runbooks oder in eine grafische runbooks-Datei (graphrunbook) für grafische runbooks importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1577f-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="1577f-108">Der Name der Datei wird zum Namen des runbooks.</span><span class="sxs-lookup"><span data-stu-id="1577f-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="1577f-109">Für wps_2 Workflow-runbooks muss das Skript eine einzelne wps_2 Workflowdefinition enthalten, die dem Namen der Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="1577f-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="1577f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1577f-110">EXAMPLES</span></span>

### <span data-ttu-id="1577f-111">Beispiel 1: Importieren einer runbooks aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="1577f-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="1577f-112">Der erste Befehl weist der $Tags-Variablen zwei Schlüssel-Wert-Paare zu.</span><span class="sxs-lookup"><span data-stu-id="1577f-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="1577f-113">Der zweite Befehl importiert eine grafische runbooks namens GraphicalRunbook06 in das Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1577f-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1577f-114">Der Befehl weist auch die in $Tags gespeicherten Tags zu.</span><span class="sxs-lookup"><span data-stu-id="1577f-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="1577f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1577f-115">PARAMETERS</span></span>

### <span data-ttu-id="1577f-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1577f-116">-AutomationAccountName</span></span>
<span data-ttu-id="1577f-117">Gibt den Namen des Automatisierungs Kontos an, in das dieses Cmdlet eine runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="1577f-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="1577f-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1577f-118">-Description</span></span>
<span data-ttu-id="1577f-119">Gibt eine Beschreibung für den importierten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="1577f-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="1577f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1577f-120">-Force</span></span>
<span data-ttu-id="1577f-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="1577f-121">ps_force</span></span>

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

### <span data-ttu-id="1577f-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="1577f-122">-LogProgress</span></span>
<span data-ttu-id="1577f-123">Gibt an, ob der runbooks Fortschrittsinformationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="1577f-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="1577f-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="1577f-124">-LogVerbose</span></span>
<span data-ttu-id="1577f-125">Gibt an, ob die runbooks detaillierte Informationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="1577f-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="1577f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1577f-126">-Name</span></span>
<span data-ttu-id="1577f-127">Gibt den Namen der runbooks an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="1577f-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1577f-128">-Path</span><span class="sxs-lookup"><span data-stu-id="1577f-128">-Path</span></span>
<span data-ttu-id="1577f-129">Gibt den Pfad einer PS1-oder graphrunbook-Datei an, die von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="1577f-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1577f-130">– Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="1577f-130">-Published</span></span>
<span data-ttu-id="1577f-131">Gibt an, dass dieses Cmdlet die runbooks veröffentlicht, die es importiert.</span><span class="sxs-lookup"><span data-stu-id="1577f-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="1577f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1577f-132">-ResourceGroupName</span></span>
<span data-ttu-id="1577f-133">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="1577f-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="1577f-134">-Tags</span><span class="sxs-lookup"><span data-stu-id="1577f-134">-Tags</span></span>
<span data-ttu-id="1577f-135">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="1577f-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1577f-136">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1577f-136">For example:</span></span>

<span data-ttu-id="1577f-137">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="1577f-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1577f-138">-Typ</span><span class="sxs-lookup"><span data-stu-id="1577f-138">-Type</span></span>
<span data-ttu-id="1577f-139">Gibt den Typ der runbooks an, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1577f-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="1577f-140">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1577f-140">Valid values are:</span></span>

- <span data-ttu-id="1577f-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1577f-141">PowerShell</span></span>
- <span data-ttu-id="1577f-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="1577f-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="1577f-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="1577f-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="1577f-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="1577f-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="1577f-145">Diagramm</span><span class="sxs-lookup"><span data-stu-id="1577f-145">Graph</span></span>

<span data-ttu-id="1577f-146">Der Wert Graph ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="1577f-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="1577f-147">Sie entspricht GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="1577f-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1577f-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1577f-148">-Confirm</span></span>
<span data-ttu-id="1577f-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1577f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1577f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1577f-150">-WhatIf</span></span>
<span data-ttu-id="1577f-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1577f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1577f-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1577f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1577f-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1577f-153">-DefaultProfile</span></span>
<span data-ttu-id="1577f-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1577f-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1577f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1577f-155">CommonParameters</span></span>
<span data-ttu-id="1577f-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1577f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1577f-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1577f-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1577f-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1577f-158">INPUTS</span></span>

## <span data-ttu-id="1577f-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1577f-159">OUTPUTS</span></span>

### <span data-ttu-id="1577f-160">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="1577f-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="1577f-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="1577f-161">NOTES</span></span>

## <span data-ttu-id="1577f-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1577f-162">RELATED LINKS</span></span>

[<span data-ttu-id="1577f-163">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1577f-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1577f-165">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1577f-166">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1577f-167">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1577f-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1577f-169">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1577f-170">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1577f-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
