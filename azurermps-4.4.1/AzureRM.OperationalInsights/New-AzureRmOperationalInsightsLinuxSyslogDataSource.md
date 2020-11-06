---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 5729daec656c7f99ac7f4c4c9440e090217c315d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496993"
---
# <span data-ttu-id="6f11d-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="6f11d-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="6f11d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f11d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f11d-103">Fügt eine Datenquelle zu Linux-Computern hinzu.</span><span class="sxs-lookup"><span data-stu-id="6f11d-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f11d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f11d-104">SYNTAX</span></span>

### <span data-ttu-id="6f11d-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f11d-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f11d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6f11d-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f11d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f11d-107">DESCRIPTION</span></span>
<span data-ttu-id="6f11d-108">Mit dem Cmdlet **New-AzureRmOperationalInsightsLinuxSyslogDataSource** wird eine syslog-Datenquelle zu verbundenen Linux-Computern in einem Arbeitsbereich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f11d-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="6f11d-109">Azure Operational Insights kann syslog-Daten sammeln.</span><span class="sxs-lookup"><span data-stu-id="6f11d-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="6f11d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f11d-110">EXAMPLES</span></span>

## <span data-ttu-id="6f11d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f11d-111">PARAMETERS</span></span>

### <span data-ttu-id="6f11d-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="6f11d-112">-CollectAlert</span></span>
<span data-ttu-id="6f11d-113">Gibt an, dass operative Einblicke Benachrichtigungsmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="6f11d-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="6f11d-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="6f11d-114">-CollectCritical</span></span>
<span data-ttu-id="6f11d-115">Gibt an, dass operative Einblicke kritische Nachrichten sammelt.</span><span class="sxs-lookup"><span data-stu-id="6f11d-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="6f11d-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="6f11d-116">-CollectDebug</span></span>
<span data-ttu-id="6f11d-117">Gibt an, dass operative Einblicke Debug-Nachrichten sammeln.</span><span class="sxs-lookup"><span data-stu-id="6f11d-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="6f11d-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="6f11d-118">-CollectEmergency</span></span>
<span data-ttu-id="6f11d-119">Gibt an, dass operative Einblicke Notfallnachrichten sammeln.</span><span class="sxs-lookup"><span data-stu-id="6f11d-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="6f11d-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="6f11d-120">-CollectError</span></span>
<span data-ttu-id="6f11d-121">Gibt an, dass operative Einblicke Fehlermeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="6f11d-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="6f11d-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="6f11d-122">-CollectInformational</span></span>
<span data-ttu-id="6f11d-123">Gibt an, dass operative Einblicke Informationsnachrichten sammelt.</span><span class="sxs-lookup"><span data-stu-id="6f11d-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="6f11d-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="6f11d-124">-CollectNotice</span></span>
<span data-ttu-id="6f11d-125">Gibt an, dass operative Einblicke Benachrichtigungsmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="6f11d-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="6f11d-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="6f11d-126">-CollectWarning</span></span>
<span data-ttu-id="6f11d-127">Gibt an, dass der syslog Warnmeldungen enthält.</span><span class="sxs-lookup"><span data-stu-id="6f11d-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="6f11d-128">-Facility</span><span class="sxs-lookup"><span data-stu-id="6f11d-128">-Facility</span></span>
<span data-ttu-id="6f11d-129">Gibt einen Facility-Code an.</span><span class="sxs-lookup"><span data-stu-id="6f11d-129">Specifies a facility code.</span></span>

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

### <span data-ttu-id="6f11d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6f11d-130">-Force</span></span>
<span data-ttu-id="6f11d-131">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6f11d-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f11d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="6f11d-132">-Name</span></span>
<span data-ttu-id="6f11d-133">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="6f11d-133">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="6f11d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f11d-134">-ResourceGroupName</span></span>
<span data-ttu-id="6f11d-135">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="6f11d-135">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="6f11d-136">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="6f11d-136">-Workspace</span></span>
<span data-ttu-id="6f11d-137">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6f11d-137">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6f11d-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f11d-138">-WorkspaceName</span></span>
<span data-ttu-id="6f11d-139">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6f11d-139">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6f11d-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f11d-140">-Confirm</span></span>
<span data-ttu-id="6f11d-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f11d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f11d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f11d-142">-WhatIf</span></span>
<span data-ttu-id="6f11d-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f11d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f11d-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f11d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f11d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f11d-145">-DefaultProfile</span></span>
<span data-ttu-id="6f11d-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f11d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f11d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f11d-147">CommonParameters</span></span>
<span data-ttu-id="6f11d-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f11d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f11d-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f11d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f11d-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f11d-150">INPUTS</span></span>

### <span data-ttu-id="6f11d-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6f11d-151">PSWorkspace</span></span>
<span data-ttu-id="6f11d-152">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f11d-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="6f11d-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f11d-153">OUTPUTS</span></span>

### <span data-ttu-id="6f11d-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6f11d-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6f11d-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f11d-155">NOTES</span></span>

## <span data-ttu-id="6f11d-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f11d-156">RELATED LINKS</span></span>

[<span data-ttu-id="6f11d-157">Deaktivieren-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6f11d-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="6f11d-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6f11d-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


