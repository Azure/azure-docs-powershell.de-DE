---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471974"
---
# <span data-ttu-id="7327c-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7327c-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="7327c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7327c-102">SYNOPSIS</span></span>
<span data-ttu-id="7327c-103">"Datenconnector erhalten" aus.</span><span class="sxs-lookup"><span data-stu-id="7327c-103">Get a Data Connector.</span></span>

## <span data-ttu-id="7327c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7327c-104">SYNTAX</span></span>

### <span data-ttu-id="7327c-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="7327c-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7327c-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="7327c-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7327c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7327c-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7327c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7327c-108">DESCRIPTION</span></span>
<span data-ttu-id="7327c-109">Das **Cmdlet "Get-AzSentinelDataConnector"** ruft einen Datenconnector aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7327c-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="7327c-110">Wenn Sie den Parameter *"DataConnectorId"* angeben, wird ein einzelnes **DataConnector-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7327c-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="7327c-111">Wenn Sie den Parameter *"DataConnectorId" nicht* angeben, wird ein Array zurückgegeben, das alle Datenconnectors im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="7327c-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="7327c-112">Sie können das Objekt **"DataConnector"** verwenden, um den Datenconnector zu aktualisieren, z. B. können Sie **"DataConnector" deaktivieren.**</span><span class="sxs-lookup"><span data-stu-id="7327c-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="7327c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7327c-113">EXAMPLES</span></span>

### <span data-ttu-id="7327c-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7327c-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="7327c-115">Dieses Beispiel ruft alle **DataConnectors** im angegebenen Arbeitsbereich ab und speichert sie dann in $DataConnectors Variable.</span><span class="sxs-lookup"><span data-stu-id="7327c-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="7327c-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7327c-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="7327c-117">Dieses Beispiel ruft einen **DataConnector** im angegebenen Arbeitsbereich ab und speichert ihn dann in der $DataConnector Variable.</span><span class="sxs-lookup"><span data-stu-id="7327c-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="7327c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7327c-118">PARAMETERS</span></span>

### <span data-ttu-id="7327c-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="7327c-119">-DataConnectorId</span></span>
<span data-ttu-id="7327c-120">Datenconnector-ID.</span><span class="sxs-lookup"><span data-stu-id="7327c-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7327c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7327c-121">-DefaultProfile</span></span>
<span data-ttu-id="7327c-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7327c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7327c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7327c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7327c-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7327c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7327c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7327c-125">-ResourceId</span></span>
<span data-ttu-id="7327c-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7327c-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7327c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7327c-127">-WorkspaceName</span></span>
<span data-ttu-id="7327c-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="7327c-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7327c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7327c-129">CommonParameters</span></span>
<span data-ttu-id="7327c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7327c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7327c-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7327c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7327c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7327c-132">INPUTS</span></span>

### <span data-ttu-id="7327c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7327c-133">System.String</span></span>
## <span data-ttu-id="7327c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7327c-134">OUTPUTS</span></span>

### <span data-ttu-id="7327c-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7327c-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="7327c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7327c-136">NOTES</span></span>

## <span data-ttu-id="7327c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7327c-137">RELATED LINKS</span></span>
