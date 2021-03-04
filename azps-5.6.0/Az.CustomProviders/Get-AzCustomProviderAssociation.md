---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: f7c36ca53b00c0fc99e5afc6e6ba74f4cff62afb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943035"
---
# <span data-ttu-id="406f6-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="406f6-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="406f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="406f6-102">SYNOPSIS</span></span>
<span data-ttu-id="406f6-103">Holen Sie sich eine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="406f6-103">Get an association.</span></span>

## <span data-ttu-id="406f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="406f6-104">SYNTAX</span></span>

### <span data-ttu-id="406f6-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="406f6-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="406f6-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="406f6-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="406f6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="406f6-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="406f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="406f6-108">DESCRIPTION</span></span>
<span data-ttu-id="406f6-109">Holen Sie sich eine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="406f6-109">Get an association.</span></span>

## <span data-ttu-id="406f6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="406f6-110">EXAMPLES</span></span>

### <span data-ttu-id="406f6-111">Beispiel 1: Auflisten benutzerdefinierter Anbieterzuordnungen</span><span class="sxs-lookup"><span data-stu-id="406f6-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="406f6-112">Listen Sie alle benutzerdefinierten Anbieterzuordnungen für einen bestimmten Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="406f6-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="406f6-113">Beispiel 2: Erhalten einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="406f6-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="406f6-114">Details zu einer einzelnen CustomProvider-Zuordnung erhalten</span><span class="sxs-lookup"><span data-stu-id="406f6-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="406f6-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="406f6-115">PARAMETERS</span></span>

### <span data-ttu-id="406f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406f6-116">-DefaultProfile</span></span>
<span data-ttu-id="406f6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="406f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="406f6-118">-InputObject</span></span>
<span data-ttu-id="406f6-119">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="406f6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="406f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="406f6-120">-Name</span></span>
<span data-ttu-id="406f6-121">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="406f6-121">The name of the association.</span></span>

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

### <span data-ttu-id="406f6-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="406f6-122">-Scope</span></span>
<span data-ttu-id="406f6-123">Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="406f6-123">The scope of the association.</span></span>

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

### <span data-ttu-id="406f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406f6-124">CommonParameters</span></span>
<span data-ttu-id="406f6-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406f6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="406f6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406f6-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="406f6-127">INPUTS</span></span>

### <span data-ttu-id="406f6-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="406f6-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="406f6-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="406f6-129">OUTPUTS</span></span>

### <span data-ttu-id="406f6-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="406f6-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="406f6-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="406f6-131">NOTES</span></span>

<span data-ttu-id="406f6-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="406f6-132">ALIASES</span></span>

<span data-ttu-id="406f6-133">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="406f6-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="406f6-134">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="406f6-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="406f6-135">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="406f6-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="406f6-136">INPUTOBJECT <ICustomProvidersIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="406f6-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="406f6-137">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="406f6-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="406f6-138">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="406f6-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="406f6-139">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="406f6-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="406f6-140">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="406f6-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="406f6-141">`[Scope <String>]`: Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="406f6-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="406f6-142">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="406f6-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="406f6-143">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="406f6-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="406f6-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="406f6-144">RELATED LINKS</span></span>

