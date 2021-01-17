---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470806"
---
# <span data-ttu-id="d7e40-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d7e40-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="d7e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e40-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e40-103">Der Vorgang zum Erhalten der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="d7e40-103">The operation to get the extension.</span></span>

## <span data-ttu-id="d7e40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7e40-104">SYNTAX</span></span>

### <span data-ttu-id="d7e40-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7e40-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7e40-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d7e40-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d7e40-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7e40-107">DESCRIPTION</span></span>
<span data-ttu-id="d7e40-108">Der Vorgang zum Erhalten der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="d7e40-108">The operation to get the extension.</span></span>

## <span data-ttu-id="d7e40-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7e40-109">EXAMPLES</span></span>

### <span data-ttu-id="d7e40-110">Beispiel 1: Auflisten aller Erweiterungen für einen Computer</span><span class="sxs-lookup"><span data-stu-id="d7e40-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="d7e40-111">Hier werden alle Erweiterungen für einen bestimmten Computer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7e40-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="d7e40-112">Beispiel 2: Erhalten einer bestimmten Erweiterung auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="d7e40-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="d7e40-113">Ruft eine bestimmte Erweiterung auf einem Computer ab.</span><span class="sxs-lookup"><span data-stu-id="d7e40-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="d7e40-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7e40-114">PARAMETERS</span></span>

### <span data-ttu-id="d7e40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e40-115">-DefaultProfile</span></span>
<span data-ttu-id="d7e40-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7e40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7e40-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="d7e40-117">-Expand</span></span>
<span data-ttu-id="d7e40-118">Der Erweiterungsausdruck, der auf den Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7e40-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="d7e40-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="d7e40-119">-MachineName</span></span>
<span data-ttu-id="d7e40-120">Der Name des Computers, der die Erweiterung enthält.</span><span class="sxs-lookup"><span data-stu-id="d7e40-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="d7e40-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d7e40-121">-Name</span></span>
<span data-ttu-id="d7e40-122">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="d7e40-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="d7e40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e40-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7e40-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7e40-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7e40-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7e40-125">-SubscriptionId</span></span>
<span data-ttu-id="d7e40-126">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d7e40-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d7e40-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d7e40-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d7e40-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e40-128">CommonParameters</span></span>
<span data-ttu-id="d7e40-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e40-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e40-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7e40-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e40-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7e40-131">INPUTS</span></span>

## <span data-ttu-id="d7e40-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7e40-132">OUTPUTS</span></span>

### <span data-ttu-id="d7e40-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d7e40-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="d7e40-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d7e40-134">NOTES</span></span>

<span data-ttu-id="d7e40-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d7e40-135">ALIASES</span></span>

## <span data-ttu-id="d7e40-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d7e40-136">RELATED LINKS</span></span>

