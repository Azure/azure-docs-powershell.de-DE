---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 460a1585c8c6c556f0044b9cd0673a3be750ffe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662668"
---
# <span data-ttu-id="cc980-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="cc980-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="cc980-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc980-102">SYNOPSIS</span></span>
<span data-ttu-id="cc980-103">Aktualisiert eine Speicher-Insight.</span><span class="sxs-lookup"><span data-stu-id="cc980-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc980-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc980-104">SYNTAX</span></span>

### <span data-ttu-id="cc980-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc980-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc980-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cc980-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc980-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc980-107">DESCRIPTION</span></span>
<span data-ttu-id="cc980-108">Das Cmdlet " **Satz-AzureRmOperationalInsightsStorageInsight** " ändert die Konfiguration einer Speicher-Insight.</span><span class="sxs-lookup"><span data-stu-id="cc980-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="cc980-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc980-109">EXAMPLES</span></span>

### <span data-ttu-id="cc980-110">Beispiel 1: Ändern eines Speicher Einblicks anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="cc980-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="cc980-111">Mit diesem Befehl werden die Tabellen geändert, aus denen die Speicher Insight mit dem Namen MyStorageInsight liest.</span><span class="sxs-lookup"><span data-stu-id="cc980-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="cc980-112">Beispiel 2: Ändern eines Speicher Einblicks mithilfe eines Workspace-Objekts</span><span class="sxs-lookup"><span data-stu-id="cc980-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="cc980-113">Der erste Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und speichert ihn dann in der Variablen $Workspace.</span><span class="sxs-lookup"><span data-stu-id="cc980-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="cc980-114">Mit dem zweiten Befehl werden die Container geändert, aus denen die Speicher Insight mit dem Namen MyStorageInsight liest.</span><span class="sxs-lookup"><span data-stu-id="cc980-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="cc980-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc980-115">PARAMETERS</span></span>

### <span data-ttu-id="cc980-116">-Container</span><span class="sxs-lookup"><span data-stu-id="cc980-116">-Containers</span></span>
<span data-ttu-id="cc980-117">Gibt die Liste der Container an, die die Daten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cc980-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="cc980-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc980-118">-DefaultProfile</span></span>
<span data-ttu-id="cc980-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cc980-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc980-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cc980-120">-Name</span></span>
<span data-ttu-id="cc980-121">Gibt den Namen einer Speicher-Insight an.</span><span class="sxs-lookup"><span data-stu-id="cc980-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="cc980-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc980-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc980-123">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="cc980-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="cc980-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cc980-124">-StorageAccountKey</span></span>
<span data-ttu-id="cc980-125">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="cc980-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="cc980-126">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="cc980-126">-Tables</span></span>
<span data-ttu-id="cc980-127">Gibt die Liste der Tabellen an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc980-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="cc980-128">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="cc980-128">-Workspace</span></span>
<span data-ttu-id="cc980-129">Gibt den Arbeitsbereich an, der den Speicher Einblick enthält.</span><span class="sxs-lookup"><span data-stu-id="cc980-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="cc980-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cc980-130">-WorkspaceName</span></span>
<span data-ttu-id="cc980-131">Gibt den Namen eines Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="cc980-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="cc980-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc980-132">CommonParameters</span></span>
<span data-ttu-id="cc980-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc980-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc980-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc980-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc980-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc980-135">INPUTS</span></span>

### <span data-ttu-id="cc980-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc980-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="cc980-137">Parameter: Arbeitsbereich (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc980-137">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="cc980-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cc980-138">System.String</span></span>

### <span data-ttu-id="cc980-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="cc980-139">System.String[]</span></span>

## <span data-ttu-id="cc980-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc980-140">OUTPUTS</span></span>

### <span data-ttu-id="cc980-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="cc980-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="cc980-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc980-142">NOTES</span></span>

## <span data-ttu-id="cc980-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc980-143">RELATED LINKS</span></span>

[<span data-ttu-id="cc980-144">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="cc980-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="cc980-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc980-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


