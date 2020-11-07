---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: b81d7e7d87e8db7658db425f889630a3897d1ecd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847935"
---
# <span data-ttu-id="c5787-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c5787-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="c5787-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5787-102">SYNOPSIS</span></span>
<span data-ttu-id="c5787-103">Aktualisiert eine Speicher-Insight.</span><span class="sxs-lookup"><span data-stu-id="c5787-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="c5787-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5787-104">SYNTAX</span></span>

### <span data-ttu-id="c5787-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5787-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5787-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c5787-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5787-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5787-107">DESCRIPTION</span></span>
<span data-ttu-id="c5787-108">Das Cmdlet " **Satz-AzOperationalInsightsStorageInsight** " ändert die Konfiguration einer Speicher-Insight.</span><span class="sxs-lookup"><span data-stu-id="c5787-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="c5787-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5787-109">EXAMPLES</span></span>

### <span data-ttu-id="c5787-110">Beispiel 1: Ändern eines Speicher Einblicks anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="c5787-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c5787-111">Mit diesem Befehl werden die Tabellen geändert, aus denen die Speicher Insight mit dem Namen MyStorageInsight liest.</span><span class="sxs-lookup"><span data-stu-id="c5787-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="c5787-112">Beispiel 2: Ändern eines Speicher Einblicks mithilfe eines Workspace-Objekts</span><span class="sxs-lookup"><span data-stu-id="c5787-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="c5787-113">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und speichert ihn dann in der Variablen $Workspace.</span><span class="sxs-lookup"><span data-stu-id="c5787-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="c5787-114">Mit dem zweiten Befehl werden die Container geändert, aus denen die Speicher Insight mit dem Namen MyStorageInsight liest.</span><span class="sxs-lookup"><span data-stu-id="c5787-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="c5787-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5787-115">PARAMETERS</span></span>

### <span data-ttu-id="c5787-116">-Container</span><span class="sxs-lookup"><span data-stu-id="c5787-116">-Containers</span></span>
<span data-ttu-id="c5787-117">Gibt die Liste der Container an, die die Daten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c5787-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="c5787-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5787-118">-DefaultProfile</span></span>
<span data-ttu-id="c5787-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c5787-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5787-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c5787-120">-Name</span></span>
<span data-ttu-id="c5787-121">Gibt den Namen einer Speicher-Insight an.</span><span class="sxs-lookup"><span data-stu-id="c5787-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="c5787-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5787-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5787-123">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="c5787-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c5787-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5787-124">-StorageAccountKey</span></span>
<span data-ttu-id="c5787-125">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="c5787-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="c5787-126">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="c5787-126">-Tables</span></span>
<span data-ttu-id="c5787-127">Gibt die Liste der Tabellen an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5787-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="c5787-128">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="c5787-128">-Workspace</span></span>
<span data-ttu-id="c5787-129">Gibt den Arbeitsbereich an, der den Speicher Einblick enthält.</span><span class="sxs-lookup"><span data-stu-id="c5787-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="c5787-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5787-130">-WorkspaceName</span></span>
<span data-ttu-id="c5787-131">Gibt den Namen eines Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="c5787-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="c5787-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5787-132">CommonParameters</span></span>
<span data-ttu-id="c5787-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5787-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5787-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5787-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5787-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5787-135">INPUTS</span></span>

### <span data-ttu-id="c5787-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5787-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c5787-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c5787-137">System.String</span></span>

### <span data-ttu-id="c5787-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="c5787-138">System.String[]</span></span>

## <span data-ttu-id="c5787-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5787-139">OUTPUTS</span></span>

### <span data-ttu-id="c5787-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c5787-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="c5787-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5787-141">NOTES</span></span>

## <span data-ttu-id="c5787-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5787-142">RELATED LINKS</span></span>

[<span data-ttu-id="c5787-143">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="c5787-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c5787-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5787-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


