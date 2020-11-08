---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005504"
---
# <span data-ttu-id="8e0b5-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="8e0b5-101">Get-AzsAlert</span></span>

## <span data-ttu-id="8e0b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0b5-103">Gibt die angeforderte Benachrichtigung zurück.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-103">Returns the requested alert.</span></span>

## <span data-ttu-id="8e0b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e0b5-104">SYNTAX</span></span>

### <span data-ttu-id="8e0b5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e0b5-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e0b5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="8e0b5-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e0b5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e0b5-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e0b5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0b5-108">DESCRIPTION</span></span>
<span data-ttu-id="8e0b5-109">Gibt die angeforderte Benachrichtigung zurück.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-109">Returns the requested alert.</span></span>

## <span data-ttu-id="8e0b5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e0b5-110">EXAMPLES</span></span>

### <span data-ttu-id="8e0b5-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="8e0b5-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="8e0b5-112">Erhalten Sie eine Benachrichtigung nach Namen.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-112">Get an alert by Name.</span></span>

### <span data-ttu-id="8e0b5-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="8e0b5-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="8e0b5-114">Rufen Sie alle aktiven Benachrichtigungen ab, und zeigen Sie deren Fehler und Titel an.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="8e0b5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e0b5-115">PARAMETERS</span></span>

### <span data-ttu-id="8e0b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0b5-116">-DefaultProfile</span></span>
<span data-ttu-id="8e0b5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e0b5-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="8e0b5-118">-Filter</span></span>
<span data-ttu-id="8e0b5-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="8e0b5-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="8e0b5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e0b5-120">-InputObject</span></span>
<span data-ttu-id="8e0b5-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8e0b5-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="8e0b5-122">-Location</span></span>
<span data-ttu-id="8e0b5-123">Name der Region</span><span class="sxs-lookup"><span data-stu-id="8e0b5-123">Name of the region</span></span>

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

### <span data-ttu-id="8e0b5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8e0b5-124">-Name</span></span>
<span data-ttu-id="8e0b5-125">Der Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e0b5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0b5-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e0b5-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e0b5-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8e0b5-128">-SubscriptionId</span></span>
<span data-ttu-id="8e0b5-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e0b5-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8e0b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0b5-131">CommonParameters</span></span>
<span data-ttu-id="8e0b5-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0b5-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e0b5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0b5-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e0b5-134">INPUTS</span></span>

### <span data-ttu-id="8e0b5-135">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8e0b5-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="8e0b5-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e0b5-136">OUTPUTS</span></span>

### <span data-ttu-id="8e0b5-137">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="8e0b5-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="8e0b5-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e0b5-138">NOTES</span></span>

<span data-ttu-id="8e0b5-139">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e0b5-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8e0b5-141">Inputobject <IInfrastructureInsightsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="8e0b5-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e0b5-142">`[AlertName <String>]`: Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="8e0b5-143">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="8e0b5-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e0b5-144">`[Location <String>]`: Name der Region</span><span class="sxs-lookup"><span data-stu-id="8e0b5-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="8e0b5-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8e0b5-146">`[ResourceRegistrationId <String>]`: Ressourcen Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="8e0b5-147">`[ServiceHealth <String>]`: Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="8e0b5-148">`[ServiceRegistrationId <String>]`: Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="8e0b5-149">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8e0b5-150">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8e0b5-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8e0b5-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e0b5-151">RELATED LINKS</span></span>

