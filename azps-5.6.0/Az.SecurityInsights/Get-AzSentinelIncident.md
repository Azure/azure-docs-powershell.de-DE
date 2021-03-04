---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: 669e0961327b6419e86f288ec71bffa6cdc69b4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935984"
---
# <span data-ttu-id="1f193-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="1f193-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="1f193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f193-102">SYNOPSIS</span></span>
<span data-ttu-id="1f193-103">Einen Vorfall erhalten.</span><span class="sxs-lookup"><span data-stu-id="1f193-103">Get an Incident.</span></span>

## <span data-ttu-id="1f193-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f193-104">SYNTAX</span></span>

### <span data-ttu-id="1f193-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f193-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f193-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="1f193-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f193-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f193-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f193-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f193-108">DESCRIPTION</span></span>
<span data-ttu-id="1f193-109">Das **Cmdlet Get-AzSentinelIncident** ruft einen Vorfall aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="1f193-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="1f193-110">Wenn Sie den *Parameter IncidentId angeben,* wird ein einzelnes **Incident-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f193-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="1f193-111">Wenn Sie den Parameter *IncidentId* nicht angeben, wird ein Array zurückgegeben, das alle Vorfälle im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="1f193-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="1f193-112">Sie können das **Incident-Objekt** verwenden, um den Vorfall zu aktualisieren, z. B. können Sie Notizen zum **Vorfall hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="1f193-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="1f193-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1f193-113">EXAMPLES</span></span>

### <span data-ttu-id="1f193-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1f193-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="1f193-115">In diesem Beispiel werden alle Vorfälle **im** angegebenen Arbeitsbereich ab- und dann in der $Incidents gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1f193-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="1f193-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1f193-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="1f193-117">In diesem Beispiel wird ein **Vorfall** im angegebenen Arbeitsbereich angezeigt und dann in der $Incident gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1f193-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="1f193-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1f193-118">PARAMETERS</span></span>

### <span data-ttu-id="1f193-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f193-119">-DefaultProfile</span></span>
<span data-ttu-id="1f193-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f193-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f193-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="1f193-121">-IncidentId</span></span>
<span data-ttu-id="1f193-122">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="1f193-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f193-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f193-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f193-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1f193-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f193-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f193-125">-ResourceId</span></span>
<span data-ttu-id="1f193-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1f193-126">Resource Id.</span></span>

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

### <span data-ttu-id="1f193-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1f193-127">-WorkspaceName</span></span>
<span data-ttu-id="1f193-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="1f193-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f193-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f193-129">CommonParameters</span></span>
<span data-ttu-id="1f193-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f193-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f193-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f193-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f193-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1f193-132">INPUTS</span></span>

### <span data-ttu-id="1f193-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1f193-133">System.String</span></span>
## <span data-ttu-id="1f193-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1f193-134">OUTPUTS</span></span>

### <span data-ttu-id="1f193-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="1f193-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="1f193-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1f193-136">NOTES</span></span>

## <span data-ttu-id="1f193-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1f193-137">RELATED LINKS</span></span>
