---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175269"
---
# <span data-ttu-id="aefa5-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="aefa5-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="aefa5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aefa5-102">SYNOPSIS</span></span>
<span data-ttu-id="aefa5-103">Besorgen Sie sich eine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefa5-103">Get an association.</span></span>

## <span data-ttu-id="aefa5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aefa5-104">SYNTAX</span></span>

### <span data-ttu-id="aefa5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="aefa5-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aefa5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="aefa5-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="aefa5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aefa5-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aefa5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aefa5-108">DESCRIPTION</span></span>
<span data-ttu-id="aefa5-109">Besorgen Sie sich eine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefa5-109">Get an association.</span></span>

## <span data-ttu-id="aefa5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aefa5-110">EXAMPLES</span></span>

### <span data-ttu-id="aefa5-111">Beispiel 1: Auflisten von benutzerdefinierten Anbieter Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="aefa5-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="aefa5-112">Auflisten aller benutzerdefinierten Anbieter Zuordnungen für einen bestimmten Bereich</span><span class="sxs-lookup"><span data-stu-id="aefa5-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="aefa5-113">Beispiel 2: Abrufen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="aefa5-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="aefa5-114">Abrufen von Details für eine einzelne customProvider-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="aefa5-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="aefa5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="aefa5-115">PARAMETERS</span></span>

### <span data-ttu-id="aefa5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefa5-116">-DefaultProfile</span></span>
<span data-ttu-id="aefa5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aefa5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aefa5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aefa5-118">-InputObject</span></span>
<span data-ttu-id="aefa5-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aefa5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aefa5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aefa5-120">-Name</span></span>
<span data-ttu-id="aefa5-121">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefa5-121">The name of the association.</span></span>

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

### <span data-ttu-id="aefa5-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="aefa5-122">-Scope</span></span>
<span data-ttu-id="aefa5-123">Der Bereich der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefa5-123">The scope of the association.</span></span>

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

### <span data-ttu-id="aefa5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefa5-124">CommonParameters</span></span>
<span data-ttu-id="aefa5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aefa5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefa5-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aefa5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefa5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aefa5-127">INPUTS</span></span>

### <span data-ttu-id="aefa5-128">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="aefa5-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="aefa5-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aefa5-129">OUTPUTS</span></span>

### <span data-ttu-id="aefa5-130">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="aefa5-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="aefa5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="aefa5-131">NOTES</span></span>

<span data-ttu-id="aefa5-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="aefa5-132">ALIASES</span></span>

<span data-ttu-id="aefa5-133">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aefa5-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aefa5-134">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aefa5-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aefa5-135">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="aefa5-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aefa5-136">Inputobject <ICustomProvidersIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="aefa5-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aefa5-137">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefa5-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="aefa5-138">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="aefa5-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aefa5-139">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aefa5-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="aefa5-140">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="aefa5-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="aefa5-141">`[Scope <String>]`: Der Bereich der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="aefa5-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="aefa5-142">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="aefa5-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="aefa5-143">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="aefa5-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="aefa5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aefa5-144">RELATED LINKS</span></span>

