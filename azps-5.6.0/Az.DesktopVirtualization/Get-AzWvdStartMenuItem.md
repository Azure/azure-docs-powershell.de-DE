---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932896"
---
# <span data-ttu-id="e4e1e-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="e4e1e-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="e4e1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e1e-103">Listen Sie Startmenüelemente in der angegebenen Anwendungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="e4e1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4e1e-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e4e1e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e1e-106">Listen Sie Startmenüelemente in der angegebenen Anwendungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="e4e1e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4e1e-107">EXAMPLES</span></span>

### <span data-ttu-id="e4e1e-108">Beispiel 2: Auflisten von Windows Virtual Desktop Startmenüelementen</span><span class="sxs-lookup"><span data-stu-id="e4e1e-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="e4e1e-109">Mit diesem Befehl werden die Startmenüelemente des virtuellen Desktops in einer Appliktongruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="e4e1e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e4e1e-110">PARAMETERS</span></span>

### <span data-ttu-id="e4e1e-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e1e-111">-ApplicationGroupName</span></span>
<span data-ttu-id="e4e1e-112">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e4e1e-112">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e1e-113">-DefaultProfile</span></span>
<span data-ttu-id="e4e1e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e1e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e1e-115">-ResourceGroupName</span></span>
<span data-ttu-id="e4e1e-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-116">The name of the resource group.</span></span>
<span data-ttu-id="e4e1e-117">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e1e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4e1e-118">-SubscriptionId</span></span>
<span data-ttu-id="e4e1e-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e1e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e1e-120">CommonParameters</span></span>
<span data-ttu-id="e4e1e-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e1e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e1e-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4e1e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e1e-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4e1e-123">INPUTS</span></span>

## <span data-ttu-id="e4e1e-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4e1e-124">OUTPUTS</span></span>

### <span data-ttu-id="e4e1e-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="e4e1e-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="e4e1e-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e4e1e-126">NOTES</span></span>

<span data-ttu-id="e4e1e-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e4e1e-127">ALIASES</span></span>

## <span data-ttu-id="e4e1e-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e4e1e-128">RELATED LINKS</span></span>

