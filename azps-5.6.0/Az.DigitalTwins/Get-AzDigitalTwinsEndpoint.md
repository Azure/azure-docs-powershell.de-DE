---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 35ba036e38b54a335cbdcdd923008a5a4ce055fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935171"
---
# <span data-ttu-id="e71cd-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="e71cd-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="e71cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e71cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e71cd-103">DigitalTwinsInstances Endpoint herunterladen.</span><span class="sxs-lookup"><span data-stu-id="e71cd-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="e71cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e71cd-104">SYNTAX</span></span>

### <span data-ttu-id="e71cd-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e71cd-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e71cd-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e71cd-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e71cd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e71cd-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e71cd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e71cd-108">DESCRIPTION</span></span>
<span data-ttu-id="e71cd-109">DigitalTwinsInstances Endpoint herunterladen.</span><span class="sxs-lookup"><span data-stu-id="e71cd-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="e71cd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e71cd-110">EXAMPLES</span></span>

### <span data-ttu-id="e71cd-111">Beispiel 1: Auflisten von AzDigitalTwinsEndpoint in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e71cd-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="e71cd-112">Auflisten aller AzDigitalTwinsEndpoints nach ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71cd-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="e71cd-113">Beispiel 2: Herunterladen von AzDigitalTwinsEndpoint nach EndpointName</span><span class="sxs-lookup"><span data-stu-id="e71cd-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="e71cd-114">AzDigitalTwinsEndpoint von EndpointName in ResourceGroup herunterladen</span><span class="sxs-lookup"><span data-stu-id="e71cd-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="e71cd-115">Beispiel 3: "AzDigitalTwinsEndpoint nach "AzDigitalTwinsEndpoint"-Objekt</span><span class="sxs-lookup"><span data-stu-id="e71cd-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="e71cd-116">AzDigitalTwinsEndpoint von 'AzDigitalTwinsEndpoint'-Objekt</span><span class="sxs-lookup"><span data-stu-id="e71cd-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="e71cd-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e71cd-117">PARAMETERS</span></span>

### <span data-ttu-id="e71cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71cd-118">-DefaultProfile</span></span>
<span data-ttu-id="e71cd-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e71cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e71cd-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e71cd-120">-EndpointName</span></span>
<span data-ttu-id="e71cd-121">Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="e71cd-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="e71cd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e71cd-122">-InputObject</span></span>
<span data-ttu-id="e71cd-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e71cd-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e71cd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71cd-124">-ResourceGroupName</span></span>
<span data-ttu-id="e71cd-125">Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="e71cd-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e71cd-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e71cd-126">-ResourceName</span></span>
<span data-ttu-id="e71cd-127">Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e71cd-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e71cd-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e71cd-128">-SubscriptionId</span></span>
<span data-ttu-id="e71cd-129">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="e71cd-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="e71cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71cd-130">CommonParameters</span></span>
<span data-ttu-id="e71cd-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e71cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71cd-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e71cd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71cd-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e71cd-133">INPUTS</span></span>

### <span data-ttu-id="e71cd-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e71cd-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e71cd-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e71cd-135">OUTPUTS</span></span>

### <span data-ttu-id="e71cd-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="e71cd-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="e71cd-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e71cd-137">NOTES</span></span>

<span data-ttu-id="e71cd-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e71cd-138">ALIASES</span></span>

<span data-ttu-id="e71cd-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e71cd-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e71cd-140">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="e71cd-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e71cd-141">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e71cd-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e71cd-142">INPUTOBJECT <IDigitalTwinsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="e71cd-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e71cd-143">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="e71cd-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e71cd-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e71cd-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e71cd-145">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e71cd-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e71cd-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="e71cd-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e71cd-147">`[ResourceName <String>]`: Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e71cd-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e71cd-148">`[SubscriptionId <String>]`: Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="e71cd-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e71cd-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e71cd-149">RELATED LINKS</span></span>

