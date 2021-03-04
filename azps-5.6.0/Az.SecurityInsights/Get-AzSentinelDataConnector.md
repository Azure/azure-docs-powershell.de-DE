---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: b99ad26ddfa0239f073c4179413b2f1fefec4d1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935987"
---
# <span data-ttu-id="7cd19-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7cd19-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="7cd19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd19-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd19-103">Holen Sie sich einen Datenconnector.</span><span class="sxs-lookup"><span data-stu-id="7cd19-103">Get a Data Connector.</span></span>

## <span data-ttu-id="7cd19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cd19-104">SYNTAX</span></span>

### <span data-ttu-id="7cd19-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="7cd19-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cd19-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="7cd19-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cd19-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd19-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cd19-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cd19-108">DESCRIPTION</span></span>
<span data-ttu-id="7cd19-109">Das **Get-AzSentinelDataConnector-Cmdlet** ruft einen Datenconnector aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7cd19-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="7cd19-110">Wenn Sie den *Parameter DataConnectorId angeben,* wird ein einzelnes **DataConnector-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cd19-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="7cd19-111">Wenn Sie den *Parameter DataConnectorId* nicht angeben, wird ein Array zurückgegeben, das alle Datenverbinder im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="7cd19-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="7cd19-112">Sie können das **DataConnector-Objekt** verwenden, um den Datenconnector zu aktualisieren, z. B. können Sie **den DataConnector deaktivieren.**</span><span class="sxs-lookup"><span data-stu-id="7cd19-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="7cd19-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7cd19-113">EXAMPLES</span></span>

### <span data-ttu-id="7cd19-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7cd19-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="7cd19-115">In diesem Beispiel werden alle **DataConnectors** im angegebenen Arbeitsbereich ab- und dann in der $DataConnectors gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cd19-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="7cd19-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7cd19-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="7cd19-117">In diesem Beispiel wird ein **DataConnector** im angegebenen Arbeitsbereich und dann in der $DataConnector gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cd19-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="7cd19-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7cd19-118">PARAMETERS</span></span>

### <span data-ttu-id="7cd19-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="7cd19-119">-DataConnectorId</span></span>
<span data-ttu-id="7cd19-120">Datenverbinder-ID.</span><span class="sxs-lookup"><span data-stu-id="7cd19-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="7cd19-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd19-121">-DefaultProfile</span></span>
<span data-ttu-id="7cd19-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cd19-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd19-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd19-123">-ResourceGroupName</span></span>
<span data-ttu-id="7cd19-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7cd19-124">Resource group name.</span></span>

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

### <span data-ttu-id="7cd19-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd19-125">-ResourceId</span></span>
<span data-ttu-id="7cd19-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7cd19-126">Resource Id.</span></span>

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

### <span data-ttu-id="7cd19-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7cd19-127">-WorkspaceName</span></span>
<span data-ttu-id="7cd19-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="7cd19-128">Workspace Name.</span></span>

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

### <span data-ttu-id="7cd19-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd19-129">CommonParameters</span></span>
<span data-ttu-id="7cd19-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd19-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd19-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cd19-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd19-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7cd19-132">INPUTS</span></span>

### <span data-ttu-id="7cd19-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7cd19-133">System.String</span></span>
## <span data-ttu-id="7cd19-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7cd19-134">OUTPUTS</span></span>

### <span data-ttu-id="7cd19-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7cd19-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="7cd19-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7cd19-136">NOTES</span></span>

## <span data-ttu-id="7cd19-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7cd19-137">RELATED LINKS</span></span>
