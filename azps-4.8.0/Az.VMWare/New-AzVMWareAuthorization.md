---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173649"
---
# <span data-ttu-id="95100-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="95100-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="95100-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95100-102">SYNOPSIS</span></span>
<span data-ttu-id="95100-103">Erstellen oder Aktualisieren einer Express Route-Schaltkreis Autorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="95100-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="95100-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95100-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="95100-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95100-105">DESCRIPTION</span></span>
<span data-ttu-id="95100-106">Erstellen oder Aktualisieren einer Express Route-Schaltkreis Autorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="95100-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="95100-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95100-107">EXAMPLES</span></span>

### <span data-ttu-id="95100-108">Beispiel 1: Erstellen der Autorisierung</span><span class="sxs-lookup"><span data-stu-id="95100-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="95100-109">Dieses Cmdlet erstellt eine Autorisierung `azps-test-auth` unter privater Cloud. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="95100-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="95100-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95100-110">PARAMETERS</span></span>

### <span data-ttu-id="95100-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95100-111">-AsJob</span></span>
<span data-ttu-id="95100-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="95100-112">Run the command as a job</span></span>

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

### <span data-ttu-id="95100-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95100-113">-DefaultProfile</span></span>
<span data-ttu-id="95100-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95100-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95100-115">-Name</span><span class="sxs-lookup"><span data-stu-id="95100-115">-Name</span></span>
<span data-ttu-id="95100-116">Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="95100-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="95100-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="95100-117">-NoWait</span></span>
<span data-ttu-id="95100-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="95100-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95100-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="95100-119">-PrivateCloudName</span></span>
<span data-ttu-id="95100-120">Der Name der privaten Cloud.</span><span class="sxs-lookup"><span data-stu-id="95100-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="95100-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95100-121">-ResourceGroupName</span></span>
<span data-ttu-id="95100-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95100-122">The name of the resource group.</span></span>
<span data-ttu-id="95100-123">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="95100-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="95100-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="95100-124">-SubscriptionId</span></span>
<span data-ttu-id="95100-125">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="95100-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="95100-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95100-126">-Confirm</span></span>
<span data-ttu-id="95100-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95100-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95100-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95100-128">-WhatIf</span></span>
<span data-ttu-id="95100-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95100-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95100-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95100-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95100-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95100-131">CommonParameters</span></span>
<span data-ttu-id="95100-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95100-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95100-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95100-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95100-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95100-134">INPUTS</span></span>

## <span data-ttu-id="95100-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95100-135">OUTPUTS</span></span>

### <span data-ttu-id="95100-136">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="95100-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="95100-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="95100-137">NOTES</span></span>

<span data-ttu-id="95100-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="95100-138">ALIASES</span></span>

## <span data-ttu-id="95100-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95100-139">RELATED LINKS</span></span>

