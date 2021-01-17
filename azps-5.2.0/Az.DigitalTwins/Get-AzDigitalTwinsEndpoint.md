---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302483"
---
# <span data-ttu-id="7f84a-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f84a-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="7f84a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f84a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f84a-103">Holen Sie sich den DigitalTwinsInstances-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7f84a-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="7f84a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f84a-104">SYNTAX</span></span>

### <span data-ttu-id="7f84a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f84a-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7f84a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7f84a-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7f84a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f84a-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f84a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f84a-108">DESCRIPTION</span></span>
<span data-ttu-id="7f84a-109">Holen Sie sich den DigitalTwinsInstances-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7f84a-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="7f84a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f84a-110">EXAMPLES</span></span>

### <span data-ttu-id="7f84a-111">Beispiel 1: Auflisten von AzDigitalTwinsEndpoint in "ResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="7f84a-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="7f84a-112">Auflisten aller AzDigitalTwinsEndpoints nach ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f84a-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="7f84a-113">Beispiel 2: Erhalten von AzDigitalTwinsEndpoint nach EndpointName</span><span class="sxs-lookup"><span data-stu-id="7f84a-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="7f84a-114">Herunterladen von AzDigitalTwinsEndpoint nach EndpointName in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f84a-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="7f84a-115">Beispiel 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span><span class="sxs-lookup"><span data-stu-id="7f84a-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="7f84a-116">AzDigitalTwinsEndpoint von 'AzDigitalTwinsEndpoint' Object</span><span class="sxs-lookup"><span data-stu-id="7f84a-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="7f84a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f84a-117">PARAMETERS</span></span>

### <span data-ttu-id="7f84a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f84a-118">-DefaultProfile</span></span>
<span data-ttu-id="7f84a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f84a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f84a-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7f84a-120">-EndpointName</span></span>
<span data-ttu-id="7f84a-121">Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="7f84a-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="7f84a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f84a-122">-InputObject</span></span>
<span data-ttu-id="7f84a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7f84a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7f84a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f84a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7f84a-125">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="7f84a-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f84a-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7f84a-126">-ResourceName</span></span>
<span data-ttu-id="7f84a-127">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="7f84a-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f84a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f84a-128">-SubscriptionId</span></span>
<span data-ttu-id="7f84a-129">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7f84a-129">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f84a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f84a-130">CommonParameters</span></span>
<span data-ttu-id="7f84a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f84a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f84a-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f84a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f84a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f84a-133">INPUTS</span></span>

### <span data-ttu-id="7f84a-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7f84a-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="7f84a-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f84a-135">OUTPUTS</span></span>

### <span data-ttu-id="7f84a-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="7f84a-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="7f84a-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f84a-137">NOTES</span></span>

<span data-ttu-id="7f84a-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7f84a-138">ALIASES</span></span>

<span data-ttu-id="7f84a-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7f84a-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f84a-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7f84a-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f84a-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f84a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f84a-142">INPUTOBJECT <IDigitalTwinsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7f84a-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f84a-143">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="7f84a-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="7f84a-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7f84a-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f84a-145">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7f84a-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7f84a-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="7f84a-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7f84a-147">`[ResourceName <String>]`: Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="7f84a-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7f84a-148">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7f84a-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="7f84a-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f84a-149">RELATED LINKS</span></span>

