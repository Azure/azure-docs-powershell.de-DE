---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293380"
---
# <span data-ttu-id="82b28-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="82b28-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="82b28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82b28-102">SYNOPSIS</span></span>
<span data-ttu-id="82b28-103">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="82b28-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="82b28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82b28-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82b28-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82b28-105">DESCRIPTION</span></span>
<span data-ttu-id="82b28-106">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="82b28-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="82b28-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82b28-107">EXAMPLES</span></span>

### <span data-ttu-id="82b28-108">Beispiel 1: Aktualisieren der Dashboarddefinition mithilfe einer Dashboardvorlage</span><span class="sxs-lookup"><span data-stu-id="82b28-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="82b28-109">Aktualisieren einer Dashboarddefinition mithilfe einer Strichbaord-Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="82b28-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="82b28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82b28-110">PARAMETERS</span></span>

### <span data-ttu-id="82b28-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="82b28-111">-DashboardPath</span></span>
<span data-ttu-id="82b28-112">Der Pfad zu einer vorhandenen Dashboardvorlage.</span><span class="sxs-lookup"><span data-stu-id="82b28-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="82b28-113">Dashboardvorlagen können aus dem Portal heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="82b28-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="82b28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b28-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="82b28-115">-Name</span><span class="sxs-lookup"><span data-stu-id="82b28-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b28-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b28-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="82b28-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82b28-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b28-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82b28-118">-Confirm</span></span>
<span data-ttu-id="82b28-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82b28-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b28-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="82b28-120">-WhatIf</span></span>
<span data-ttu-id="82b28-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82b28-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b28-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82b28-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b28-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b28-123">CommonParameters</span></span>
<span data-ttu-id="82b28-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b28-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b28-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82b28-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b28-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82b28-126">INPUTS</span></span>

## <span data-ttu-id="82b28-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82b28-127">OUTPUTS</span></span>

### <span data-ttu-id="82b28-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="82b28-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="82b28-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="82b28-129">NOTES</span></span>

<span data-ttu-id="82b28-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="82b28-130">ALIASES</span></span>

## <span data-ttu-id="82b28-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="82b28-131">RELATED LINKS</span></span>

