---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 7502bbd96371aa505d8d927dfb9a491c2ca32b34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173444"
---
# <span data-ttu-id="59fd5-101">Get-AzVMwarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="59fd5-101">Get-AzVMwarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="59fd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="59fd5-103">Auflisten der Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="59fd5-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="59fd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59fd5-104">SYNTAX</span></span>

```
Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59fd5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="59fd5-106">Auflisten der Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="59fd5-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="59fd5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59fd5-107">EXAMPLES</span></span>

### <span data-ttu-id="59fd5-108">Beispiel 1: Erhalten von Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="59fd5-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="59fd5-109">Erhalten von Administratoranmeldeinformationen für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="59fd5-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="59fd5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59fd5-110">PARAMETERS</span></span>

### <span data-ttu-id="59fd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fd5-111">-DefaultProfile</span></span>
<span data-ttu-id="59fd5-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59fd5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59fd5-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="59fd5-113">-PrivateCloudName</span></span>
<span data-ttu-id="59fd5-114">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="59fd5-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="59fd5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fd5-115">-ResourceGroupName</span></span>
<span data-ttu-id="59fd5-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59fd5-116">The name of the resource group.</span></span>
<span data-ttu-id="59fd5-117">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="59fd5-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="59fd5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59fd5-118">-SubscriptionId</span></span>
<span data-ttu-id="59fd5-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="59fd5-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="59fd5-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59fd5-120">-Confirm</span></span>
<span data-ttu-id="59fd5-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59fd5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59fd5-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="59fd5-122">-WhatIf</span></span>
<span data-ttu-id="59fd5-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59fd5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59fd5-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59fd5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59fd5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fd5-125">CommonParameters</span></span>
<span data-ttu-id="59fd5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59fd5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fd5-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59fd5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fd5-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59fd5-128">INPUTS</span></span>

## <span data-ttu-id="59fd5-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59fd5-129">OUTPUTS</span></span>

### <span data-ttu-id="59fd5-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="59fd5-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="59fd5-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59fd5-131">NOTES</span></span>

<span data-ttu-id="59fd5-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="59fd5-132">ALIASES</span></span>

## <span data-ttu-id="59fd5-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59fd5-133">RELATED LINKS</span></span>

