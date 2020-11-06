---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500957"
---
# <span data-ttu-id="96f82-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="96f82-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="96f82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96f82-102">SYNOPSIS</span></span>
<span data-ttu-id="96f82-103">Ruft DSC-Kompilierungsaufträge in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="96f82-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96f82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96f82-104">SYNTAX</span></span>

### <span data-ttu-id="96f82-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="96f82-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96f82-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="96f82-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96f82-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="96f82-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96f82-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96f82-108">DESCRIPTION</span></span>
<span data-ttu-id="96f82-109">Das Cmdlet " **Get-AzureRmAutomationDscCompilationJob** " ruft APS-Kompilierungsaufträge (Desired State Configuration, DSC) in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="96f82-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="96f82-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96f82-110">EXAMPLES</span></span>

### <span data-ttu-id="96f82-111">Beispiel 1: Abrufen aller DSC-Kompilierungsaufträge</span><span class="sxs-lookup"><span data-stu-id="96f82-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="96f82-112">Dieser Befehl ruft alle Kompilierungsaufträge im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="96f82-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="96f82-113">Beispiel 2: Abrufen von DSC-Kompilierungs Aufträgen für eine Konfiguration</span><span class="sxs-lookup"><span data-stu-id="96f82-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="96f82-114">Dieser Befehl ruft alle Kompilierungsaufträge für die DSC-Konfiguration mit dem Namen ContosoConfiguration im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="96f82-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="96f82-115">Beispiel 3: Abrufen eines bestimmten DSC-Kompilierungs Auftrags</span><span class="sxs-lookup"><span data-stu-id="96f82-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="96f82-116">Dieser Befehl ruft den Kompilierungs Auftrag mit der angegebenen ID im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="96f82-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="96f82-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="96f82-117">PARAMETERS</span></span>

### <span data-ttu-id="96f82-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="96f82-118">-AutomationAccountName</span></span>
<span data-ttu-id="96f82-119">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Kompilierungsaufträge enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="96f82-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="96f82-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="96f82-120">-ConfigurationName</span></span>
<span data-ttu-id="96f82-121">Gibt den Namen der DSC-Konfiguration an, für die dieses Cmdlet Kompilierungsaufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="96f82-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="96f82-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="96f82-122">-EndTime</span></span>
<span data-ttu-id="96f82-123">Gibt eine Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="96f82-123">Specifies an end time.</span></span>
<span data-ttu-id="96f82-124">Dieses Cmdlet ruft Kompilierungsaufträge ab, die bis zu dem von diesem Parameter festgelegten Zeitpunkt gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="96f82-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="96f82-125">-ID</span><span class="sxs-lookup"><span data-stu-id="96f82-125">-Id</span></span>
<span data-ttu-id="96f82-126">Gibt die eindeutige ID des DSC-Kompilierungs Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="96f82-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="96f82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f82-127">-ResourceGroupName</span></span>
<span data-ttu-id="96f82-128">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet DSC-Kompilierungsaufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="96f82-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="96f82-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="96f82-129">-StartTime</span></span>
<span data-ttu-id="96f82-130">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="96f82-130">Specifies a start time.</span></span>
<span data-ttu-id="96f82-131">Dieses Cmdlet ruft Aufträge ab, die am oder nach dem von diesem Parameter festgelegten Zeitpunkt beginnen.</span><span class="sxs-lookup"><span data-stu-id="96f82-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="96f82-132">-Status</span><span class="sxs-lookup"><span data-stu-id="96f82-132">-Status</span></span>
<span data-ttu-id="96f82-133">Gibt den Status von Aufträgen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="96f82-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="96f82-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="96f82-134">Valid values are:</span></span> 

- <span data-ttu-id="96f82-135">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="96f82-135">Completed</span></span> 
- <span data-ttu-id="96f82-136">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="96f82-136">Failed</span></span> 
- <span data-ttu-id="96f82-137">Queued</span><span class="sxs-lookup"><span data-stu-id="96f82-137">Queued</span></span> 
- <span data-ttu-id="96f82-138">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="96f82-138">Starting</span></span> 
- <span data-ttu-id="96f82-139">Wieder</span><span class="sxs-lookup"><span data-stu-id="96f82-139">Resuming</span></span> 
- <span data-ttu-id="96f82-140">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="96f82-140">Running</span></span> 
- <span data-ttu-id="96f82-141">Funktioniert nicht mehr</span><span class="sxs-lookup"><span data-stu-id="96f82-141">Stopped</span></span> 
- <span data-ttu-id="96f82-142">Beenden</span><span class="sxs-lookup"><span data-stu-id="96f82-142">Stopping</span></span> 
- <span data-ttu-id="96f82-143">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="96f82-143">Suspended</span></span> 
- <span data-ttu-id="96f82-144">Suspending</span><span class="sxs-lookup"><span data-stu-id="96f82-144">Suspending</span></span> 
- <span data-ttu-id="96f82-145">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="96f82-145">Activating</span></span>
- <span data-ttu-id="96f82-146">Neu</span><span class="sxs-lookup"><span data-stu-id="96f82-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f82-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f82-147">-DefaultProfile</span></span>
<span data-ttu-id="96f82-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96f82-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96f82-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f82-149">CommonParameters</span></span>
<span data-ttu-id="96f82-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f82-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f82-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96f82-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f82-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96f82-152">INPUTS</span></span>

## <span data-ttu-id="96f82-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96f82-153">OUTPUTS</span></span>

### <span data-ttu-id="96f82-154">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="96f82-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="96f82-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="96f82-155">NOTES</span></span>

## <span data-ttu-id="96f82-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96f82-156">RELATED LINKS</span></span>

[<span data-ttu-id="96f82-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="96f82-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="96f82-158">Anfang-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="96f82-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


