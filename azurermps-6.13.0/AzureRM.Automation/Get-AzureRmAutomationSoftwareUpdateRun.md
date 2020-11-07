---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d49d99f8edd3ffe0c25886447eac0bbd15837fc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663693"
---
# <span data-ttu-id="4815d-101">Get-AzureRmAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4815d-101">Get-AzureRmAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="4815d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4815d-102">SYNOPSIS</span></span>
<span data-ttu-id="4815d-103">Ruft eine Liste der Azure-Automatisierungs-Software Update Läufe ab.</span><span class="sxs-lookup"><span data-stu-id="4815d-103">Gets a list of azure automation software update runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4815d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4815d-104">SYNTAX</span></span>

### <span data-ttu-id="4815d-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="4815d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>]
 [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4815d-106">ById</span><span class="sxs-lookup"><span data-stu-id="4815d-106">ById</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4815d-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="4815d-107">BySucName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4815d-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="4815d-108">BySuc</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4815d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4815d-109">DESCRIPTION</span></span>
<span data-ttu-id="4815d-110">Das Get-AzureRmAutomationSoftwareUpdateRun-Cmdlet gibt eine Liste der Software Update Läufe zurück.</span><span class="sxs-lookup"><span data-stu-id="4815d-110">The Get-AzureRmAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="4815d-111">Da eine Software Update-Konfiguration einen zugeordneten Zeitplan aufweist, kann Sie mehrmals ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4815d-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="4815d-112">Jedes Mal, wenn ein Terminplan ausgelöst wird, wird ein Update-Durchlauf erstellt.</span><span class="sxs-lookup"><span data-stu-id="4815d-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="4815d-113">Update Run ist ein Aggregat des Ergebnisses aller Computer Läufe.</span><span class="sxs-lookup"><span data-stu-id="4815d-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="4815d-114">Sie können Runs für eine bestimmte Software Update Konfiguration abrufen, indem Sie den SoftwareUpdateConfigurationName-Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4815d-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="4815d-115">Um eine bestimmte Ausführung zu erhalten, müssen Sie den Name-Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4815d-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="4815d-116">Sie können auch Runs mit einem bestimmten Status auflisten, auf ein bestimmtes operatins-System Zielen oder nach einer bestimmten Zeit gestartete Läufe ausführen, indem Sie den entsprechenden Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4815d-116">You can also list runs with specific status, runs targeting specific operatins system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="4815d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4815d-117">EXAMPLES</span></span>

### <span data-ttu-id="4815d-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4815d-118">Example 1</span></span>
<span data-ttu-id="4815d-119">In diesem Beispiel werden alle Aktualisierungs Läufe aufgelistet, die von einer bestimmten Software Update Konfiguration ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4815d-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="4815d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4815d-120">PARAMETERS</span></span>

### <span data-ttu-id="4815d-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4815d-121">-AutomationAccountName</span></span>
<span data-ttu-id="4815d-122">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="4815d-122">The automation account name.</span></span>

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

### <span data-ttu-id="4815d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4815d-123">-DefaultProfile</span></span>
<span data-ttu-id="4815d-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4815d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4815d-125">-ID</span><span class="sxs-lookup"><span data-stu-id="4815d-125">-Id</span></span>
<span data-ttu-id="4815d-126">Die ID des Software Update-Konfigurations Laufs.</span><span class="sxs-lookup"><span data-stu-id="4815d-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4815d-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4815d-127">-OperatingSystem</span></span>
<span data-ttu-id="4815d-128">Das Betriebssystem des Laufs.</span><span class="sxs-lookup"><span data-stu-id="4815d-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4815d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4815d-129">-ResourceGroupName</span></span>
<span data-ttu-id="4815d-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4815d-130">The resource group name.</span></span>

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

### <span data-ttu-id="4815d-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="4815d-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="4815d-132">Die Software-Update-Konfiguration hat die Ausführung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4815d-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4815d-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4815d-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="4815d-134">Der Name der Software Update Konfiguration hat die Ausführung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4815d-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4815d-135">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="4815d-135">-StartTime</span></span>
<span data-ttu-id="4815d-136">Minimale Startzeit des Laufs.</span><span class="sxs-lookup"><span data-stu-id="4815d-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4815d-137">-Status</span><span class="sxs-lookup"><span data-stu-id="4815d-137">-Status</span></span>
<span data-ttu-id="4815d-138">Der Status des Laufs.</span><span class="sxs-lookup"><span data-stu-id="4815d-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4815d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4815d-139">CommonParameters</span></span>
<span data-ttu-id="4815d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4815d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4815d-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4815d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4815d-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4815d-142">INPUTS</span></span>

### <span data-ttu-id="4815d-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4815d-143">System.Guid</span></span>

### <span data-ttu-id="4815d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4815d-144">System.String</span></span>

### <span data-ttu-id="4815d-145">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="4815d-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="4815d-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. operatingtype, Microsoft. Azure. Commands. ResourceManager. Automation, Version = 5.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4815d-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4815d-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. Commands. ResourceManager. Automation, Version = 5.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4815d-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4815d-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4815d-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="4815d-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4815d-149">OUTPUTS</span></span>

### <span data-ttu-id="4815d-150">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4815d-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="4815d-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="4815d-151">NOTES</span></span>

## <span data-ttu-id="4815d-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4815d-152">RELATED LINKS</span></span>
