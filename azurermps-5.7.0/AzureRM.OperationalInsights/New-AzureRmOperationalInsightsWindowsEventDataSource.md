---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: cebbcb0526c35fb803de783604db291612694baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481053"
---
# <span data-ttu-id="bf873-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="bf873-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="bf873-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf873-102">SYNOPSIS</span></span>
<span data-ttu-id="bf873-103">Sammelt Ereignisprotokolle von Computern, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf873-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf873-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf873-104">SYNTAX</span></span>

### <span data-ttu-id="bf873-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf873-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf873-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bf873-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf873-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf873-107">DESCRIPTION</span></span>
<span data-ttu-id="bf873-108">Das Cmdlet **New-AzureRmOperationalInsightsWindowsEventDataSource** fügt eine Datenquelle hinzu, die Windows-Ereignisprotokolle von verbundenen Computern, auf denen das BetriebssystemWindows ausgeführt wird, in Azure Operating Insights sammelt.</span><span class="sxs-lookup"><span data-stu-id="bf873-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="bf873-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf873-109">EXAMPLES</span></span>

## <span data-ttu-id="bf873-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf873-110">PARAMETERS</span></span>

### <span data-ttu-id="bf873-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="bf873-111">-CollectErrors</span></span>
<span data-ttu-id="bf873-112">Gibt an, dass operative Einblicke Fehlermeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="bf873-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="bf873-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="bf873-113">-CollectInformation</span></span>
<span data-ttu-id="bf873-114">Gibt an, dass operative Einblicke Informationsnachrichten sammelt.</span><span class="sxs-lookup"><span data-stu-id="bf873-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="bf873-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="bf873-115">-CollectWarnings</span></span>
<span data-ttu-id="bf873-116">Gibt an, dass operative Einblicke Warnmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="bf873-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="bf873-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf873-117">-DefaultProfile</span></span>
<span data-ttu-id="bf873-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bf873-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf873-119">-Eventlogname</span><span class="sxs-lookup"><span data-stu-id="bf873-119">-EventLogName</span></span>
<span data-ttu-id="bf873-120">Gibt den Namen des Ereignisprotokolls an.</span><span class="sxs-lookup"><span data-stu-id="bf873-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="bf873-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bf873-121">-Force</span></span>
<span data-ttu-id="bf873-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="bf873-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf873-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bf873-123">-Name</span></span>
<span data-ttu-id="bf873-124">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="bf873-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="bf873-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf873-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf873-126">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="bf873-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="bf873-127">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="bf873-127">-Workspace</span></span>
<span data-ttu-id="bf873-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bf873-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bf873-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bf873-129">-WorkspaceName</span></span>
<span data-ttu-id="bf873-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bf873-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bf873-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf873-131">-Confirm</span></span>
<span data-ttu-id="bf873-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf873-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf873-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf873-133">-WhatIf</span></span>
<span data-ttu-id="bf873-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf873-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf873-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf873-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf873-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf873-136">CommonParameters</span></span>
<span data-ttu-id="bf873-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf873-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf873-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf873-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf873-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf873-139">INPUTS</span></span>

### <span data-ttu-id="bf873-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf873-140">PSWorkspace</span></span>
<span data-ttu-id="bf873-141">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf873-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bf873-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf873-142">OUTPUTS</span></span>

### <span data-ttu-id="bf873-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bf873-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bf873-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf873-144">NOTES</span></span>

## <span data-ttu-id="bf873-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf873-145">RELATED LINKS</span></span>

