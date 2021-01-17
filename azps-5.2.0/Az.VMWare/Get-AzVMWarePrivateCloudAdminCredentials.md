---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290902"
---
# <span data-ttu-id="18dae-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="18dae-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="18dae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18dae-102">SYNOPSIS</span></span>
<span data-ttu-id="18dae-103">Auflisten der Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="18dae-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="18dae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18dae-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18dae-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18dae-105">DESCRIPTION</span></span>
<span data-ttu-id="18dae-106">Auflisten der Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="18dae-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="18dae-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18dae-107">EXAMPLES</span></span>

### <span data-ttu-id="18dae-108">Beispiel 1: Erhalten von Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="18dae-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="18dae-109">Erhalten von Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="18dae-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="18dae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18dae-110">PARAMETERS</span></span>

### <span data-ttu-id="18dae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dae-111">-DefaultProfile</span></span>
<span data-ttu-id="18dae-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18dae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18dae-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="18dae-113">-PrivateCloudName</span></span>
<span data-ttu-id="18dae-114">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="18dae-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="18dae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dae-115">-ResourceGroupName</span></span>
<span data-ttu-id="18dae-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="18dae-116">The name of the resource group.</span></span>
<span data-ttu-id="18dae-117">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="18dae-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="18dae-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18dae-118">-SubscriptionId</span></span>
<span data-ttu-id="18dae-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="18dae-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="18dae-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18dae-120">-Confirm</span></span>
<span data-ttu-id="18dae-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18dae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18dae-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="18dae-122">-WhatIf</span></span>
<span data-ttu-id="18dae-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18dae-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18dae-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18dae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18dae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dae-125">CommonParameters</span></span>
<span data-ttu-id="18dae-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dae-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18dae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dae-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18dae-128">INPUTS</span></span>

## <span data-ttu-id="18dae-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18dae-129">OUTPUTS</span></span>

### <span data-ttu-id="18dae-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="18dae-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="18dae-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="18dae-131">NOTES</span></span>

<span data-ttu-id="18dae-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="18dae-132">ALIASES</span></span>

## <span data-ttu-id="18dae-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="18dae-133">RELATED LINKS</span></span>

