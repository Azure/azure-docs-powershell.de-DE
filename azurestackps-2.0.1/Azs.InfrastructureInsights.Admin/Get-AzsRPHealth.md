---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005500"
---
# <span data-ttu-id="81920-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="81920-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="81920-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81920-102">SYNOPSIS</span></span>
<span data-ttu-id="81920-103">Gibt das angeforderte Dienst Integritäts Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="81920-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="81920-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81920-104">SYNTAX</span></span>

### <span data-ttu-id="81920-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="81920-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81920-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="81920-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81920-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81920-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="81920-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81920-108">DESCRIPTION</span></span>
<span data-ttu-id="81920-109">Gibt das angeforderte Dienst Integritäts Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="81920-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="81920-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81920-110">EXAMPLES</span></span>

### <span data-ttu-id="81920-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="81920-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="81920-112">Gibt eine Liste der Integritätsstatus jedes Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="81920-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="81920-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="81920-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="81920-114">Gibt den Status eines Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="81920-114">Returns a service's health.</span></span>

## <span data-ttu-id="81920-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="81920-115">PARAMETERS</span></span>

### <span data-ttu-id="81920-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81920-116">-DefaultProfile</span></span>
<span data-ttu-id="81920-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81920-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81920-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="81920-118">-Filter</span></span>
<span data-ttu-id="81920-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="81920-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="81920-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81920-120">-InputObject</span></span>
<span data-ttu-id="81920-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="81920-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81920-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="81920-122">-Location</span></span>
<span data-ttu-id="81920-123">Name der Region</span><span class="sxs-lookup"><span data-stu-id="81920-123">Name of the region</span></span>

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

### <span data-ttu-id="81920-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81920-124">-ResourceGroupName</span></span>
<span data-ttu-id="81920-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81920-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="81920-126">-ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="81920-126">-ServiceHealth</span></span>
<span data-ttu-id="81920-127">Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="81920-127">Service Health name.</span></span>

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

### <span data-ttu-id="81920-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="81920-128">-SubscriptionId</span></span>
<span data-ttu-id="81920-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="81920-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="81920-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="81920-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="81920-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81920-131">CommonParameters</span></span>
<span data-ttu-id="81920-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81920-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81920-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81920-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81920-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81920-134">INPUTS</span></span>

### <span data-ttu-id="81920-135">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="81920-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="81920-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81920-136">OUTPUTS</span></span>

### <span data-ttu-id="81920-137">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="81920-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="81920-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="81920-138">NOTES</span></span>

<span data-ttu-id="81920-139">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81920-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81920-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="81920-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="81920-141">Inputobject <IInfrastructureInsightsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="81920-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81920-142">`[AlertName <String>]`: Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="81920-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="81920-143">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="81920-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81920-144">`[Location <String>]`: Name der Region</span><span class="sxs-lookup"><span data-stu-id="81920-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="81920-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81920-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="81920-146">`[ResourceRegistrationId <String>]`: Ressourcen Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="81920-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="81920-147">`[ServiceHealth <String>]`: Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="81920-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="81920-148">`[ServiceRegistrationId <String>]`: Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="81920-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="81920-149">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="81920-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="81920-150">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="81920-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="81920-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81920-151">RELATED LINKS</span></span>

