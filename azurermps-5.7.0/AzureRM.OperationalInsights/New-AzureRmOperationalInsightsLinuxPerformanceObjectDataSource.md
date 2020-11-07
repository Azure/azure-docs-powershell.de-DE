---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: decae9e9282ad85832df676162f6bc684684f339
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665177"
---
# <span data-ttu-id="a2841-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="a2841-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="a2841-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2841-102">SYNOPSIS</span></span>
<span data-ttu-id="a2841-103">Fügt allen Linux-Computern in einem Arbeitsbereich Leistungsindikatoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2841-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2841-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2841-104">SYNTAX</span></span>

### <span data-ttu-id="a2841-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2841-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2841-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a2841-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2841-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2841-107">DESCRIPTION</span></span>
<span data-ttu-id="a2841-108">Das Cmdlet **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** fügt Leistungsindikatoren hinzu, aus denen Azure Operational Insights Daten auf allen Linux-Computern in einem Arbeitsbereich sammelt.</span><span class="sxs-lookup"><span data-stu-id="a2841-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="a2841-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2841-109">EXAMPLES</span></span>

## <span data-ttu-id="a2841-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2841-110">PARAMETERS</span></span>

### <span data-ttu-id="a2841-111">-Gegen Namen</span><span class="sxs-lookup"><span data-stu-id="a2841-111">-CounterNames</span></span>
<span data-ttu-id="a2841-112">Gibt ein Array mit Namen von Zählern an.</span><span class="sxs-lookup"><span data-stu-id="a2841-112">Specifies an array of names of counters.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2841-113">-DefaultProfile</span></span>
<span data-ttu-id="a2841-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a2841-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a2841-115">-Force</span></span>
<span data-ttu-id="a2841-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a2841-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a2841-117">-InstanceName</span></span>
<span data-ttu-id="a2841-118">Gibt den Namen einer Instanz an.</span><span class="sxs-lookup"><span data-stu-id="a2841-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="a2841-119">-IntervalSeconds</span></span>
<span data-ttu-id="a2841-120">Gibt das Intervall der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="a2841-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2841-121">-Name</span></span>
<span data-ttu-id="a2841-122">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="a2841-122">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-123">-Objektname</span><span class="sxs-lookup"><span data-stu-id="a2841-123">-ObjectName</span></span>
<span data-ttu-id="a2841-124">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="a2841-124">Specifies the name of an object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2841-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2841-126">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="a2841-126">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-127">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a2841-127">-Workspace</span></span>
<span data-ttu-id="a2841-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a2841-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2841-129">-WorkspaceName</span></span>
<span data-ttu-id="a2841-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a2841-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2841-131">-Confirm</span></span>
<span data-ttu-id="a2841-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2841-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2841-133">-WhatIf</span></span>
<span data-ttu-id="a2841-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2841-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2841-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2841-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2841-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2841-136">CommonParameters</span></span>
<span data-ttu-id="a2841-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2841-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2841-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2841-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2841-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2841-139">INPUTS</span></span>

### <span data-ttu-id="a2841-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2841-140">PSWorkspace</span></span>
<span data-ttu-id="a2841-141">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2841-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a2841-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2841-142">OUTPUTS</span></span>

### <span data-ttu-id="a2841-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a2841-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a2841-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2841-144">NOTES</span></span>

## <span data-ttu-id="a2841-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2841-145">RELATED LINKS</span></span>

[<span data-ttu-id="a2841-146">Deaktivieren-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="a2841-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="a2841-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="a2841-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


