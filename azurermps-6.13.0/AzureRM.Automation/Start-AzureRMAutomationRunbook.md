---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46544d42cb28f5fca046586696b95286cdd7f3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663687"
---
# <span data-ttu-id="bb900-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="bb900-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb900-102">SYNOPSIS</span></span>
<span data-ttu-id="bb900-103">Startet einen runbooks-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="bb900-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb900-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb900-104">SYNTAX</span></span>

### <span data-ttu-id="bb900-105">ByAsynchronousReturnJob (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb900-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb900-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="bb900-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb900-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb900-107">DESCRIPTION</span></span>
<span data-ttu-id="bb900-108">Mit dem Cmdlet **Start-AzureRmAutomationRunbook** wird ein Azure Automation runbooks-Auftrag gestartet.</span><span class="sxs-lookup"><span data-stu-id="bb900-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="bb900-109">Geben Sie die ID oder den Namen eines runbooks an.</span><span class="sxs-lookup"><span data-stu-id="bb900-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="bb900-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb900-110">EXAMPLES</span></span>

### <span data-ttu-id="bb900-111">Beispiel 1: Starten eines runbooks-Auftrags</span><span class="sxs-lookup"><span data-stu-id="bb900-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bb900-112">Mit diesem Befehl wird ein runbooks-Auftrag für den runbooks mit dem Namen Runbk01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 gestartet.</span><span class="sxs-lookup"><span data-stu-id="bb900-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="bb900-113">Beispiel 2: Starten eines runbooks-Auftrags und warten auf Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="bb900-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="bb900-114">Mit diesem Befehl wird ein runbooks-Auftrag für den runbooks mit dem Namen Runbk01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 gestartet.</span><span class="sxs-lookup"><span data-stu-id="bb900-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="bb900-115">Mit diesem Befehl wird der _Wait_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="bb900-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="bb900-116">Daher gibt Sie Ergebnisse zurück, nachdem der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bb900-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="bb900-117">Das Cmdlet wartet auf bis zu 1000 Sekunden für die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="bb900-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="bb900-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb900-118">PARAMETERS</span></span>

### <span data-ttu-id="bb900-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb900-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="bb900-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb900-120">-DefaultProfile</span></span>
<span data-ttu-id="bb900-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb900-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb900-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="bb900-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="bb900-123">Gibt an, wie viele Sekunden dieses Cmdlet wartet, bis ein Auftrag beendet wird, bevor der Auftrag aufgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bb900-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="bb900-124">Der Standardwert ist 10800 oder drei Stunden.</span><span class="sxs-lookup"><span data-stu-id="bb900-124">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="bb900-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bb900-125">-Name</span></span>
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

### <span data-ttu-id="bb900-126">-Parameter</span><span class="sxs-lookup"><span data-stu-id="bb900-126">-Parameters</span></span>
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

### <span data-ttu-id="bb900-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb900-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="bb900-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="bb900-128">-RunOn</span></span>
<span data-ttu-id="bb900-129">Gibt an, welche Hybrid Arbeitskraft Gruppe für die runbooks ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb900-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="bb900-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="bb900-130">-Wait</span></span>
<span data-ttu-id="bb900-131">Gibt an, dass dieses Cmdlet wartet, bis der Auftrag abgeschlossen, angehalten oder fehlschlägt, und gibt dann die Steuerung an Azure PowerShell zurück.</span><span class="sxs-lookup"><span data-stu-id="bb900-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="bb900-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb900-132">CommonParameters</span></span>
<span data-ttu-id="bb900-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb900-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb900-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb900-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb900-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb900-135">INPUTS</span></span>

### <span data-ttu-id="bb900-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bb900-136">System.String</span></span>

## <span data-ttu-id="bb900-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb900-137">OUTPUTS</span></span>

### <span data-ttu-id="bb900-138">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="bb900-138">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="bb900-139">– Dieses Cmdlet gibt ein **Auftrags** Objekt zurück, es sei denn, Sie geben den _Wait_ -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="bb900-139">-This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>
<span data-ttu-id="bb900-140">-Wenn Sie _Wait_ nicht angeben, gibt Azure PowerShell ein **Auftrags** Objekt sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="bb900-140">-If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="bb900-141">– Wenn Sie _Wait_ angeben, schließt Azure PowerShell den Auftrag ab und gibt dann das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="bb900-141">-If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="bb900-142">– Das Ergebnis ist kein **Auftrags** Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb900-142">-The result is not a **Job** object.</span></span>

### <span data-ttu-id="bb900-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bb900-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bb900-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb900-144">NOTES</span></span>

## <span data-ttu-id="bb900-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb900-145">RELATED LINKS</span></span>

[<span data-ttu-id="bb900-146">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bb900-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bb900-148">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bb900-149">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bb900-150">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bb900-151">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bb900-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bb900-153">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb900-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
