---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170687"
---
# <span data-ttu-id="bcc74-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="bcc74-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="bcc74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc74-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc74-103">Holen Sie sich die Ressource "DigitalTwinsInstances".</span><span class="sxs-lookup"><span data-stu-id="bcc74-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="bcc74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcc74-104">SYNTAX</span></span>

### <span data-ttu-id="bcc74-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcc74-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bcc74-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="bcc74-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bcc74-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bcc74-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcc74-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="bcc74-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bcc74-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcc74-109">DESCRIPTION</span></span>
<span data-ttu-id="bcc74-110">Holen Sie sich die Ressource "DigitalTwinsInstances".</span><span class="sxs-lookup"><span data-stu-id="bcc74-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="bcc74-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bcc74-111">EXAMPLES</span></span>

### <span data-ttu-id="bcc74-112">Beispiel 1: Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcc74-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="bcc74-113">Standardmäßiges Herunterladen aller DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="bcc74-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="bcc74-114">Beispiel 2: Erhalten</span><span class="sxs-lookup"><span data-stu-id="bcc74-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="bcc74-115">Die angegebene Datei "AzDigitalTwinsInstance" nach "ResourceName"</span><span class="sxs-lookup"><span data-stu-id="bcc74-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="bcc74-116">Beispiel 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bcc74-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="bcc74-117">Die angegebene Datei "AzDigitalTwinsInstance by Object"</span><span class="sxs-lookup"><span data-stu-id="bcc74-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="bcc74-118">Beispiel 4: Liste1</span><span class="sxs-lookup"><span data-stu-id="bcc74-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="bcc74-119">Alles von "DigitalTwinsInstance by ResourceGroupName" herunterladen</span><span class="sxs-lookup"><span data-stu-id="bcc74-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="bcc74-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcc74-120">PARAMETERS</span></span>

### <span data-ttu-id="bcc74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc74-121">-DefaultProfile</span></span>
<span data-ttu-id="bcc74-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcc74-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc74-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcc74-123">-InputObject</span></span>
<span data-ttu-id="bcc74-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bcc74-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bcc74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc74-125">-ResourceGroupName</span></span>
<span data-ttu-id="bcc74-126">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="bcc74-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="bcc74-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bcc74-127">-ResourceName</span></span>
<span data-ttu-id="bcc74-128">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="bcc74-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="bcc74-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcc74-129">-SubscriptionId</span></span>
<span data-ttu-id="bcc74-130">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="bcc74-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="bcc74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc74-131">CommonParameters</span></span>
<span data-ttu-id="bcc74-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc74-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcc74-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc74-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bcc74-134">INPUTS</span></span>

### <span data-ttu-id="bcc74-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="bcc74-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="bcc74-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bcc74-136">OUTPUTS</span></span>

### <span data-ttu-id="bcc74-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="bcc74-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="bcc74-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bcc74-138">NOTES</span></span>

<span data-ttu-id="bcc74-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bcc74-139">ALIASES</span></span>

<span data-ttu-id="bcc74-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="bcc74-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bcc74-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bcc74-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bcc74-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bcc74-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bcc74-143">INPUTOBJECT <IDigitalTwinsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bcc74-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bcc74-144">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="bcc74-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="bcc74-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="bcc74-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bcc74-146">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bcc74-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="bcc74-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="bcc74-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="bcc74-148">`[ResourceName <String>]`: Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="bcc74-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="bcc74-149">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="bcc74-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="bcc74-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bcc74-150">RELATED LINKS</span></span>

