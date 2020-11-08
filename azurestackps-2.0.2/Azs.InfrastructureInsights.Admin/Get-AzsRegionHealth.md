---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006915"
---
# <span data-ttu-id="003e4-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="003e4-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="003e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="003e4-102">SYNOPSIS</span></span>
<span data-ttu-id="003e4-103">Gibt den angeforderten Integritätsstatus eines Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="003e4-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="003e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="003e4-104">SYNTAX</span></span>

### <span data-ttu-id="003e4-105">Abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="003e4-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="003e4-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="003e4-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="003e4-107">Liste</span><span class="sxs-lookup"><span data-stu-id="003e4-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="003e4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="003e4-108">DESCRIPTION</span></span>
<span data-ttu-id="003e4-109">Gibt den angeforderten Integritätsstatus eines Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="003e4-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="003e4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="003e4-110">EXAMPLES</span></span>

### <span data-ttu-id="003e4-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="003e4-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="003e4-112">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="003e4-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="003e4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="003e4-113">PARAMETERS</span></span>

### <span data-ttu-id="003e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003e4-114">-DefaultProfile</span></span>
<span data-ttu-id="003e4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="003e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="003e4-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="003e4-116">-Filter</span></span>
<span data-ttu-id="003e4-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="003e4-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="003e4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="003e4-118">-InputObject</span></span>
<span data-ttu-id="003e4-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="003e4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="003e4-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="003e4-120">-Location</span></span>
<span data-ttu-id="003e4-121">Name der Region</span><span class="sxs-lookup"><span data-stu-id="003e4-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="003e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="003e4-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="003e4-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="003e4-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="003e4-124">-SubscriptionId</span></span>
<span data-ttu-id="003e4-125">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="003e4-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="003e4-126">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="003e4-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="003e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003e4-127">CommonParameters</span></span>
<span data-ttu-id="003e4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003e4-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="003e4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003e4-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="003e4-130">INPUTS</span></span>

### <span data-ttu-id="003e4-131">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="003e4-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="003e4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="003e4-132">OUTPUTS</span></span>

### <span data-ttu-id="003e4-133">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IRegionHealth</span><span class="sxs-lookup"><span data-stu-id="003e4-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="003e4-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="003e4-134">NOTES</span></span>

<span data-ttu-id="003e4-135">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="003e4-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="003e4-136">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="003e4-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="003e4-137">Inputobject <IInfrastructureInsightsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="003e4-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="003e4-138">`[AlertName <String>]`: Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="003e4-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="003e4-139">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="003e4-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="003e4-140">`[Location <String>]`: Name der Region</span><span class="sxs-lookup"><span data-stu-id="003e4-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="003e4-141">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="003e4-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="003e4-142">`[ResourceRegistrationId <String>]`: Ressourcen Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="003e4-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="003e4-143">`[ServiceHealth <String>]`: Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="003e4-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="003e4-144">`[ServiceRegistrationId <String>]`: Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="003e4-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="003e4-145">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="003e4-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="003e4-146">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="003e4-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="003e4-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="003e4-147">RELATED LINKS</span></span>

