---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298959"
---
# <span data-ttu-id="e3d77-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="e3d77-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="e3d77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3d77-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d77-103">Ruft das benutzerdefinierte Ressourcenanbieter Manifest ab.</span><span class="sxs-lookup"><span data-stu-id="e3d77-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="e3d77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3d77-104">SYNTAX</span></span>

### <span data-ttu-id="e3d77-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3d77-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3d77-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e3d77-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3d77-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3d77-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3d77-108">Liste</span><span class="sxs-lookup"><span data-stu-id="e3d77-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3d77-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3d77-109">DESCRIPTION</span></span>
<span data-ttu-id="e3d77-110">Ruft das benutzerdefinierte Ressourcenanbieter Manifest ab.</span><span class="sxs-lookup"><span data-stu-id="e3d77-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="e3d77-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3d77-111">EXAMPLES</span></span>

### <span data-ttu-id="e3d77-112">Beispiel 1: Auflisten aller benutzerdefinierten Anbieter in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e3d77-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="e3d77-113">Listet alle benutzerdefinierten Anbieter in einem Abonnement auf</span><span class="sxs-lookup"><span data-stu-id="e3d77-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="e3d77-114">Beispiel 2: Abrufen eines einzelnen benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="e3d77-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :

```

<span data-ttu-id="e3d77-115">Ruft Details für einen einzelnen benutzerdefinierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="e3d77-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="e3d77-116">Verwenden Sie Format-List, um Objektdetails auf dem Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3d77-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="e3d77-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3d77-117">PARAMETERS</span></span>

### <span data-ttu-id="e3d77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d77-118">-DefaultProfile</span></span>
<span data-ttu-id="e3d77-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3d77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d77-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e3d77-120">-InputObject</span></span>
<span data-ttu-id="e3d77-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e3d77-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d77-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e3d77-122">-Name</span></span>
<span data-ttu-id="e3d77-123">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="e3d77-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d77-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d77-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3d77-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3d77-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3d77-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e3d77-126">-SubscriptionId</span></span>
<span data-ttu-id="e3d77-127">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e3d77-127">The Azure subscription ID.</span></span>
<span data-ttu-id="e3d77-128">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="e3d77-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="e3d77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d77-129">CommonParameters</span></span>
<span data-ttu-id="e3d77-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d77-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3d77-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d77-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3d77-132">INPUTS</span></span>

### <span data-ttu-id="e3d77-133">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="e3d77-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="e3d77-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3d77-134">OUTPUTS</span></span>

### <span data-ttu-id="e3d77-135">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="e3d77-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="e3d77-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3d77-136">NOTES</span></span>

<span data-ttu-id="e3d77-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="e3d77-137">ALIASES</span></span>

<span data-ttu-id="e3d77-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3d77-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3d77-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3d77-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3d77-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e3d77-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3d77-141">Inputobject <ICustomProvidersIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e3d77-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3d77-142">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="e3d77-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="e3d77-143">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e3d77-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3d77-144">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3d77-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e3d77-145">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="e3d77-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="e3d77-146">`[Scope <String>]`: Der Bereich der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="e3d77-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="e3d77-147">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e3d77-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="e3d77-148">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="e3d77-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="e3d77-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3d77-149">RELATED LINKS</span></span>

