---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cd7dad03d8542685339778d0b0cdac967f83ea21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663875"
---
# <span data-ttu-id="dadad-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="dadad-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="dadad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dadad-102">SYNOPSIS</span></span>
<span data-ttu-id="dadad-103">Ruft Informationen zu einem Speicher Einblick ab.</span><span class="sxs-lookup"><span data-stu-id="dadad-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dadad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dadad-104">SYNTAX</span></span>

### <span data-ttu-id="dadad-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dadad-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dadad-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dadad-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dadad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dadad-107">DESCRIPTION</span></span>
<span data-ttu-id="dadad-108">Das Cmdlet " **Get-AzureRmOperationalInsightsStorageInsight** " Ruft Informationen zu einem vorhandenen Speicher Insight ab.</span><span class="sxs-lookup"><span data-stu-id="dadad-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="dadad-109">Wenn ein Speicher Insight-Name angegeben wird, erhält dieses Cmdlet Informationen zu dieser Speicher Einsicht.</span><span class="sxs-lookup"><span data-stu-id="dadad-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="dadad-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Speicher Einblicken in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="dadad-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="dadad-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dadad-111">EXAMPLES</span></span>

### <span data-ttu-id="dadad-112">Beispiel 1: Abrufen eines Speicher Einblicks nach Namen</span><span class="sxs-lookup"><span data-stu-id="dadad-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="dadad-113">Dieser Befehl ruft den Speicher Einblick mit dem Namen MyStorageInsight aus dem Arbeitsbereich mit dem Namen ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="dadad-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="dadad-114">Beispiel 2: Abrufen eines Speicher Einblicks mithilfe eines Workspace-Objekts</span><span class="sxs-lookup"><span data-stu-id="dadad-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="dadad-115">Der erste Befehl verwendet das Cmdlet " **Get-AzureRmOperationalInsightsWorkspace** ", um einen Arbeitsbereich für operationelle Einblicke abzurufen, und speichert ihn dann in der $Workspace-Variablen.</span><span class="sxs-lookup"><span data-stu-id="dadad-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="dadad-116">Der zweite Befehl ruft den Speicher Einblick mit dem Namen MyStorageInsight für den Arbeitsbereich in $Workspace ab.</span><span class="sxs-lookup"><span data-stu-id="dadad-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="dadad-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="dadad-117">PARAMETERS</span></span>

### <span data-ttu-id="dadad-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dadad-118">-Name</span></span>
<span data-ttu-id="dadad-119">Gibt den Namen der Speicher Insight an.</span><span class="sxs-lookup"><span data-stu-id="dadad-119">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="dadad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dadad-120">-ResourceGroupName</span></span>
<span data-ttu-id="dadad-121">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dadad-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="dadad-122">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="dadad-122">-Workspace</span></span>
<span data-ttu-id="dadad-123">Gibt den Arbeitsbereich an, der die Speicher Einblicke enthält.</span><span class="sxs-lookup"><span data-stu-id="dadad-123">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="dadad-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dadad-124">-WorkspaceName</span></span>
<span data-ttu-id="dadad-125">Gibt den Namen des Arbeitsbereichs an, der die Speicher Einblicke enthält.</span><span class="sxs-lookup"><span data-stu-id="dadad-125">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="dadad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dadad-126">-DefaultProfile</span></span>
<span data-ttu-id="dadad-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dadad-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dadad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dadad-128">CommonParameters</span></span>
<span data-ttu-id="dadad-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dadad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dadad-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dadad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dadad-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dadad-131">INPUTS</span></span>

### <span data-ttu-id="dadad-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="dadad-132">PSWorkspace</span></span>
<span data-ttu-id="dadad-133">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dadad-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="dadad-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dadad-134">OUTPUTS</span></span>

### <span data-ttu-id="dadad-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="dadad-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="dadad-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="dadad-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="dadad-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="dadad-137">NOTES</span></span>

## <span data-ttu-id="dadad-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dadad-138">RELATED LINKS</span></span>

[<span data-ttu-id="dadad-139">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="dadad-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


