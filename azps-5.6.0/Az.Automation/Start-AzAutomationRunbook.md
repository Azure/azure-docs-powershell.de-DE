---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 00eb652bc9779554f1c860edd503fc752c7ccaa0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921456"
---
# <span data-ttu-id="ce762-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="ce762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce762-102">SYNOPSIS</span></span>
<span data-ttu-id="ce762-103">Startet einen Runbookauftrag.</span><span class="sxs-lookup"><span data-stu-id="ce762-103">Starts a runbook job.</span></span>

## <span data-ttu-id="ce762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce762-104">SYNTAX</span></span>

### <span data-ttu-id="ce762-105">ByAsynchronousReturnJob (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce762-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce762-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="ce762-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce762-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce762-107">DESCRIPTION</span></span>
<span data-ttu-id="ce762-108">Das **Cmdlet Start-AzAutomationRunbook** startet einen Azure Automation-Runbookauftrag.</span><span class="sxs-lookup"><span data-stu-id="ce762-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="ce762-109">Geben Sie die ID oder den Namen eines Runbooks an.</span><span class="sxs-lookup"><span data-stu-id="ce762-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="ce762-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce762-110">EXAMPLES</span></span>

### <span data-ttu-id="ce762-111">Beispiel 1: Starten eines Runbookauftrags</span><span class="sxs-lookup"><span data-stu-id="ce762-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ce762-112">Mit diesem Befehl wird ein Runbookauftrag für das Runbook mit dem Namen Runbk01 im Azure Automation-Konto namens Contoso17 gestartet.</span><span class="sxs-lookup"><span data-stu-id="ce762-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="ce762-113">Beispiel 2: Starten eines Python 2-Runbookauftrags mit Parametern</span><span class="sxs-lookup"><span data-stu-id="ce762-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="ce762-114">Mit diesem Befehl wird ein Runbookauftrag für das Runbook "Python 2" mit dem Namen RunbkPy01 im Azure Automation-Konto namens Contoso17 mit "ValueForPosition1" als erstem Positionsparameter und "ValueForPosition2" für den zweiten Befehl gestartet.</span><span class="sxs-lookup"><span data-stu-id="ce762-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="ce762-115">Beispiel 3: Starten eines Runbookauftrags und Warten auf Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="ce762-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="ce762-116">Mit diesem Befehl wird ein Runbookauftrag für das Runbook mit dem Namen Runbk01 im Azure Automation-Konto namens Contoso17 gestartet.</span><span class="sxs-lookup"><span data-stu-id="ce762-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="ce762-117">Dieser Befehl gibt den Parameter _"Warten"_ an.</span><span class="sxs-lookup"><span data-stu-id="ce762-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="ce762-118">Daher gibt es Ergebnisse zurück, nachdem der Auftrag abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ce762-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="ce762-119">Das Cmdlet wartet bis zu 1000 Sekunden auf die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="ce762-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="ce762-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ce762-120">PARAMETERS</span></span>

### <span data-ttu-id="ce762-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce762-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="ce762-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce762-122">-DefaultProfile</span></span>
<span data-ttu-id="ce762-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ce762-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce762-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="ce762-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="ce762-125">Gibt die Anzahl der Sekunden an, in der dieses Cmdlet auf den Abschluss eines Auftrags wartet, bevor er den Auftrag aufgibt.</span><span class="sxs-lookup"><span data-stu-id="ce762-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="ce762-126">Der Standardwert ist 10800 oder drei Stunden.</span><span class="sxs-lookup"><span data-stu-id="ce762-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce762-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ce762-127">-Name</span></span>
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

### <span data-ttu-id="ce762-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ce762-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce762-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce762-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ce762-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="ce762-130">-RunOn</span></span>
<span data-ttu-id="ce762-131">Gibt an, für welche Hybridarbeitergruppe das Runbook ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce762-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce762-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="ce762-132">-Wait</span></span>
<span data-ttu-id="ce762-133">Gibt an, dass dieses Cmdlet wartet, bis der Auftrag abgeschlossen, angehalten oder fehlgeschlagen ist, und gibt dann das Steuerelement an Azure PowerShell zurück.</span><span class="sxs-lookup"><span data-stu-id="ce762-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce762-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce762-134">CommonParameters</span></span>
<span data-ttu-id="ce762-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce762-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce762-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce762-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce762-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce762-137">INPUTS</span></span>

### <span data-ttu-id="ce762-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ce762-138">System.String</span></span>

## <span data-ttu-id="ce762-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce762-139">OUTPUTS</span></span>

### <span data-ttu-id="ce762-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="ce762-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="ce762-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="ce762-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ce762-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ce762-142">NOTES</span></span>

## <span data-ttu-id="ce762-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ce762-143">RELATED LINKS</span></span>

[<span data-ttu-id="ce762-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="ce762-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="ce762-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ce762-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ce762-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ce762-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="ce762-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="ce762-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ce762-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
