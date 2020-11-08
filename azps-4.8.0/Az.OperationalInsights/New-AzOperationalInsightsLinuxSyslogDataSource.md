---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009623"
---
# <span data-ttu-id="18ace-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="18ace-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="18ace-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18ace-102">SYNOPSIS</span></span>
<span data-ttu-id="18ace-103">Fügt eine Datenquelle zu Linux-Computern hinzu.</span><span class="sxs-lookup"><span data-stu-id="18ace-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="18ace-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18ace-104">SYNTAX</span></span>

### <span data-ttu-id="18ace-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="18ace-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ace-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="18ace-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ace-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18ace-107">DESCRIPTION</span></span>
<span data-ttu-id="18ace-108">Mit dem Cmdlet **New-AzOperationalInsightsLinuxSyslogDataSource** wird eine syslog-Datenquelle zu verbundenen Linux-Computern in einem Arbeitsbereich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="18ace-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="18ace-109">Azure Operational Insights kann syslog-Daten sammeln.</span><span class="sxs-lookup"><span data-stu-id="18ace-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="18ace-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18ace-110">EXAMPLES</span></span>

### <span data-ttu-id="18ace-111">Beispiel 1: Erstellen von syslog-Datenquellen</span><span class="sxs-lookup"><span data-stu-id="18ace-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="18ace-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="18ace-112">PARAMETERS</span></span>

### <span data-ttu-id="18ace-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="18ace-113">-CollectAlert</span></span>
<span data-ttu-id="18ace-114">Gibt an, dass operative Einblicke Benachrichtigungsmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="18ace-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="18ace-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="18ace-115">-CollectCritical</span></span>
<span data-ttu-id="18ace-116">Gibt an, dass operative Einblicke kritische Nachrichten sammelt.</span><span class="sxs-lookup"><span data-stu-id="18ace-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="18ace-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="18ace-117">-CollectDebug</span></span>
<span data-ttu-id="18ace-118">Gibt an, dass operative Einblicke Debug-Nachrichten sammeln.</span><span class="sxs-lookup"><span data-stu-id="18ace-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="18ace-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="18ace-119">-CollectEmergency</span></span>
<span data-ttu-id="18ace-120">Gibt an, dass operative Einblicke Notfallnachrichten sammeln.</span><span class="sxs-lookup"><span data-stu-id="18ace-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="18ace-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="18ace-121">-CollectError</span></span>
<span data-ttu-id="18ace-122">Gibt an, dass operative Einblicke Fehlermeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="18ace-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="18ace-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="18ace-123">-CollectInformational</span></span>
<span data-ttu-id="18ace-124">Gibt an, dass operative Einblicke Informationsnachrichten sammelt.</span><span class="sxs-lookup"><span data-stu-id="18ace-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="18ace-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="18ace-125">-CollectNotice</span></span>
<span data-ttu-id="18ace-126">Gibt an, dass operative Einblicke Benachrichtigungsmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="18ace-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="18ace-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="18ace-127">-CollectWarning</span></span>
<span data-ttu-id="18ace-128">Gibt an, dass der syslog Warnmeldungen enthält.</span><span class="sxs-lookup"><span data-stu-id="18ace-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="18ace-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ace-129">-DefaultProfile</span></span>
<span data-ttu-id="18ace-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="18ace-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18ace-131">-Facility</span><span class="sxs-lookup"><span data-stu-id="18ace-131">-Facility</span></span>
<span data-ttu-id="18ace-132">Gibt einen Facility-Code an.</span><span class="sxs-lookup"><span data-stu-id="18ace-132">Specifies a facility code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ace-133">-Force</span><span class="sxs-lookup"><span data-stu-id="18ace-133">-Force</span></span>
<span data-ttu-id="18ace-134">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="18ace-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18ace-135">-Name</span><span class="sxs-lookup"><span data-stu-id="18ace-135">-Name</span></span>
<span data-ttu-id="18ace-136">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="18ace-136">Specifies a name for the data source.</span></span> <span data-ttu-id="18ace-137">Der Name wird im Azure-Portal nicht verfügbar gemacht, und eine beliebige Zeichenfolge kann verwendet werden, solange Sie eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="18ace-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ace-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ace-138">-ResourceGroupName</span></span>
<span data-ttu-id="18ace-139">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="18ace-139">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ace-140">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="18ace-140">-Workspace</span></span>
<span data-ttu-id="18ace-141">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="18ace-141">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18ace-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="18ace-142">-WorkspaceName</span></span>
<span data-ttu-id="18ace-143">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="18ace-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ace-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18ace-144">-Confirm</span></span>
<span data-ttu-id="18ace-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18ace-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ace-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ace-146">-WhatIf</span></span>
<span data-ttu-id="18ace-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18ace-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18ace-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18ace-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ace-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ace-149">CommonParameters</span></span>
<span data-ttu-id="18ace-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ace-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ace-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ace-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ace-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18ace-152">INPUTS</span></span>

### <span data-ttu-id="18ace-153">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="18ace-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="18ace-154">System. String</span><span class="sxs-lookup"><span data-stu-id="18ace-154">System.String</span></span>

## <span data-ttu-id="18ace-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18ace-155">OUTPUTS</span></span>

### <span data-ttu-id="18ace-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="18ace-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="18ace-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="18ace-157">NOTES</span></span>

## <span data-ttu-id="18ace-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18ace-158">RELATED LINKS</span></span>

[<span data-ttu-id="18ace-159">Deaktivieren-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="18ace-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="18ace-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="18ace-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


