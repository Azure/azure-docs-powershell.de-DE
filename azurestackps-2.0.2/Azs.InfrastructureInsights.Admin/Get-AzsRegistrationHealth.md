---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006912"
---
# <span data-ttu-id="94b95-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="94b95-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="94b95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94b95-102">SYNOPSIS</span></span>
<span data-ttu-id="94b95-103">Gibt die angeforderten Integritätsinformationen zu einer Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="94b95-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="94b95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b95-104">SYNTAX</span></span>

### <span data-ttu-id="94b95-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="94b95-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94b95-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="94b95-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94b95-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94b95-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="94b95-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94b95-108">DESCRIPTION</span></span>
<span data-ttu-id="94b95-109">Gibt die angeforderten Integritätsinformationen zu einer Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="94b95-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="94b95-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94b95-110">EXAMPLES</span></span>

### <span data-ttu-id="94b95-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="94b95-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="94b95-112">Gibt eine Liste der Status der einzelnen Ressourcen unter einem Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="94b95-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="94b95-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="94b95-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="94b95-114">Gibt den Integritätsstatus unter einem für Microsoft. Fabric. admin zurück.</span><span class="sxs-lookup"><span data-stu-id="94b95-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="94b95-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="94b95-115">PARAMETERS</span></span>

### <span data-ttu-id="94b95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b95-116">-DefaultProfile</span></span>
<span data-ttu-id="94b95-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94b95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94b95-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="94b95-118">-Filter</span></span>
<span data-ttu-id="94b95-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="94b95-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94b95-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94b95-120">-InputObject</span></span>
<span data-ttu-id="94b95-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="94b95-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94b95-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="94b95-122">-Location</span></span>
<span data-ttu-id="94b95-123">Name der Region</span><span class="sxs-lookup"><span data-stu-id="94b95-123">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94b95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b95-124">-ResourceGroupName</span></span>
<span data-ttu-id="94b95-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94b95-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="94b95-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="94b95-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="94b95-127">Ressourcen Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="94b95-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="94b95-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="94b95-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="94b95-129">Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="94b95-129">Service registration ID.</span></span>

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

### <span data-ttu-id="94b95-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="94b95-130">-SubscriptionId</span></span>
<span data-ttu-id="94b95-131">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="94b95-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94b95-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="94b95-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94b95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b95-133">CommonParameters</span></span>
<span data-ttu-id="94b95-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b95-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94b95-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b95-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94b95-136">INPUTS</span></span>

### <span data-ttu-id="94b95-137">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="94b95-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="94b95-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94b95-138">OUTPUTS</span></span>

### <span data-ttu-id="94b95-139">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="94b95-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="94b95-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="94b95-140">NOTES</span></span>

<span data-ttu-id="94b95-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="94b95-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94b95-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="94b95-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="94b95-143">Inputobject <IInfrastructureInsightsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="94b95-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94b95-144">`[AlertName <String>]`: Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="94b95-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="94b95-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="94b95-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94b95-146">`[Location <String>]`: Name der Region</span><span class="sxs-lookup"><span data-stu-id="94b95-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="94b95-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94b95-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="94b95-148">`[ResourceRegistrationId <String>]`: Ressourcen Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="94b95-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="94b95-149">`[ServiceHealth <String>]`: Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="94b95-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="94b95-150">`[ServiceRegistrationId <String>]`: Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="94b95-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="94b95-151">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="94b95-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94b95-152">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="94b95-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94b95-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94b95-153">RELATED LINKS</span></span>

