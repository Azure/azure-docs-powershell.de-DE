---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387231"
---
# <span data-ttu-id="c0166-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c0166-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c0166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0166-102">SYNOPSIS</span></span>
<span data-ttu-id="c0166-103">Registrieren Sie eine Gruppe für virtuelle Windows-Desktopanwendung.</span><span class="sxs-lookup"><span data-stu-id="c0166-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c0166-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0166-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c0166-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0166-105">DESCRIPTION</span></span>
<span data-ttu-id="c0166-106">Registrieren Sie eine Gruppe für virtuelle Windows-Desktopanwendung.</span><span class="sxs-lookup"><span data-stu-id="c0166-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c0166-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0166-107">EXAMPLES</span></span>

### <span data-ttu-id="c0166-108">Beispiel 1: Registrieren einer Gruppe für virtuelle Windows-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="c0166-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="c0166-109">Mit diesem Befehl wird eine Gruppe für virtuelle Windows-Desktopanwendung für einen Arbeitsbereich registriert.</span><span class="sxs-lookup"><span data-stu-id="c0166-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="c0166-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0166-110">PARAMETERS</span></span>

### <span data-ttu-id="c0166-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="c0166-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="c0166-112">ApplicationGroupPath Path</span><span class="sxs-lookup"><span data-stu-id="c0166-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="c0166-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0166-113">-DefaultProfile</span></span>
<span data-ttu-id="c0166-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0166-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0166-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0166-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0166-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c0166-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c0166-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0166-117">-SubscriptionId</span></span>
<span data-ttu-id="c0166-118">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="c0166-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0166-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0166-119">-WorkspaceName</span></span>
<span data-ttu-id="c0166-120">Arbeitsbereichsname</span><span class="sxs-lookup"><span data-stu-id="c0166-120">Workspace Name</span></span>

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

### <span data-ttu-id="c0166-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0166-121">-Confirm</span></span>
<span data-ttu-id="c0166-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0166-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0166-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c0166-123">-WhatIf</span></span>
<span data-ttu-id="c0166-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0166-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0166-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0166-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0166-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0166-126">CommonParameters</span></span>
<span data-ttu-id="c0166-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0166-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0166-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0166-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0166-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0166-129">INPUTS</span></span>

## <span data-ttu-id="c0166-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0166-130">OUTPUTS</span></span>

### <span data-ttu-id="c0166-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0166-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="c0166-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c0166-132">NOTES</span></span>

<span data-ttu-id="c0166-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c0166-133">ALIASES</span></span>

## <span data-ttu-id="c0166-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c0166-134">RELATED LINKS</span></span>

