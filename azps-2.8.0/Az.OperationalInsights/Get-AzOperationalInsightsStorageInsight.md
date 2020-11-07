---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 589b6012a1819eac638f6197d0569972e4727fba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847768"
---
# <span data-ttu-id="7bce1-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="7bce1-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="7bce1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bce1-102">SYNOPSIS</span></span>
<span data-ttu-id="7bce1-103">Ruft Informationen zu einem Speicher Einblick ab.</span><span class="sxs-lookup"><span data-stu-id="7bce1-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="7bce1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bce1-104">SYNTAX</span></span>

### <span data-ttu-id="7bce1-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bce1-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bce1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7bce1-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bce1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bce1-107">DESCRIPTION</span></span>
<span data-ttu-id="7bce1-108">Das Cmdlet " **Get-AzOperationalInsightsStorageInsight** " Ruft Informationen zu einem vorhandenen Speicher Insight ab.</span><span class="sxs-lookup"><span data-stu-id="7bce1-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="7bce1-109">Wenn ein Speicher Insight-Name angegeben wird, erhält dieses Cmdlet Informationen zu dieser Speicher Einsicht.</span><span class="sxs-lookup"><span data-stu-id="7bce1-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="7bce1-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Speicher Einblicken in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7bce1-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="7bce1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bce1-111">EXAMPLES</span></span>

### <span data-ttu-id="7bce1-112">Beispiel 1: Abrufen eines Speicher Einblicks nach Namen</span><span class="sxs-lookup"><span data-stu-id="7bce1-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="7bce1-113">Dieser Befehl ruft den Speicher Einblick mit dem Namen MyStorageInsight aus dem Arbeitsbereich mit dem Namen ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="7bce1-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7bce1-114">Beispiel 2: Abrufen eines Speicher Einblicks mithilfe eines Workspace-Objekts</span><span class="sxs-lookup"><span data-stu-id="7bce1-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="7bce1-115">Der erste Befehl verwendet das Cmdlet " **Get-AzOperationalInsightsWorkspace** ", um einen Arbeitsbereich für operationelle Einblicke abzurufen, und speichert ihn dann in der $Workspace-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7bce1-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="7bce1-116">Der zweite Befehl ruft den Speicher Einblick mit dem Namen MyStorageInsight für den Arbeitsbereich in $Workspace ab.</span><span class="sxs-lookup"><span data-stu-id="7bce1-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="7bce1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bce1-117">PARAMETERS</span></span>

### <span data-ttu-id="7bce1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bce1-118">-DefaultProfile</span></span>
<span data-ttu-id="7bce1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7bce1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bce1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7bce1-120">-Name</span></span>
<span data-ttu-id="7bce1-121">Gibt den Namen der Speicher Insight an.</span><span class="sxs-lookup"><span data-stu-id="7bce1-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bce1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bce1-122">-ResourceGroupName</span></span>
<span data-ttu-id="7bce1-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7bce1-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="7bce1-124">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7bce1-124">-Workspace</span></span>
<span data-ttu-id="7bce1-125">Gibt den Arbeitsbereich an, der die Speicher Einblicke enthält.</span><span class="sxs-lookup"><span data-stu-id="7bce1-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="7bce1-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7bce1-126">-WorkspaceName</span></span>
<span data-ttu-id="7bce1-127">Gibt den Namen des Arbeitsbereichs an, der die Speicher Einblicke enthält.</span><span class="sxs-lookup"><span data-stu-id="7bce1-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="7bce1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bce1-128">CommonParameters</span></span>
<span data-ttu-id="7bce1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bce1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bce1-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bce1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bce1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bce1-131">INPUTS</span></span>

### <span data-ttu-id="7bce1-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7bce1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7bce1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7bce1-133">System.String</span></span>

## <span data-ttu-id="7bce1-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bce1-134">OUTPUTS</span></span>

### <span data-ttu-id="7bce1-135">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="7bce1-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="7bce1-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bce1-136">NOTES</span></span>

## <span data-ttu-id="7bce1-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bce1-137">RELATED LINKS</span></span>

[<span data-ttu-id="7bce1-138">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="7bce1-138">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


