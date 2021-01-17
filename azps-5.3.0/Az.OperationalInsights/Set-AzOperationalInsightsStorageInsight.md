---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378564"
---
# <span data-ttu-id="358ee-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="358ee-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="358ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="358ee-102">SYNOPSIS</span></span>
<span data-ttu-id="358ee-103">Aktualisiert einen Speicher-Einblick.</span><span class="sxs-lookup"><span data-stu-id="358ee-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="358ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="358ee-104">SYNTAX</span></span>

### <span data-ttu-id="358ee-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="358ee-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="358ee-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="358ee-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="358ee-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="358ee-107">DESCRIPTION</span></span>
<span data-ttu-id="358ee-108">Das **Cmdlet "Set-AzOperationalInsightsStorageInsight"** ändert die Konfiguration eines Speichereinblicks.</span><span class="sxs-lookup"><span data-stu-id="358ee-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="358ee-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="358ee-109">EXAMPLES</span></span>

### <span data-ttu-id="358ee-110">Beispiel 1: Ändern eines Speicherinblicks nach Name</span><span class="sxs-lookup"><span data-stu-id="358ee-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="358ee-111">Mit diesem Befehl werden die Tabellen geändert, aus denen der Speichersichter "MeineStorageInsight" liest.</span><span class="sxs-lookup"><span data-stu-id="358ee-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="358ee-112">Beispiel 2: Ändern eines Speicherinblicks mithilfe eines Arbeitsbereichsobjekts</span><span class="sxs-lookup"><span data-stu-id="358ee-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="358ee-113">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace Cmdlet, um den Arbeitsbereich "MyWorkspace" zu erhalten, und speichert ihn dann in der $Workspace Variable.</span><span class="sxs-lookup"><span data-stu-id="358ee-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="358ee-114">Der zweite Befehl ändert die Container, aus denen der Speichersichter "MeineStorageInsight" liest.</span><span class="sxs-lookup"><span data-stu-id="358ee-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="358ee-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="358ee-115">PARAMETERS</span></span>

### <span data-ttu-id="358ee-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="358ee-116">-Containers</span></span>
<span data-ttu-id="358ee-117">Gibt die Liste der Container an, die die Daten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="358ee-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358ee-118">-DefaultProfile</span></span>
<span data-ttu-id="358ee-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="358ee-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="358ee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="358ee-120">-Name</span></span>
<span data-ttu-id="358ee-121">Gibt den Namen eines Speicherinblicks an.</span><span class="sxs-lookup"><span data-stu-id="358ee-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="358ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="358ee-123">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="358ee-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="358ee-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="358ee-124">-StorageAccountKey</span></span>
<span data-ttu-id="358ee-125">Gibt den Zugriffsschlüssel für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="358ee-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358ee-126">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="358ee-126">-Tables</span></span>
<span data-ttu-id="358ee-127">Gibt die Liste der Tabellen an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="358ee-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358ee-128">-Workspace</span><span class="sxs-lookup"><span data-stu-id="358ee-128">-Workspace</span></span>
<span data-ttu-id="358ee-129">Gibt den Arbeitsbereich an, der die Speicherinblicke enthält.</span><span class="sxs-lookup"><span data-stu-id="358ee-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="358ee-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="358ee-130">-WorkspaceName</span></span>
<span data-ttu-id="358ee-131">Gibt den Namen eines Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="358ee-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="358ee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358ee-132">CommonParameters</span></span>
<span data-ttu-id="358ee-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358ee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358ee-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358ee-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358ee-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="358ee-135">INPUTS</span></span>

### <span data-ttu-id="358ee-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="358ee-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="358ee-137">System.String</span><span class="sxs-lookup"><span data-stu-id="358ee-137">System.String</span></span>

### <span data-ttu-id="358ee-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="358ee-138">System.String[]</span></span>

## <span data-ttu-id="358ee-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="358ee-139">OUTPUTS</span></span>

### <span data-ttu-id="358ee-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="358ee-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="358ee-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="358ee-141">NOTES</span></span>

## <span data-ttu-id="358ee-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="358ee-142">RELATED LINKS</span></span>

[<span data-ttu-id="358ee-143">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="358ee-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="358ee-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="358ee-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


