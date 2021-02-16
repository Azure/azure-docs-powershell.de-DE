---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165953"
---
# <span data-ttu-id="51758-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="51758-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="51758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51758-102">SYNOPSIS</span></span>
<span data-ttu-id="51758-103">Sie können eine Textmarke erhalten.</span><span class="sxs-lookup"><span data-stu-id="51758-103">Get a Bookmark.</span></span>

## <span data-ttu-id="51758-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51758-104">SYNTAX</span></span>

### <span data-ttu-id="51758-105">WorkspaceScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="51758-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51758-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="51758-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51758-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="51758-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51758-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51758-108">DESCRIPTION</span></span>
<span data-ttu-id="51758-109">Das **Cmdlet "Get-AzSentinelBookmark"** ruft eine Textmarke aus dem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="51758-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="51758-110">Wenn Sie den Parameter *"BookmarkId"* angeben, wird **ein** einzelnes Lesezeichenobjekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51758-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="51758-111">Wenn Sie den Parameter *"BookmarkId" nicht* angeben, wird ein Array zurückgegeben, das alle Textmarken im angegebenen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="51758-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="51758-112">Sie können das Objekt **"Textmarke"** verwenden, um die Textmarke zu aktualisieren, beispielsweise können Sie notizen die **Textmarke hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="51758-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="51758-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51758-113">EXAMPLES</span></span>

### <span data-ttu-id="51758-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51758-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="51758-115">Dieses Beispiel ruft alle Lesezeichen **im** angegebenen Arbeitsbereich ab und speichert sie dann in der $Bookmarks Variable.</span><span class="sxs-lookup"><span data-stu-id="51758-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="51758-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="51758-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="51758-117">Dieses Beispiel ruft eine **Textmarke** im angegebenen Arbeitsbereich ab und speichert sie dann in $Bookmark Variable.</span><span class="sxs-lookup"><span data-stu-id="51758-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="51758-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51758-118">PARAMETERS</span></span>

### <span data-ttu-id="51758-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="51758-119">-BookmarkId</span></span>
<span data-ttu-id="51758-120">"Lesezeichen-ID"</span><span class="sxs-lookup"><span data-stu-id="51758-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="51758-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51758-121">-DefaultProfile</span></span>
<span data-ttu-id="51758-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51758-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51758-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51758-123">-ResourceGroupName</span></span>
<span data-ttu-id="51758-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="51758-124">Resource group name.</span></span>

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

### <span data-ttu-id="51758-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51758-125">-ResourceId</span></span>
<span data-ttu-id="51758-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="51758-126">Resource Id.</span></span>

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

### <span data-ttu-id="51758-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51758-127">-WorkspaceName</span></span>
<span data-ttu-id="51758-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="51758-128">Workspace Name.</span></span>

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

### <span data-ttu-id="51758-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51758-129">CommonParameters</span></span>
<span data-ttu-id="51758-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51758-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51758-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51758-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51758-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51758-132">INPUTS</span></span>

### <span data-ttu-id="51758-133">System.String</span><span class="sxs-lookup"><span data-stu-id="51758-133">System.String</span></span>
## <span data-ttu-id="51758-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51758-134">OUTPUTS</span></span>

### <span data-ttu-id="51758-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="51758-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="51758-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="51758-136">NOTES</span></span>

## <span data-ttu-id="51758-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="51758-137">RELATED LINKS</span></span>
