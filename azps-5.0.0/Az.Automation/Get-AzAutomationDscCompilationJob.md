---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176338"
---
# <span data-ttu-id="404dc-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="404dc-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="404dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="404dc-102">SYNOPSIS</span></span>
<span data-ttu-id="404dc-103">Ruft DSC-Kompilierungsaufträge in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="404dc-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="404dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="404dc-104">SYNTAX</span></span>

### <span data-ttu-id="404dc-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="404dc-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="404dc-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="404dc-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="404dc-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="404dc-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="404dc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="404dc-108">DESCRIPTION</span></span>
<span data-ttu-id="404dc-109">Das Cmdlet " **Get-AzAutomationDscCompilationJob** " ruft APS-Kompilierungsaufträge (Desired State Configuration, DSC) in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="404dc-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="404dc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="404dc-110">EXAMPLES</span></span>

### <span data-ttu-id="404dc-111">Beispiel 1: Abrufen aller DSC-Kompilierungsaufträge</span><span class="sxs-lookup"><span data-stu-id="404dc-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="404dc-112">Dieser Befehl ruft alle Kompilierungsaufträge im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="404dc-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="404dc-113">Beispiel 2: Abrufen von DSC-Kompilierungs Aufträgen für eine Konfiguration</span><span class="sxs-lookup"><span data-stu-id="404dc-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="404dc-114">Dieser Befehl ruft alle Kompilierungsaufträge für die DSC-Konfiguration mit dem Namen ContosoConfiguration im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="404dc-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="404dc-115">Beispiel 3: Abrufen eines bestimmten DSC-Kompilierungs Auftrags</span><span class="sxs-lookup"><span data-stu-id="404dc-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="404dc-116">Dieser Befehl ruft den Kompilierungs Auftrag mit der angegebenen ID im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="404dc-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="404dc-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="404dc-117">PARAMETERS</span></span>

### <span data-ttu-id="404dc-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="404dc-118">-AutomationAccountName</span></span>
<span data-ttu-id="404dc-119">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Kompilierungsaufträge enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="404dc-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="404dc-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="404dc-120">-ConfigurationName</span></span>
<span data-ttu-id="404dc-121">Gibt den Namen der DSC-Konfiguration an, für die dieses Cmdlet Kompilierungsaufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="404dc-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="404dc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404dc-122">-DefaultProfile</span></span>
<span data-ttu-id="404dc-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="404dc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="404dc-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="404dc-124">-EndTime</span></span>
<span data-ttu-id="404dc-125">Gibt eine Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="404dc-125">Specifies an end time.</span></span>
<span data-ttu-id="404dc-126">Dieses Cmdlet ruft Kompilierungsaufträge ab, die bis zu dem von diesem Parameter festgelegten Zeitpunkt gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="404dc-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="404dc-127">-ID</span><span class="sxs-lookup"><span data-stu-id="404dc-127">-Id</span></span>
<span data-ttu-id="404dc-128">Gibt die eindeutige ID des DSC-Kompilierungs Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="404dc-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="404dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="404dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="404dc-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet DSC-Kompilierungsaufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="404dc-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="404dc-131">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="404dc-131">-StartTime</span></span>
<span data-ttu-id="404dc-132">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="404dc-132">Specifies a start time.</span></span>
<span data-ttu-id="404dc-133">Dieses Cmdlet ruft Aufträge ab, die am oder nach dem von diesem Parameter festgelegten Zeitpunkt beginnen.</span><span class="sxs-lookup"><span data-stu-id="404dc-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="404dc-134">-Status</span><span class="sxs-lookup"><span data-stu-id="404dc-134">-Status</span></span>
<span data-ttu-id="404dc-135">Gibt den Status von Aufträgen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="404dc-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="404dc-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="404dc-136">Valid values are:</span></span> 
- <span data-ttu-id="404dc-137">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="404dc-137">Completed</span></span> 
- <span data-ttu-id="404dc-138">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="404dc-138">Failed</span></span> 
- <span data-ttu-id="404dc-139">Queued</span><span class="sxs-lookup"><span data-stu-id="404dc-139">Queued</span></span> 
- <span data-ttu-id="404dc-140">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="404dc-140">Starting</span></span> 
- <span data-ttu-id="404dc-141">Wieder</span><span class="sxs-lookup"><span data-stu-id="404dc-141">Resuming</span></span> 
- <span data-ttu-id="404dc-142">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="404dc-142">Running</span></span> 
- <span data-ttu-id="404dc-143">Funktioniert nicht mehr</span><span class="sxs-lookup"><span data-stu-id="404dc-143">Stopped</span></span> 
- <span data-ttu-id="404dc-144">Beenden</span><span class="sxs-lookup"><span data-stu-id="404dc-144">Stopping</span></span> 
- <span data-ttu-id="404dc-145">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="404dc-145">Suspended</span></span> 
- <span data-ttu-id="404dc-146">Suspending</span><span class="sxs-lookup"><span data-stu-id="404dc-146">Suspending</span></span> 
- <span data-ttu-id="404dc-147">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="404dc-147">Activating</span></span>
- <span data-ttu-id="404dc-148">Neu</span><span class="sxs-lookup"><span data-stu-id="404dc-148">New</span></span>

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

### <span data-ttu-id="404dc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404dc-149">CommonParameters</span></span>
<span data-ttu-id="404dc-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404dc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404dc-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="404dc-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404dc-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="404dc-152">INPUTS</span></span>

### <span data-ttu-id="404dc-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="404dc-153">System.Guid</span></span>

### <span data-ttu-id="404dc-154">System. String</span><span class="sxs-lookup"><span data-stu-id="404dc-154">System.String</span></span>

## <span data-ttu-id="404dc-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="404dc-155">OUTPUTS</span></span>

### <span data-ttu-id="404dc-156">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="404dc-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="404dc-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="404dc-157">NOTES</span></span>

## <span data-ttu-id="404dc-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="404dc-158">RELATED LINKS</span></span>

[<span data-ttu-id="404dc-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="404dc-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="404dc-160">Anfang-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="404dc-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


