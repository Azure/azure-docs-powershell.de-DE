---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5157b4d4e1a291193f10fef22308002de210e748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939760"
---
# <span data-ttu-id="f4e63-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f4e63-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="f4e63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e63-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e63-103">Ruft DSC-Kompilierungsaufträge in automation ab.</span><span class="sxs-lookup"><span data-stu-id="f4e63-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="f4e63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4e63-104">SYNTAX</span></span>

### <span data-ttu-id="f4e63-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4e63-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4e63-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="f4e63-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e63-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f4e63-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e63-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4e63-108">DESCRIPTION</span></span>
<span data-ttu-id="f4e63-109">Das **Get-AzAutomationDscCompilationJob-Cmdlet** ruft APS-Kompilierungsaufträge (Desired State Configuration, DSC) in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="f4e63-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="f4e63-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4e63-110">EXAMPLES</span></span>

### <span data-ttu-id="f4e63-111">Beispiel 1: Alle DSC-Kompilierungsaufträge erhalten</span><span class="sxs-lookup"><span data-stu-id="f4e63-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f4e63-112">Dieser Befehl ruft alle Kompilierungsaufträge im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="f4e63-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f4e63-113">Beispiel 2: Erhalten von DSC-Kompilierungsaufträgen für eine Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f4e63-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="f4e63-114">Dieser Befehl ruft alle Kompilierungsaufträge für die DSC-Konfiguration namens ContosoConfiguration im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="f4e63-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f4e63-115">Beispiel 3: Erhalten eines bestimmten DSC-Kompilierungsauftrags</span><span class="sxs-lookup"><span data-stu-id="f4e63-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="f4e63-116">Dieser Befehl ruft den Kompilierungsauftrag mit der angegebenen ID im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="f4e63-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f4e63-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4e63-117">PARAMETERS</span></span>

### <span data-ttu-id="f4e63-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4e63-118">-AutomationAccountName</span></span>
<span data-ttu-id="f4e63-119">Gibt den Namen des Automatisierungskontos an, das DSC-Kompilierungsaufträge enthält, die von diesem Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f4e63-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4e63-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f4e63-120">-ConfigurationName</span></span>
<span data-ttu-id="f4e63-121">Gibt den Namen der DSC-Konfiguration an, für die dieses Cmdlet Kompilierungsaufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="f4e63-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e63-122">-DefaultProfile</span></span>
<span data-ttu-id="f4e63-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f4e63-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4e63-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f4e63-124">-EndTime</span></span>
<span data-ttu-id="f4e63-125">Gibt eine Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="f4e63-125">Specifies an end time.</span></span>
<span data-ttu-id="f4e63-126">Dieses Cmdlet ruft Kompilierungsaufträge ab, die bis zu dem Von diesem Parameter angegebenen Zeitpunkt gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="f4e63-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e63-127">-ID</span><span class="sxs-lookup"><span data-stu-id="f4e63-127">-Id</span></span>
<span data-ttu-id="f4e63-128">Gibt die eindeutige ID des DSC-Kompilierungsauftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f4e63-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e63-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e63-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4e63-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet DSC-Kompilierungsaufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="f4e63-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="f4e63-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f4e63-131">-StartTime</span></span>
<span data-ttu-id="f4e63-132">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="f4e63-132">Specifies a start time.</span></span>
<span data-ttu-id="f4e63-133">Dieses Cmdlet ruft Aufträge ab, die zu oder nach dem von diesem Parameter angegebenen Zeitpunkt beginnen.</span><span class="sxs-lookup"><span data-stu-id="f4e63-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e63-134">-Status</span><span class="sxs-lookup"><span data-stu-id="f4e63-134">-Status</span></span>
<span data-ttu-id="f4e63-135">Gibt den Status von Aufträgen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f4e63-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f4e63-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f4e63-136">Valid values are:</span></span> 
- <span data-ttu-id="f4e63-137">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="f4e63-137">Completed</span></span> 
- <span data-ttu-id="f4e63-138">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="f4e63-138">Failed</span></span> 
- <span data-ttu-id="f4e63-139">In warteschlangen</span><span class="sxs-lookup"><span data-stu-id="f4e63-139">Queued</span></span> 
- <span data-ttu-id="f4e63-140">Starten</span><span class="sxs-lookup"><span data-stu-id="f4e63-140">Starting</span></span> 
- <span data-ttu-id="f4e63-141">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="f4e63-141">Resuming</span></span> 
- <span data-ttu-id="f4e63-142">Ausführen</span><span class="sxs-lookup"><span data-stu-id="f4e63-142">Running</span></span> 
- <span data-ttu-id="f4e63-143">Beendet</span><span class="sxs-lookup"><span data-stu-id="f4e63-143">Stopped</span></span> 
- <span data-ttu-id="f4e63-144">Beenden</span><span class="sxs-lookup"><span data-stu-id="f4e63-144">Stopping</span></span> 
- <span data-ttu-id="f4e63-145">Angehalten</span><span class="sxs-lookup"><span data-stu-id="f4e63-145">Suspended</span></span> 
- <span data-ttu-id="f4e63-146">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f4e63-146">Suspending</span></span> 
- <span data-ttu-id="f4e63-147">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="f4e63-147">Activating</span></span>
- <span data-ttu-id="f4e63-148">Neu</span><span class="sxs-lookup"><span data-stu-id="f4e63-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e63-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e63-149">CommonParameters</span></span>
<span data-ttu-id="f4e63-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e63-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e63-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e63-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e63-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4e63-152">INPUTS</span></span>

### <span data-ttu-id="f4e63-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f4e63-153">System.Guid</span></span>

### <span data-ttu-id="f4e63-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f4e63-154">System.String</span></span>

## <span data-ttu-id="f4e63-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4e63-155">OUTPUTS</span></span>

### <span data-ttu-id="f4e63-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f4e63-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f4e63-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4e63-157">NOTES</span></span>

## <span data-ttu-id="f4e63-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4e63-158">RELATED LINKS</span></span>

[<span data-ttu-id="f4e63-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f4e63-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="f4e63-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f4e63-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


