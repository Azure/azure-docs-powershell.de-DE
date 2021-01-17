---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: fd91ea79cbad51d03c0986ed5f55601af240de16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387301"
---
# <span data-ttu-id="24b31-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="24b31-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="24b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b31-102">SYNOPSIS</span></span>
<span data-ttu-id="24b31-103">Listen Sie Startmenüelemente in der angegebenen Anwendungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="24b31-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="24b31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24b31-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="24b31-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24b31-105">DESCRIPTION</span></span>
<span data-ttu-id="24b31-106">Listen Sie Startmenüelemente in der angegebenen Anwendungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="24b31-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="24b31-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24b31-107">EXAMPLES</span></span>

### <span data-ttu-id="24b31-108">Beispiel 2: Auflisten der Startmenüelemente des virtuellen Desktops von Windows</span><span class="sxs-lookup"><span data-stu-id="24b31-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="24b31-109">Mit diesem Befehl werden die Startmenüelemente des virtuellen Desktops von Windows in einer Anwendungsgruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="24b31-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="24b31-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24b31-110">PARAMETERS</span></span>

### <span data-ttu-id="24b31-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="24b31-111">-ApplicationGroupName</span></span>
<span data-ttu-id="24b31-112">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="24b31-112">The name of the application group</span></span>

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

### <span data-ttu-id="24b31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b31-113">-DefaultProfile</span></span>
<span data-ttu-id="24b31-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24b31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b31-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b31-115">-ResourceGroupName</span></span>
<span data-ttu-id="24b31-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24b31-116">The name of the resource group.</span></span>
<span data-ttu-id="24b31-117">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="24b31-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="24b31-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24b31-118">-SubscriptionId</span></span>
<span data-ttu-id="24b31-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="24b31-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="24b31-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b31-120">CommonParameters</span></span>
<span data-ttu-id="24b31-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b31-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b31-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24b31-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b31-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24b31-123">INPUTS</span></span>

## <span data-ttu-id="24b31-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24b31-124">OUTPUTS</span></span>

### <span data-ttu-id="24b31-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="24b31-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="24b31-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="24b31-126">NOTES</span></span>

<span data-ttu-id="24b31-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="24b31-127">ALIASES</span></span>

## <span data-ttu-id="24b31-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="24b31-128">RELATED LINKS</span></span>

