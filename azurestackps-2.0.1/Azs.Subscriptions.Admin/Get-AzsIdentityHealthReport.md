---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005442"
---
# <span data-ttu-id="46541-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="46541-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="46541-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46541-102">SYNOPSIS</span></span>
<span data-ttu-id="46541-103">Überprüft den Identitätsstatus</span><span class="sxs-lookup"><span data-stu-id="46541-103">Checks the identity health</span></span>

## <span data-ttu-id="46541-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46541-104">SYNTAX</span></span>

### <span data-ttu-id="46541-105">Überprüfen (Standard)</span><span class="sxs-lookup"><span data-stu-id="46541-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="46541-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46541-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46541-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46541-107">DESCRIPTION</span></span>
<span data-ttu-id="46541-108">Überprüft den Identitätsstatus</span><span class="sxs-lookup"><span data-stu-id="46541-108">Checks the identity health</span></span>

## <span data-ttu-id="46541-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46541-109">EXAMPLES</span></span>

### <span data-ttu-id="46541-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46541-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="46541-111">Abrufen des Status des Identitäts Zustands.</span><span class="sxs-lookup"><span data-stu-id="46541-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="46541-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="46541-112">PARAMETERS</span></span>

### <span data-ttu-id="46541-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46541-113">-DefaultProfile</span></span>
<span data-ttu-id="46541-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46541-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46541-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46541-115">-InputObject</span></span>
<span data-ttu-id="46541-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="46541-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="46541-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="46541-117">-SubscriptionId</span></span>
<span data-ttu-id="46541-118">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="46541-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46541-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46541-119">-Confirm</span></span>
<span data-ttu-id="46541-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46541-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46541-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46541-121">-WhatIf</span></span>
<span data-ttu-id="46541-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46541-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46541-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46541-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="46541-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46541-124">CommonParameters</span></span>
<span data-ttu-id="46541-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46541-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46541-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46541-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46541-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46541-127">INPUTS</span></span>

### <span data-ttu-id="46541-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="46541-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="46541-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46541-129">OUTPUTS</span></span>

### <span data-ttu-id="46541-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IIdentityHealthCheckReportDefinition</span><span class="sxs-lookup"><span data-stu-id="46541-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="46541-131">Aliase</span><span class="sxs-lookup"><span data-stu-id="46541-131">ALIASES</span></span>

## <span data-ttu-id="46541-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="46541-132">NOTES</span></span>

<span data-ttu-id="46541-133">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46541-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46541-134">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="46541-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="46541-135">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="46541-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46541-136">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="46541-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="46541-137">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="46541-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="46541-138">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="46541-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46541-139">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="46541-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="46541-140">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="46541-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="46541-141">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="46541-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="46541-142">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="46541-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="46541-143">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="46541-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="46541-144">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="46541-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="46541-145">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="46541-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="46541-146">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="46541-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="46541-147">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="46541-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="46541-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="46541-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="46541-149">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="46541-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="46541-150">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="46541-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="46541-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46541-151">RELATED LINKS</span></span>

