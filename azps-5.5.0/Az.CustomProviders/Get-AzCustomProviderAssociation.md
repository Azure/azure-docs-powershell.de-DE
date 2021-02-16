---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163900"
---
# <span data-ttu-id="10132-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="10132-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="10132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10132-102">SYNOPSIS</span></span>
<span data-ttu-id="10132-103">Eine Zuordnung erhalten.</span><span class="sxs-lookup"><span data-stu-id="10132-103">Get an association.</span></span>

## <span data-ttu-id="10132-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10132-104">SYNTAX</span></span>

### <span data-ttu-id="10132-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="10132-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="10132-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="10132-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="10132-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="10132-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="10132-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10132-108">DESCRIPTION</span></span>
<span data-ttu-id="10132-109">Eine Zuordnung erhalten.</span><span class="sxs-lookup"><span data-stu-id="10132-109">Get an association.</span></span>

## <span data-ttu-id="10132-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10132-110">EXAMPLES</span></span>

### <span data-ttu-id="10132-111">Beispiel 1: Auflisten benutzerdefinierter Anbieterzuordnungen</span><span class="sxs-lookup"><span data-stu-id="10132-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="10132-112">Listen Sie alle benutzerdefinierten Anbieterzuordnungen für einen bestimmten Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="10132-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="10132-113">Beispiel 2: Zuordnung erhalten</span><span class="sxs-lookup"><span data-stu-id="10132-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="10132-114">Details zu einer einzelnen CustomProvider-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="10132-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="10132-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10132-115">PARAMETERS</span></span>

### <span data-ttu-id="10132-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10132-116">-DefaultProfile</span></span>
<span data-ttu-id="10132-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10132-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10132-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10132-118">-InputObject</span></span>
<span data-ttu-id="10132-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="10132-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="10132-120">-Name</span><span class="sxs-lookup"><span data-stu-id="10132-120">-Name</span></span>
<span data-ttu-id="10132-121">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="10132-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10132-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="10132-122">-Scope</span></span>
<span data-ttu-id="10132-123">Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="10132-123">The scope of the association.</span></span>

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

### <span data-ttu-id="10132-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10132-124">CommonParameters</span></span>
<span data-ttu-id="10132-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10132-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10132-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10132-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10132-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10132-127">INPUTS</span></span>

### <span data-ttu-id="10132-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="10132-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="10132-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10132-129">OUTPUTS</span></span>

### <span data-ttu-id="10132-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="10132-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="10132-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="10132-131">NOTES</span></span>

<span data-ttu-id="10132-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="10132-132">ALIASES</span></span>

<span data-ttu-id="10132-133">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="10132-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10132-134">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="10132-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10132-135">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10132-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10132-136">INPUTOBJECT <ICustomProvidersIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="10132-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="10132-137">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="10132-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="10132-138">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="10132-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10132-139">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10132-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="10132-140">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="10132-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="10132-141">`[Scope <String>]`: Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="10132-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="10132-142">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="10132-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="10132-143">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="10132-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="10132-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="10132-144">RELATED LINKS</span></span>

