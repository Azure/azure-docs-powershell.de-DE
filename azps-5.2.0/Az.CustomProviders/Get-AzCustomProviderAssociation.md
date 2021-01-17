---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369171"
---
# <span data-ttu-id="660b9-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="660b9-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="660b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="660b9-102">SYNOPSIS</span></span>
<span data-ttu-id="660b9-103">Eine Zuordnung erhalten.</span><span class="sxs-lookup"><span data-stu-id="660b9-103">Get an association.</span></span>

## <span data-ttu-id="660b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="660b9-104">SYNTAX</span></span>

### <span data-ttu-id="660b9-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="660b9-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="660b9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="660b9-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="660b9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="660b9-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="660b9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="660b9-108">DESCRIPTION</span></span>
<span data-ttu-id="660b9-109">Eine Zuordnung erhalten.</span><span class="sxs-lookup"><span data-stu-id="660b9-109">Get an association.</span></span>

## <span data-ttu-id="660b9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="660b9-110">EXAMPLES</span></span>

### <span data-ttu-id="660b9-111">Beispiel 1: Auflisten benutzerdefinierter Anbieterzuordnungen</span><span class="sxs-lookup"><span data-stu-id="660b9-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="660b9-112">Listen Sie alle benutzerdefinierten Anbieterzuordnungen für einen bestimmten Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="660b9-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="660b9-113">Beispiel 2: Zuordnung erhalten</span><span class="sxs-lookup"><span data-stu-id="660b9-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="660b9-114">Details zu einer einzelnen CustomProvider-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="660b9-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="660b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="660b9-115">PARAMETERS</span></span>

### <span data-ttu-id="660b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660b9-116">-DefaultProfile</span></span>
<span data-ttu-id="660b9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="660b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="660b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="660b9-118">-InputObject</span></span>
<span data-ttu-id="660b9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="660b9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="660b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="660b9-120">-Name</span></span>
<span data-ttu-id="660b9-121">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="660b9-121">The name of the association.</span></span>

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

### <span data-ttu-id="660b9-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="660b9-122">-Scope</span></span>
<span data-ttu-id="660b9-123">Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="660b9-123">The scope of the association.</span></span>

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

### <span data-ttu-id="660b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660b9-124">CommonParameters</span></span>
<span data-ttu-id="660b9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660b9-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="660b9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660b9-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="660b9-127">INPUTS</span></span>

### <span data-ttu-id="660b9-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="660b9-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="660b9-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="660b9-129">OUTPUTS</span></span>

### <span data-ttu-id="660b9-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="660b9-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="660b9-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="660b9-131">NOTES</span></span>

<span data-ttu-id="660b9-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="660b9-132">ALIASES</span></span>

<span data-ttu-id="660b9-133">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="660b9-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="660b9-134">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="660b9-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="660b9-135">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="660b9-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="660b9-136">INPUTOBJECT <ICustomProvidersIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="660b9-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="660b9-137">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="660b9-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="660b9-138">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="660b9-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="660b9-139">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="660b9-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="660b9-140">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="660b9-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="660b9-141">`[Scope <String>]`: Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="660b9-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="660b9-142">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="660b9-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="660b9-143">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="660b9-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="660b9-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="660b9-144">RELATED LINKS</span></span>

