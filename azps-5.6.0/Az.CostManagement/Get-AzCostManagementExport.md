---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: f318fcf3592c0b865684df57230f73a5f22ce024
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941912"
---
# <span data-ttu-id="b5ec9-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="b5ec9-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="b5ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ec9-103">Der Vorgang, um den Export für den definierten Bereich nach Exportname zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="b5ec9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5ec9-104">SYNTAX</span></span>

### <span data-ttu-id="b5ec9-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5ec9-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5ec9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b5ec9-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5ec9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5ec9-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b5ec9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5ec9-108">DESCRIPTION</span></span>
<span data-ttu-id="b5ec9-109">Der Vorgang, um den Export für den definierten Bereich nach Exportname zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="b5ec9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5ec9-110">EXAMPLES</span></span>

### <span data-ttu-id="b5ec9-111">Beispiel 1: Alle AzCostManagementExports nach Bereich erhalten</span><span class="sxs-lookup"><span data-stu-id="b5ec9-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="b5ec9-112">Alle AzCostManagementExports nach Scope</span><span class="sxs-lookup"><span data-stu-id="b5ec9-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="b5ec9-113">Beispiel 2: AzCostManagementExport nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="b5ec9-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="b5ec9-114">AzCostManagementExport nach Name und Umfang erhalten</span><span class="sxs-lookup"><span data-stu-id="b5ec9-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="b5ec9-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5ec9-115">PARAMETERS</span></span>

### <span data-ttu-id="b5ec9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ec9-116">-DefaultProfile</span></span>
<span data-ttu-id="b5ec9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ec9-118">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="b5ec9-118">-Expand</span></span>
<span data-ttu-id="b5ec9-119">Kann verwendet werden, um die Eigenschaften in einem Export zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="b5ec9-120">Derzeit wird nur "runHistory" unterstützt und gibt Informationen für die letzten 10 Exportausführungen zurück.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="b5ec9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5ec9-121">-InputObject</span></span>
<span data-ttu-id="b5ec9-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b5ec9-123">-Name</span></span>
<span data-ttu-id="b5ec9-124">Exportname.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec9-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="b5ec9-125">-Scope</span></span>
<span data-ttu-id="b5ec9-126">Dieser Parameter definiert den Umfang des Kostenmanagements aus verschiedenen Perspektiven : "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="b5ec9-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="b5ec9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ec9-127">CommonParameters</span></span>
<span data-ttu-id="b5ec9-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ec9-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5ec9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ec9-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5ec9-130">INPUTS</span></span>

### <span data-ttu-id="b5ec9-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="b5ec9-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="b5ec9-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5ec9-132">OUTPUTS</span></span>

### <span data-ttu-id="b5ec9-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="b5ec9-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="b5ec9-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5ec9-134">NOTES</span></span>

<span data-ttu-id="b5ec9-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b5ec9-135">ALIASES</span></span>

<span data-ttu-id="b5ec9-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b5ec9-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5ec9-137">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5ec9-138">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5ec9-139">INPUTOBJECT <ICostManagementIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b5ec9-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5ec9-140">`[AlertId <String>]`: Warnungs-ID</span><span class="sxs-lookup"><span data-stu-id="b5ec9-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="b5ec9-141">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="b5ec9-142">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das mit Dimensions-/Abfragevorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="b5ec9-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der mit Dimensions-/Abfragevorgängen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="b5ec9-144">Dies umfasst "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="b5ec9-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b5ec9-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5ec9-146">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b5ec9-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="b5ec9-147">Dies umfasst "Abonnements/{subscriptionId}" für den Abonnementbereich, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" für resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}" für den Bereich "Management Group", "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" für den Bereich "Externe Abrechnungskonten", "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" für den Bereich "Externes Abonnement".</span><span class="sxs-lookup"><span data-stu-id="b5ec9-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="b5ec9-148">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="b5ec9-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="b5ec9-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5ec9-149">RELATED LINKS</span></span>

