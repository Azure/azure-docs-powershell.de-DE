---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: dfdea6498ac7f553dafeea186a8b60f157cbd904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662634"
---
# <span data-ttu-id="958ec-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="958ec-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="958ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="958ec-102">SYNOPSIS</span></span>
<span data-ttu-id="958ec-103">Fügt eine Windows-Leistungsindikator-Datenquelle für verbundene Computer hinzu, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="958ec-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="958ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="958ec-104">SYNTAX</span></span>

### <span data-ttu-id="958ec-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="958ec-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958ec-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="958ec-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="958ec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="958ec-107">DESCRIPTION</span></span>
<span data-ttu-id="958ec-108">Mit dem Cmdlet **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** wird eine Windows-Leistungsindikator-Datenquelle für verbundene Computer hinzugefügt, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="958ec-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="958ec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="958ec-109">EXAMPLES</span></span>

## <span data-ttu-id="958ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="958ec-110">PARAMETERS</span></span>

### <span data-ttu-id="958ec-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="958ec-111">-CounterName</span></span>
<span data-ttu-id="958ec-112">Gibt den Namen eines Indikators an.</span><span class="sxs-lookup"><span data-stu-id="958ec-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958ec-113">-Force</span><span class="sxs-lookup"><span data-stu-id="958ec-113">-Force</span></span>
<span data-ttu-id="958ec-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="958ec-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="958ec-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="958ec-115">-InstanceName</span></span>
<span data-ttu-id="958ec-116">Gibt den Namen einer Instanz an.</span><span class="sxs-lookup"><span data-stu-id="958ec-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="958ec-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="958ec-117">-IntervalSeconds</span></span>
<span data-ttu-id="958ec-118">Gibt das Intervall der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="958ec-118">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958ec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="958ec-119">-Name</span></span>
<span data-ttu-id="958ec-120">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="958ec-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="958ec-121">-Objektname</span><span class="sxs-lookup"><span data-stu-id="958ec-121">-ObjectName</span></span>
<span data-ttu-id="958ec-122">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="958ec-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="958ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="958ec-124">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="958ec-124">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="958ec-125">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="958ec-125">-UseLegacyCollector</span></span>
<span data-ttu-id="958ec-126">Verwenden Sie den Legacy-Kollektor oder den Standard Kollektor.</span><span class="sxs-lookup"><span data-stu-id="958ec-126">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="958ec-127">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="958ec-127">-Workspace</span></span>
<span data-ttu-id="958ec-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="958ec-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="958ec-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="958ec-129">-WorkspaceName</span></span>
<span data-ttu-id="958ec-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="958ec-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="958ec-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="958ec-131">-Confirm</span></span>
<span data-ttu-id="958ec-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="958ec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="958ec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="958ec-133">-WhatIf</span></span>
<span data-ttu-id="958ec-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="958ec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="958ec-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="958ec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="958ec-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958ec-136">-DefaultProfile</span></span>
<span data-ttu-id="958ec-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="958ec-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="958ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958ec-138">CommonParameters</span></span>
<span data-ttu-id="958ec-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958ec-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958ec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958ec-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="958ec-141">INPUTS</span></span>

### <span data-ttu-id="958ec-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="958ec-142">PSWorkspace</span></span>
<span data-ttu-id="958ec-143">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="958ec-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="958ec-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="958ec-144">OUTPUTS</span></span>

### <span data-ttu-id="958ec-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="958ec-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="958ec-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="958ec-146">NOTES</span></span>

## <span data-ttu-id="958ec-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="958ec-147">RELATED LINKS</span></span>

