---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: ef1829dec7bdc1c3b41fa9e418246e1d9afcc1f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925643"
---
# <span data-ttu-id="f5c4b-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f5c4b-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="f5c4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c4b-103">Registrieren Sie eine Gruppe für virtuelle Windows-Desktopanwendung.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="f5c4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5c4b-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f5c4b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="f5c4b-106">Registrieren Sie eine Gruppe für virtuelle Windows-Desktopanwendung.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="f5c4b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5c4b-107">EXAMPLES</span></span>

### <span data-ttu-id="f5c4b-108">Beispiel 1: Registrieren einer Gruppe für virtuelle Windows-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="f5c4b-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="f5c4b-109">Mit diesem Befehl wird eine Gruppe virtueller Windows-Desktopanwendung in einem Arbeitsbereich registriert.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="f5c4b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f5c4b-110">PARAMETERS</span></span>

### <span data-ttu-id="f5c4b-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="f5c4b-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="f5c4b-112">ApplicationGroupPath Path</span><span class="sxs-lookup"><span data-stu-id="f5c4b-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="f5c4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c4b-113">-DefaultProfile</span></span>
<span data-ttu-id="f5c4b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5c4b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c4b-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5c4b-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f5c4b-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f5c4b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5c4b-117">-SubscriptionId</span></span>
<span data-ttu-id="f5c4b-118">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="f5c4b-118">Subscription Id</span></span>

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

### <span data-ttu-id="f5c4b-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5c4b-119">-WorkspaceName</span></span>
<span data-ttu-id="f5c4b-120">Arbeitsbereichsname</span><span class="sxs-lookup"><span data-stu-id="f5c4b-120">Workspace Name</span></span>

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

### <span data-ttu-id="f5c4b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5c4b-121">-Confirm</span></span>
<span data-ttu-id="f5c4b-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5c4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c4b-123">-WhatIf</span></span>
<span data-ttu-id="f5c4b-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c4b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5c4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c4b-126">CommonParameters</span></span>
<span data-ttu-id="f5c4b-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c4b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5c4b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c4b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5c4b-129">INPUTS</span></span>

## <span data-ttu-id="f5c4b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5c4b-130">OUTPUTS</span></span>

### <span data-ttu-id="f5c4b-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5c4b-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="f5c4b-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f5c4b-132">NOTES</span></span>

<span data-ttu-id="f5c4b-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f5c4b-133">ALIASES</span></span>

## <span data-ttu-id="f5c4b-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f5c4b-134">RELATED LINKS</span></span>

