---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302467"
---
# <span data-ttu-id="598c2-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="598c2-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="598c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="598c2-102">SYNOPSIS</span></span>
<span data-ttu-id="598c2-103">Holen Sie sich die Ressource "DigitalTwinsInstances".</span><span class="sxs-lookup"><span data-stu-id="598c2-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="598c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="598c2-104">SYNTAX</span></span>

### <span data-ttu-id="598c2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="598c2-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="598c2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="598c2-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="598c2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="598c2-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="598c2-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="598c2-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="598c2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="598c2-109">DESCRIPTION</span></span>
<span data-ttu-id="598c2-110">Holen Sie sich die Ressource "DigitalTwinsInstances".</span><span class="sxs-lookup"><span data-stu-id="598c2-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="598c2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="598c2-111">EXAMPLES</span></span>

### <span data-ttu-id="598c2-112">Beispiel 1: Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="598c2-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="598c2-113">Standardmäßiges Herunterladen aller DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="598c2-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="598c2-114">Beispiel 2: Erhalten</span><span class="sxs-lookup"><span data-stu-id="598c2-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="598c2-115">Die angegebene Datei "AzDigitalTwinsInstance" nach "ResourceName"</span><span class="sxs-lookup"><span data-stu-id="598c2-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="598c2-116">Beispiel 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="598c2-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="598c2-117">Die angegebene Datei "AzDigitalTwinsInstance by Object"</span><span class="sxs-lookup"><span data-stu-id="598c2-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="598c2-118">Beispiel 4: Liste1</span><span class="sxs-lookup"><span data-stu-id="598c2-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="598c2-119">Herunterladen aller DigitalTwinsInstance von ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598c2-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="598c2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="598c2-120">PARAMETERS</span></span>

### <span data-ttu-id="598c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598c2-121">-DefaultProfile</span></span>
<span data-ttu-id="598c2-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="598c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="598c2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="598c2-123">-InputObject</span></span>
<span data-ttu-id="598c2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="598c2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="598c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="598c2-126">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="598c2-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598c2-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="598c2-127">-ResourceName</span></span>
<span data-ttu-id="598c2-128">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="598c2-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="598c2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="598c2-129">-SubscriptionId</span></span>
<span data-ttu-id="598c2-130">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="598c2-130">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598c2-131">CommonParameters</span></span>
<span data-ttu-id="598c2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="598c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598c2-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="598c2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598c2-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="598c2-134">INPUTS</span></span>

### <span data-ttu-id="598c2-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="598c2-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="598c2-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="598c2-136">OUTPUTS</span></span>

### <span data-ttu-id="598c2-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="598c2-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="598c2-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="598c2-138">NOTES</span></span>

<span data-ttu-id="598c2-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="598c2-139">ALIASES</span></span>

<span data-ttu-id="598c2-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="598c2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="598c2-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="598c2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="598c2-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="598c2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="598c2-143">INPUTOBJECT <IDigitalTwinsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="598c2-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="598c2-144">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="598c2-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="598c2-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="598c2-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="598c2-146">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="598c2-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="598c2-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="598c2-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="598c2-148">`[ResourceName <String>]`: Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="598c2-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="598c2-149">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="598c2-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="598c2-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="598c2-150">RELATED LINKS</span></span>

