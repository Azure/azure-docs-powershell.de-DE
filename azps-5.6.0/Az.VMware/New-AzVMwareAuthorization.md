---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 7c532f6aca8c959367d4e67725f36b44e4978840
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939056"
---
# <span data-ttu-id="bf1ec-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="bf1ec-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="bf1ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1ec-103">Erstellen oder Aktualisieren einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bf1ec-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="bf1ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf1ec-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bf1ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1ec-106">Erstellen oder Aktualisieren einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bf1ec-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="bf1ec-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf1ec-107">EXAMPLES</span></span>

### <span data-ttu-id="bf1ec-108">Beispiel 1: Erstellen einer Autorisierung</span><span class="sxs-lookup"><span data-stu-id="bf1ec-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="bf1ec-109">Mit diesem Cmdlet wird eine Autorisierung `azps-test-auth` unter der privaten Cloud erstellt. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="bf1ec-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="bf1ec-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf1ec-110">PARAMETERS</span></span>

### <span data-ttu-id="bf1ec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf1ec-111">-AsJob</span></span>
<span data-ttu-id="bf1ec-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="bf1ec-112">Run the command as a job</span></span>

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

### <span data-ttu-id="bf1ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1ec-113">-DefaultProfile</span></span>
<span data-ttu-id="bf1ec-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf1ec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bf1ec-115">-Name</span></span>
<span data-ttu-id="bf1ec-116">Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bf1ec-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="bf1ec-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf1ec-117">-NoWait</span></span>
<span data-ttu-id="bf1ec-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="bf1ec-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bf1ec-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="bf1ec-119">-PrivateCloudName</span></span>
<span data-ttu-id="bf1ec-120">Der Name der privaten Cloud.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="bf1ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf1ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf1ec-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-122">The name of the resource group.</span></span>
<span data-ttu-id="bf1ec-123">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bf1ec-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf1ec-124">-SubscriptionId</span></span>
<span data-ttu-id="bf1ec-125">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bf1ec-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf1ec-126">-Confirm</span></span>
<span data-ttu-id="bf1ec-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf1ec-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf1ec-128">-WhatIf</span></span>
<span data-ttu-id="bf1ec-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf1ec-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf1ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1ec-131">CommonParameters</span></span>
<span data-ttu-id="bf1ec-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1ec-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf1ec-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1ec-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf1ec-134">INPUTS</span></span>

## <span data-ttu-id="bf1ec-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf1ec-135">OUTPUTS</span></span>

### <span data-ttu-id="bf1ec-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="bf1ec-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="bf1ec-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bf1ec-137">NOTES</span></span>

<span data-ttu-id="bf1ec-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bf1ec-138">ALIASES</span></span>

## <span data-ttu-id="bf1ec-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bf1ec-139">RELATED LINKS</span></span>

