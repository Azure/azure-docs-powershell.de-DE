---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: f6399c35316deb5590eada9eccd474ba7e47b116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498509"
---
# <span data-ttu-id="07913-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="07913-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07913-102">SYNOPSIS</span></span>
<span data-ttu-id="07913-103">Importiert ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="07913-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07913-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07913-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07913-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07913-105">DESCRIPTION</span></span>
<span data-ttu-id="07913-106">Mit dem Cmdlet " **Import-AzureRmAutomationRunbook** " wird ein Azure Automation-runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="07913-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="07913-107">Geben Sie den Pfad zu einer wps_2-Skriptdatei (. ps1) an, die für wps_2 und wps_2 Workflow-runbooks (graphrunbook) für die grafische runbooks oder (. py)-Datei für python 2 runbooks importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07913-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="07913-108">Für wps_2 Workflow-runbooks muss das Skript eine einzelne wps_2 Workflowdefinition enthalten, die dem Namen der Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="07913-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="07913-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07913-109">EXAMPLES</span></span>

### <span data-ttu-id="07913-110">Beispiel 1: Importieren einer runbooks aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="07913-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="07913-111">Der erste Befehl weist der $Tags-Variablen zwei Schlüssel-Wert-Paare zu.</span><span class="sxs-lookup"><span data-stu-id="07913-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="07913-112">Der zweite Befehl importiert eine grafische runbooks namens GraphicalRunbook06 in das Automatisierungs Konto mit dem Namen AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="07913-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="07913-113">Der Befehl weist auch die in $Tags gespeicherten Tags zu.</span><span class="sxs-lookup"><span data-stu-id="07913-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="07913-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="07913-114">PARAMETERS</span></span>

### <span data-ttu-id="07913-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="07913-115">-AutomationAccountName</span></span>
<span data-ttu-id="07913-116">Gibt den Namen des Automatisierungs Kontos an, in das dieses Cmdlet eine runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="07913-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="07913-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07913-117">-DefaultProfile</span></span>
<span data-ttu-id="07913-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="07913-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07913-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07913-119">-Description</span></span>
<span data-ttu-id="07913-120">Gibt eine Beschreibung für den importierten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="07913-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="07913-121">-Force</span><span class="sxs-lookup"><span data-stu-id="07913-121">-Force</span></span>
<span data-ttu-id="07913-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="07913-122">ps_force</span></span>

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

### <span data-ttu-id="07913-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="07913-123">-LogProgress</span></span>
<span data-ttu-id="07913-124">Gibt an, ob der runbooks Fortschrittsinformationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="07913-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="07913-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="07913-125">-LogVerbose</span></span>
<span data-ttu-id="07913-126">Gibt an, ob die runbooks detaillierte Informationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="07913-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="07913-127">-Name</span><span class="sxs-lookup"><span data-stu-id="07913-127">-Name</span></span>
<span data-ttu-id="07913-128">Gibt den Namen der runbooks an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="07913-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="07913-129">-Path</span><span class="sxs-lookup"><span data-stu-id="07913-129">-Path</span></span>
<span data-ttu-id="07913-130">Gibt den Pfad einer PS1-oder graphrunbook-Datei an, die von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="07913-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="07913-131">– Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="07913-131">-Published</span></span>
<span data-ttu-id="07913-132">Gibt an, dass dieses Cmdlet die runbooks veröffentlicht, die es importiert.</span><span class="sxs-lookup"><span data-stu-id="07913-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="07913-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07913-133">-ResourceGroupName</span></span>
<span data-ttu-id="07913-134">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks importiert.</span><span class="sxs-lookup"><span data-stu-id="07913-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="07913-135">-Tags</span><span class="sxs-lookup"><span data-stu-id="07913-135">-Tags</span></span>
<span data-ttu-id="07913-136">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="07913-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07913-137">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="07913-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="07913-138">-Typ</span><span class="sxs-lookup"><span data-stu-id="07913-138">-Type</span></span>
<span data-ttu-id="07913-139">Gibt den Typ der runbooks an, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="07913-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="07913-140">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="07913-140">Valid values are:</span></span>
- <span data-ttu-id="07913-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="07913-141">PowerShell</span></span>
- <span data-ttu-id="07913-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="07913-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="07913-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="07913-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="07913-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="07913-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="07913-145">Diagramm</span><span class="sxs-lookup"><span data-stu-id="07913-145">Graph</span></span>
- <span data-ttu-id="07913-146">Python2 der Wert Graph ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="07913-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="07913-147">Sie entspricht GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="07913-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07913-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07913-148">-Confirm</span></span>
<span data-ttu-id="07913-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07913-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07913-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07913-150">-WhatIf</span></span>
<span data-ttu-id="07913-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07913-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07913-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07913-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07913-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07913-153">CommonParameters</span></span>
<span data-ttu-id="07913-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07913-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07913-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07913-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07913-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07913-156">INPUTS</span></span>

### <span data-ttu-id="07913-157">System. String</span><span class="sxs-lookup"><span data-stu-id="07913-157">System.String</span></span>

### <span data-ttu-id="07913-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="07913-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="07913-159">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="07913-159">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="07913-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07913-160">OUTPUTS</span></span>

### <span data-ttu-id="07913-161">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="07913-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="07913-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="07913-162">NOTES</span></span>

## <span data-ttu-id="07913-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07913-163">RELATED LINKS</span></span>

[<span data-ttu-id="07913-164">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-164">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="07913-165">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-165">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="07913-166">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="07913-167">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="07913-168">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-168">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="07913-169">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-169">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="07913-170">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-170">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="07913-171">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="07913-171">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
