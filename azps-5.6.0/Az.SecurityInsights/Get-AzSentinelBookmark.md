---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 5093f924f87f146550b13e3858f9a93b3f193ca0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945707"
---
# <span data-ttu-id="ba978-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="ba978-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="ba978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba978-102">SYNOPSIS</span></span>
<span data-ttu-id="ba978-103">Holen Sie sich eine Textmarke.</span><span class="sxs-lookup"><span data-stu-id="ba978-103">Get a Bookmark.</span></span>

## <span data-ttu-id="ba978-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba978-104">SYNTAX</span></span>

### <span data-ttu-id="ba978-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba978-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba978-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="ba978-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba978-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba978-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba978-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba978-108">DESCRIPTION</span></span>
<span data-ttu-id="ba978-109">Das **Get-AzSentinelBookmark-Cmdlet** ruft ein Lesezeichen aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="ba978-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="ba978-110">Wenn Sie den *Parameter BookmarkId angeben,* wird ein einzelnes **Lesezeichenobjekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba978-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="ba978-111">Wenn Sie den Parameter *BookmarkId* nicht angeben, wird ein Array zurückgegeben, das alle Lesezeichen im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="ba978-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="ba978-112">Sie können das **Lesezeichenobjekt** verwenden, um die Textmarke zu aktualisieren, z. B. können Sie notizen die **Textmarke hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="ba978-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="ba978-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba978-113">EXAMPLES</span></span>

### <span data-ttu-id="ba978-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba978-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="ba978-115">In diesem Beispiel werden alle Lesezeichen **im** angegebenen Arbeitsbereich ab- und dann in der $Bookmarks gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ba978-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="ba978-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ba978-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="ba978-117">In diesem Beispiel wird eine **Textmarke** im angegebenen Arbeitsbereich angezeigt und dann in der $Bookmark gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ba978-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="ba978-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba978-118">PARAMETERS</span></span>

### <span data-ttu-id="ba978-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="ba978-119">-BookmarkId</span></span>
<span data-ttu-id="ba978-120">Lesezeichen-ID,</span><span class="sxs-lookup"><span data-stu-id="ba978-120">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba978-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba978-121">-DefaultProfile</span></span>
<span data-ttu-id="ba978-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba978-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba978-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba978-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba978-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba978-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba978-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba978-125">-ResourceId</span></span>
<span data-ttu-id="ba978-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ba978-126">Resource Id.</span></span>

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

### <span data-ttu-id="ba978-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ba978-127">-WorkspaceName</span></span>
<span data-ttu-id="ba978-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="ba978-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba978-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba978-129">CommonParameters</span></span>
<span data-ttu-id="ba978-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba978-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba978-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba978-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba978-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba978-132">INPUTS</span></span>

### <span data-ttu-id="ba978-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ba978-133">System.String</span></span>
## <span data-ttu-id="ba978-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba978-134">OUTPUTS</span></span>

### <span data-ttu-id="ba978-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="ba978-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="ba978-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba978-136">NOTES</span></span>

## <span data-ttu-id="ba978-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba978-137">RELATED LINKS</span></span>
