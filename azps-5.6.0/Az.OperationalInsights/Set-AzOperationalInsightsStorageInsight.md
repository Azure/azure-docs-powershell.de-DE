---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: c2a622b110bdc17fe325934b50c59ac7e9b8f3ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937816"
---
# <span data-ttu-id="631d6-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="631d6-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="631d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631d6-102">SYNOPSIS</span></span>
<span data-ttu-id="631d6-103">Aktualisiert eine Speicherinblicke.</span><span class="sxs-lookup"><span data-stu-id="631d6-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="631d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="631d6-104">SYNTAX</span></span>

### <span data-ttu-id="631d6-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="631d6-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="631d6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="631d6-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="631d6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="631d6-107">DESCRIPTION</span></span>
<span data-ttu-id="631d6-108">Das **Cmdlet Set-AzOperationalInsightsStorageInsight** ändert die Konfiguration einer Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="631d6-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="631d6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="631d6-109">EXAMPLES</span></span>

### <span data-ttu-id="631d6-110">Beispiel 1: Ändern einer Speicheraufschluss nach Name</span><span class="sxs-lookup"><span data-stu-id="631d6-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="631d6-111">Mit diesem Befehl werden die Tabellen geändert, aus denen die Storage Insight namens MyStorageInsight gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="631d6-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="631d6-112">Beispiel 2: Ändern einer Speicheraufschlussansicht mithilfe eines Arbeitsbereichsobjekts</span><span class="sxs-lookup"><span data-stu-id="631d6-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="631d6-113">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen MyWorkspace zu erhalten, und speichert ihn dann in der $Workspace-Variable.</span><span class="sxs-lookup"><span data-stu-id="631d6-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="631d6-114">Mit dem zweiten Befehl werden die Container geändert, aus denen die Storage Insight namens MyStorageInsight gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="631d6-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="631d6-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="631d6-115">PARAMETERS</span></span>

### <span data-ttu-id="631d6-116">-Container</span><span class="sxs-lookup"><span data-stu-id="631d6-116">-Containers</span></span>
<span data-ttu-id="631d6-117">Gibt die Liste der Container an, die die Daten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="631d6-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="631d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631d6-118">-DefaultProfile</span></span>
<span data-ttu-id="631d6-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="631d6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="631d6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="631d6-120">-Name</span></span>
<span data-ttu-id="631d6-121">Gibt den Namen einer Storage Insight an.</span><span class="sxs-lookup"><span data-stu-id="631d6-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="631d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="631d6-123">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="631d6-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="631d6-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="631d6-124">-StorageAccountKey</span></span>
<span data-ttu-id="631d6-125">Gibt den Zugriffsschlüssel für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="631d6-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="631d6-126">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="631d6-126">-Tables</span></span>
<span data-ttu-id="631d6-127">Gibt die Liste der Tabellen an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="631d6-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="631d6-128">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="631d6-128">-Workspace</span></span>
<span data-ttu-id="631d6-129">Gibt den Arbeitsbereich an, der die Storage Insight enthält.</span><span class="sxs-lookup"><span data-stu-id="631d6-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="631d6-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="631d6-130">-WorkspaceName</span></span>
<span data-ttu-id="631d6-131">Gibt den Namen eines Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="631d6-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="631d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631d6-132">CommonParameters</span></span>
<span data-ttu-id="631d6-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631d6-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="631d6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631d6-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="631d6-135">INPUTS</span></span>

### <span data-ttu-id="631d6-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="631d6-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="631d6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="631d6-137">System.String</span></span>

### <span data-ttu-id="631d6-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="631d6-138">System.String[]</span></span>

## <span data-ttu-id="631d6-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="631d6-139">OUTPUTS</span></span>

### <span data-ttu-id="631d6-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="631d6-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="631d6-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="631d6-141">NOTES</span></span>

## <span data-ttu-id="631d6-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="631d6-142">RELATED LINKS</span></span>

[<span data-ttu-id="631d6-143">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="631d6-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="631d6-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="631d6-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


