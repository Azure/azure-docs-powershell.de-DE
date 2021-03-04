---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: 423834d0dc7a324743795e0d54324a51f1cd04ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948816"
---
# <span data-ttu-id="d6e18-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d6e18-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="d6e18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6e18-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e18-103">Der Vorgang, um die Erweiterung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6e18-103">The operation to get the extension.</span></span>

## <span data-ttu-id="d6e18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6e18-104">SYNTAX</span></span>

### <span data-ttu-id="d6e18-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6e18-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6e18-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d6e18-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d6e18-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6e18-107">DESCRIPTION</span></span>
<span data-ttu-id="d6e18-108">Der Vorgang, um die Erweiterung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6e18-108">The operation to get the extension.</span></span>

## <span data-ttu-id="d6e18-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6e18-109">EXAMPLES</span></span>

### <span data-ttu-id="d6e18-110">Beispiel 1: Auflisten aller Erweiterungen für einen Computer</span><span class="sxs-lookup"><span data-stu-id="d6e18-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="d6e18-111">Listet alle Erweiterungen für einen bestimmten Computer auf.</span><span class="sxs-lookup"><span data-stu-id="d6e18-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="d6e18-112">Beispiel 2: Erhalten einer bestimmten Erweiterung auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="d6e18-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="d6e18-113">Ruft eine bestimmte Erweiterung auf einem Computer ab.</span><span class="sxs-lookup"><span data-stu-id="d6e18-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="d6e18-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d6e18-114">PARAMETERS</span></span>

### <span data-ttu-id="d6e18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e18-115">-DefaultProfile</span></span>
<span data-ttu-id="d6e18-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6e18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e18-117">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="d6e18-117">-Expand</span></span>
<span data-ttu-id="d6e18-118">Der erweiterungsausdruck, der auf den Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6e18-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e18-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="d6e18-119">-MachineName</span></span>
<span data-ttu-id="d6e18-120">Der Name des Computers, der die Erweiterung enthält.</span><span class="sxs-lookup"><span data-stu-id="d6e18-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="d6e18-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d6e18-121">-Name</span></span>
<span data-ttu-id="d6e18-122">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="d6e18-122">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e18-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e18-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6e18-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d6e18-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6e18-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6e18-125">-SubscriptionId</span></span>
<span data-ttu-id="d6e18-126">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d6e18-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6e18-127">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d6e18-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6e18-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e18-128">CommonParameters</span></span>
<span data-ttu-id="d6e18-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e18-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e18-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6e18-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e18-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6e18-131">INPUTS</span></span>

## <span data-ttu-id="d6e18-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6e18-132">OUTPUTS</span></span>

### <span data-ttu-id="d6e18-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d6e18-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="d6e18-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d6e18-134">NOTES</span></span>

<span data-ttu-id="d6e18-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d6e18-135">ALIASES</span></span>

## <span data-ttu-id="d6e18-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d6e18-136">RELATED LINKS</span></span>

