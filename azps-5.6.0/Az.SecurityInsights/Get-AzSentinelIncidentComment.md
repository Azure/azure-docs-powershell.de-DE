---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: b25e99766c4dc0433b14810352968300fd5bd129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935963"
---
# <span data-ttu-id="8a310-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="8a310-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="8a310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a310-102">SYNOPSIS</span></span>
<span data-ttu-id="8a310-103">Einen Vorfallkommentar erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a310-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="8a310-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a310-104">SYNTAX</span></span>

### <span data-ttu-id="8a310-105">IncidentId (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a310-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a310-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="8a310-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a310-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a310-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a310-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a310-108">DESCRIPTION</span></span>
<span data-ttu-id="8a310-109">Das **Cmdlet Get-AzSentinelIncidentComment** ruft einen Vorfallkommentar aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="8a310-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="8a310-110">Wenn Sie die Parameter *IncidentCommentId* und *IncidentId* angeben, wird ein einzelnes **IncidentComment-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a310-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="8a310-111">Wenn Sie den Parameter *IncidentCommentId* nicht angeben, wird ein Array zurückgegeben, das alle Vorfallkommentare für den angegebenen Vorfall im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="8a310-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="8a310-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a310-112">EXAMPLES</span></span>

### <span data-ttu-id="8a310-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a310-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="8a310-114">In diesem Beispiel werden alle **IncidentComments** für den angegebenen Vorfall im angegebenen Arbeitsbereich ab- und dann in der $IncidentComments gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8a310-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="8a310-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8a310-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="8a310-116">Dieses Beispiel ruft ein **IncidentComment** für den angegebenen Vorfall im angegebenen Arbeitsbereich ab und speichert es dann in der $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="8a310-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="8a310-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a310-117">PARAMETERS</span></span>

### <span data-ttu-id="8a310-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a310-118">-DefaultProfile</span></span>
<span data-ttu-id="8a310-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a310-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a310-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="8a310-120">-IncidentCommentId</span></span>
<span data-ttu-id="8a310-121">Vorfallkommentar-ID.</span><span class="sxs-lookup"><span data-stu-id="8a310-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a310-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="8a310-122">-IncidentId</span></span>
<span data-ttu-id="8a310-123">Vorfall-ID.</span><span class="sxs-lookup"><span data-stu-id="8a310-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a310-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a310-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a310-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8a310-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a310-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a310-126">-ResourceId</span></span>
<span data-ttu-id="8a310-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8a310-127">Resource Id.</span></span>

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

### <span data-ttu-id="8a310-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a310-128">-WorkspaceName</span></span>
<span data-ttu-id="8a310-129">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="8a310-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a310-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a310-130">CommonParameters</span></span>
<span data-ttu-id="8a310-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a310-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a310-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a310-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a310-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a310-133">INPUTS</span></span>

### <span data-ttu-id="8a310-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8a310-134">System.String</span></span>
## <span data-ttu-id="8a310-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a310-135">OUTPUTS</span></span>

### <span data-ttu-id="8a310-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="8a310-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="8a310-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a310-137">NOTES</span></span>

## <span data-ttu-id="8a310-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a310-138">RELATED LINKS</span></span>
