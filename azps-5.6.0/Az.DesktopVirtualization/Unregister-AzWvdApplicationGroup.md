---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 9d3b8c0b1c126353eeab8a2509395e25e467bf0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925611"
---
# <span data-ttu-id="54c35-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="54c35-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="54c35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c35-102">SYNOPSIS</span></span>
<span data-ttu-id="54c35-103">Aufheben der Registrierung der Gruppe der virtuellen Windows-Desktopanwendung.</span><span class="sxs-lookup"><span data-stu-id="54c35-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="54c35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54c35-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="54c35-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54c35-105">DESCRIPTION</span></span>
<span data-ttu-id="54c35-106">Aufheben der Registrierung der Gruppe der virtuellen Windows-Desktopanwendung.</span><span class="sxs-lookup"><span data-stu-id="54c35-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="54c35-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54c35-107">EXAMPLES</span></span>

### <span data-ttu-id="54c35-108">Beispiel 1: Aufheben der Registrierung einer Gruppe für virtuelle Windows-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="54c35-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="54c35-109">Mit diesem Befehl wird die Registrierung einer Gruppe für virtuelle Windows-Desktopanwendung in einem Arbeitsbereich aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="54c35-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="54c35-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54c35-110">PARAMETERS</span></span>

### <span data-ttu-id="54c35-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="54c35-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="54c35-112">ResourceGroupName Path</span><span class="sxs-lookup"><span data-stu-id="54c35-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="54c35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c35-113">-DefaultProfile</span></span>
<span data-ttu-id="54c35-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54c35-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c35-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c35-115">-ResourceGroupName</span></span>
<span data-ttu-id="54c35-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="54c35-116">Resource Group Name</span></span>

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

### <span data-ttu-id="54c35-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54c35-117">-SubscriptionId</span></span>
<span data-ttu-id="54c35-118">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="54c35-118">Subscription Id</span></span>

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

### <span data-ttu-id="54c35-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54c35-119">-WorkspaceName</span></span>
<span data-ttu-id="54c35-120">Arbeitsbereichsname</span><span class="sxs-lookup"><span data-stu-id="54c35-120">Workspace Name</span></span>

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

### <span data-ttu-id="54c35-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54c35-121">-Confirm</span></span>
<span data-ttu-id="54c35-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54c35-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c35-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c35-123">-WhatIf</span></span>
<span data-ttu-id="54c35-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54c35-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c35-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54c35-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c35-126">CommonParameters</span></span>
<span data-ttu-id="54c35-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c35-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54c35-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c35-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54c35-129">INPUTS</span></span>

## <span data-ttu-id="54c35-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54c35-130">OUTPUTS</span></span>

### <span data-ttu-id="54c35-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="54c35-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="54c35-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54c35-132">NOTES</span></span>

<span data-ttu-id="54c35-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="54c35-133">ALIASES</span></span>

## <span data-ttu-id="54c35-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54c35-134">RELATED LINKS</span></span>

