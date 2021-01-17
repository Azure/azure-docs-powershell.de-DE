---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380819"
---
# <span data-ttu-id="0f369-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="0f369-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="0f369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f369-102">SYNOPSIS</span></span>
<span data-ttu-id="0f369-103">Erstellen oder Aktualisieren einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="0f369-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0f369-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f369-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0f369-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f369-105">DESCRIPTION</span></span>
<span data-ttu-id="0f369-106">Erstellen oder Aktualisieren einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="0f369-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0f369-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f369-107">EXAMPLES</span></span>

### <span data-ttu-id="0f369-108">Beispiel 1: Erstellen einer Autorisierung</span><span class="sxs-lookup"><span data-stu-id="0f369-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="0f369-109">Dieses Cmdlet erstellt Autorisierung `azps-test-auth` in der privaten Cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="0f369-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="0f369-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f369-110">PARAMETERS</span></span>

### <span data-ttu-id="0f369-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f369-111">-AsJob</span></span>
<span data-ttu-id="0f369-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0f369-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f369-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f369-113">-DefaultProfile</span></span>
<span data-ttu-id="0f369-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f369-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f369-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0f369-115">-Name</span></span>
<span data-ttu-id="0f369-116">Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="0f369-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f369-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0f369-117">-NoWait</span></span>
<span data-ttu-id="0f369-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0f369-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f369-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0f369-119">-PrivateCloudName</span></span>
<span data-ttu-id="0f369-120">Der Name der privaten Cloud.</span><span class="sxs-lookup"><span data-stu-id="0f369-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="0f369-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f369-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f369-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0f369-122">The name of the resource group.</span></span>
<span data-ttu-id="0f369-123">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0f369-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0f369-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f369-124">-SubscriptionId</span></span>
<span data-ttu-id="0f369-125">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0f369-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0f369-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f369-126">-Confirm</span></span>
<span data-ttu-id="0f369-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f369-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f369-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0f369-128">-WhatIf</span></span>
<span data-ttu-id="0f369-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f369-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f369-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f369-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f369-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f369-131">CommonParameters</span></span>
<span data-ttu-id="0f369-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f369-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f369-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f369-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f369-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f369-134">INPUTS</span></span>

## <span data-ttu-id="0f369-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f369-135">OUTPUTS</span></span>

### <span data-ttu-id="0f369-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="0f369-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="0f369-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f369-137">NOTES</span></span>

<span data-ttu-id="0f369-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0f369-138">ALIASES</span></span>

## <span data-ttu-id="0f369-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f369-139">RELATED LINKS</span></span>

