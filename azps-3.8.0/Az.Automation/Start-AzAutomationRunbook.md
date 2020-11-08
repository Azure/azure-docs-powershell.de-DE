---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995272"
---
# <span data-ttu-id="70afc-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="70afc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70afc-102">SYNOPSIS</span></span>
<span data-ttu-id="70afc-103">Startet einen runbooks-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="70afc-103">Starts a runbook job.</span></span>

## <span data-ttu-id="70afc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70afc-104">SYNTAX</span></span>

### <span data-ttu-id="70afc-105">ByAsynchronousReturnJob (Standard)</span><span class="sxs-lookup"><span data-stu-id="70afc-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70afc-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="70afc-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70afc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70afc-107">DESCRIPTION</span></span>
<span data-ttu-id="70afc-108">Mit dem Cmdlet **Start-AzAutomationRunbook** wird ein Azure Automation runbooks-Auftrag gestartet.</span><span class="sxs-lookup"><span data-stu-id="70afc-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="70afc-109">Geben Sie die ID oder den Namen eines runbooks an.</span><span class="sxs-lookup"><span data-stu-id="70afc-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="70afc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70afc-110">EXAMPLES</span></span>

### <span data-ttu-id="70afc-111">Beispiel 1: Starten eines runbooks-Auftrags</span><span class="sxs-lookup"><span data-stu-id="70afc-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="70afc-112">Mit diesem Befehl wird ein runbooks-Auftrag für den runbooks mit dem Namen Runbk01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 gestartet.</span><span class="sxs-lookup"><span data-stu-id="70afc-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="70afc-113">Beispiel 2: Starten eines Python 2-runbooks-Auftrags mit Parametern</span><span class="sxs-lookup"><span data-stu-id="70afc-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="70afc-114">Mit diesem Befehl wird ein runbooks-Auftrag für die python 2-runbooks mit dem Namen RunbkPy01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 mit "ValueForPosition1" als erster positioneller Parameter und "ValueForPosition2" für das zweite Element gestartet.</span><span class="sxs-lookup"><span data-stu-id="70afc-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="70afc-115">Beispiel 3: Starten eines runbooks-Auftrags und warten auf Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="70afc-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="70afc-116">Mit diesem Befehl wird ein runbooks-Auftrag für den runbooks mit dem Namen Runbk01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 gestartet.</span><span class="sxs-lookup"><span data-stu-id="70afc-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="70afc-117">Mit diesem Befehl wird der _Wait_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="70afc-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="70afc-118">Daher gibt Sie Ergebnisse zurück, nachdem der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="70afc-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="70afc-119">Das Cmdlet wartet auf bis zu 1000 Sekunden für die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="70afc-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="70afc-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="70afc-120">PARAMETERS</span></span>

### <span data-ttu-id="70afc-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70afc-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="70afc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70afc-122">-DefaultProfile</span></span>
<span data-ttu-id="70afc-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="70afc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70afc-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="70afc-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="70afc-125">Gibt an, wie viele Sekunden dieses Cmdlet wartet, bis ein Auftrag beendet wird, bevor der Auftrag aufgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="70afc-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="70afc-126">Der Standardwert ist 10800 oder drei Stunden.</span><span class="sxs-lookup"><span data-stu-id="70afc-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="70afc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="70afc-127">-Name</span></span>
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

### <span data-ttu-id="70afc-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="70afc-128">-Parameters</span></span>
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

### <span data-ttu-id="70afc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70afc-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="70afc-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="70afc-130">-RunOn</span></span>
<span data-ttu-id="70afc-131">Gibt an, welche Hybrid Arbeitskraft Gruppe für die runbooks ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="70afc-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="70afc-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="70afc-132">-Wait</span></span>
<span data-ttu-id="70afc-133">Gibt an, dass dieses Cmdlet wartet, bis der Auftrag abgeschlossen, angehalten oder fehlschlägt, und gibt dann die Steuerung an Azure PowerShell zurück.</span><span class="sxs-lookup"><span data-stu-id="70afc-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="70afc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70afc-134">CommonParameters</span></span>
<span data-ttu-id="70afc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70afc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70afc-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70afc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70afc-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70afc-137">INPUTS</span></span>

### <span data-ttu-id="70afc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="70afc-138">System.String</span></span>

## <span data-ttu-id="70afc-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70afc-139">OUTPUTS</span></span>

### <span data-ttu-id="70afc-140">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="70afc-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="70afc-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="70afc-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="70afc-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="70afc-142">NOTES</span></span>

## <span data-ttu-id="70afc-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70afc-143">RELATED LINKS</span></span>

[<span data-ttu-id="70afc-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="70afc-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="70afc-146">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="70afc-147">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="70afc-148">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="70afc-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="70afc-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="70afc-151">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70afc-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
