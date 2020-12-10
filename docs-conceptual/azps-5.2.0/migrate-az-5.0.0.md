---
title: Migrationsleitfaden für Az 5.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit Breaking Changes, die in Az-Version 5.0.0 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856425"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="e680e-103">Migrationsleitfaden für Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="e680e-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="e680e-104">In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 4.0.0 und 5.0.0 von Az vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="e680e-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="e680e-105">Migrationsleitfaden für Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="e680e-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="e680e-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e680e-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="e680e-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e680e-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="e680e-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e680e-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="e680e-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e680e-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="e680e-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e680e-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="e680e-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e680e-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="e680e-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e680e-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="e680e-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e680e-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="e680e-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e680e-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="e680e-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e680e-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="e680e-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e680e-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="e680e-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e680e-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="e680e-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e680e-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="e680e-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e680e-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="e680e-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="e680e-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="e680e-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="e680e-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="e680e-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e680e-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="e680e-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="e680e-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="e680e-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="e680e-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="e680e-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="e680e-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="e680e-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="e680e-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="e680e-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="e680e-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="e680e-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="e680e-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="e680e-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="e680e-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="e680e-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="e680e-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="e680e-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="e680e-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="e680e-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="e680e-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="e680e-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="e680e-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="e680e-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="e680e-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="e680e-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="e680e-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="e680e-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="e680e-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="e680e-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="e680e-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="e680e-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="e680e-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="e680e-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="e680e-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="e680e-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e680e-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="e680e-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e680e-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="e680e-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="e680e-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="e680e-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e680e-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="e680e-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e680e-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="e680e-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e680e-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="e680e-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="e680e-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="e680e-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="e680e-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="e680e-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="e680e-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e680e-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="e680e-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e680e-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="e680e-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e680e-169">New-AzAksCluster</span></span>

- <span data-ttu-id="e680e-170">Der Parameter `NodeOsType` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden. Er lautet immer `Linux`.</span><span class="sxs-lookup"><span data-stu-id="e680e-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="e680e-171">Der Alias `ClientIdAndSecret` für den Parameter `ServicePrincipalIdAndSecret` wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e680e-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="e680e-172">Der Standardwert von `NodeVmSetType` wurde von `AvailabilitySet` in `VirtualMachineScaleSets` geändert.</span><span class="sxs-lookup"><span data-stu-id="e680e-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="e680e-173">Der Standardwert von `NetworkPlugin` wurde von `none` in `azure` geändert.</span><span class="sxs-lookup"><span data-stu-id="e680e-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-174">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-175">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="e680e-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e680e-176">Set-AzAksCluster</span></span>

<span data-ttu-id="e680e-177">Der Alias `ClientIdAndSecret` für den Parameter `ServicePrincipalIdAndSecret` wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e680e-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-178">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-179">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="e680e-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e680e-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="e680e-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e680e-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="e680e-182">Der Parameter `StorageAccountName` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-183">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="e680e-184">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-184">After</span></span>

<span data-ttu-id="e680e-185">`Classic` wurde als veraltet eingestuft, und der Parameter `StorageAccountName` wurde entfernt, da er nur mit der klassischen Containerregistrierung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e680e-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="e680e-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e680e-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="e680e-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e680e-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="e680e-188">Der Switch-Parameter `IncludeSlot` wurde aus allen Parametersätzen von „`Get-AzFunctionApp`“ entfernt (bis auf einen).</span><span class="sxs-lookup"><span data-stu-id="e680e-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="e680e-189">Das Cmdlet unterstützt jetzt das Abrufen von Bereitstellungsslots in den Ergebnissen, wenn `-IncludeSlot` angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e680e-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="e680e-190">Diese Funktionalität war in der vorherigen Cmdlet-Version beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e680e-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="e680e-191">Der Fehler ist jetzt aber behoben.</span><span class="sxs-lookup"><span data-stu-id="e680e-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="e680e-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e680e-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="e680e-193">`-DisableApplicationInsights` wurde in `New-AzFunctionApp` korrigiert, damit bei Angabe dieser Option kein Application Insights-Projekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e680e-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="e680e-194">Die Unterstützung für die Erstellung von PowerShell 6.2-Funktions-Apps wurde entfernt, da für PowerShell 6.2 der EOL-Zeitpunkt erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="e680e-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="e680e-195">Für Kunden wird derzeit empfohlen, stattdessen PowerShell 7.0-Funktions-Apps zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e680e-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="e680e-196">Es wurde festgelegt, dass in Functions-Version 3 von Windows für PowerShell-Funktions-Apps anstelle der Runtime-Standardversion 6.2 die Version 7.0 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e680e-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="e680e-197">Es wurde festgelegt, dass in Functions-Version 3 von Windows/Linux für Node-Funktions-Apps anstelle der Runtime-Standardversion 10 die Version 12 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e680e-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="e680e-198">Benutzer können aber weiterhin Node 10-Funktions-Apps erstellen, indem sie `-Runtime Node` und `-RuntimeVersion 10` angeben.</span><span class="sxs-lookup"><span data-stu-id="e680e-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="e680e-199">Es wurde festgelegt, dass in Functions-Version 3 von Linux für Python-Funktions-Apps anstelle der Runtime-Standardversion 3.7 die Version 3.8 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e680e-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="e680e-200">Benutzer können aber weiterhin Python 3.7-Funktions-Apps erstellen, indem sie `-Runtime Python` und `-RuntimeVersion 3.7` angeben.</span><span class="sxs-lookup"><span data-stu-id="e680e-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-201">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-201">Before</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a><span data-ttu-id="e680e-202">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-202">After</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a><span data-ttu-id="e680e-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e680e-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="e680e-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e680e-204">New-AzKeyVault</span></span>

<span data-ttu-id="e680e-205">Der Parameter `DisableSoftDelete` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-206">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="e680e-207">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-207">After</span></span>

<span data-ttu-id="e680e-208">Die Möglichkeit zum Aktualisieren der Einstellung für das vorläufige Löschen wurde in Az.KeyVault 3.0.0 als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="e680e-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="e680e-209">Weitere Informationen: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="e680e-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="e680e-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e680e-210">Update-AzKeyVault</span></span>

<span data-ttu-id="e680e-211">Die Parameter `EnableSoftDelete` und `SoftDeleteRetentionInDays` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-212">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="e680e-213">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-213">After</span></span>

<span data-ttu-id="e680e-214">Die Möglichkeit zum Aktualisieren der Einstellung für das vorläufige Löschen wurde in Az.KeyVault 3.0.0 als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="e680e-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="e680e-215">Weitere Informationen: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="e680e-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="e680e-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e680e-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="e680e-217">Die `SecretValueText`-Eigenschaft vom Typ `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="e680e-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="e680e-218">Die Eigenschaft `SecretValueText` wurde durch `SecretValue` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e680e-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-219">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="e680e-220">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="e680e-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e680e-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="e680e-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e680e-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="e680e-223">Der Parameter `ResourceId` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-224">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-225">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="e680e-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="e680e-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="e680e-227">Die Parameter `RegistrationDefinitionName` und `RegistrationDefinitionResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-228">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-229">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="e680e-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="e680e-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="e680e-231">Die Parameter `Id` und `ResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-232">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-233">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="e680e-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e680e-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="e680e-235">Die Parameter `Id` und `ResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-236">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-237">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="e680e-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="e680e-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="e680e-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="e680e-240">Der Parameter `ApiVersion` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-241">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-242">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="e680e-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="e680e-244">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="e680e-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-245">Get-AzDeployment</span></span>

<span data-ttu-id="e680e-246">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="e680e-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="e680e-248">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="e680e-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="e680e-250">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="e680e-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="e680e-252">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="e680e-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="e680e-254">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="e680e-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="e680e-256">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="e680e-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-257">New-AzDeployment</span></span>

<span data-ttu-id="e680e-258">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="e680e-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="e680e-260">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="e680e-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="e680e-262">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="e680e-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-263">Remove-AzDeployment</span></span>

<span data-ttu-id="e680e-264">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="e680e-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="e680e-266">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="e680e-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="e680e-268">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="e680e-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="e680e-270">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="e680e-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="e680e-272">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="e680e-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="e680e-274">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="e680e-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-275">Stop-AzDeployment</span></span>

<span data-ttu-id="e680e-276">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="e680e-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="e680e-278">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="e680e-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="e680e-280">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="e680e-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-281">Test-AzDeployment</span></span>

<span data-ttu-id="e680e-282">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="e680e-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="e680e-284">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="e680e-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="e680e-286">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="e680e-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e680e-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="e680e-288">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="e680e-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="e680e-290">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="e680e-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="e680e-292">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="e680e-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="e680e-294">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="e680e-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e680e-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="e680e-296">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="e680e-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="e680e-298">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="e680e-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e680e-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="e680e-300">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="e680e-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="e680e-302">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="e680e-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e680e-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="e680e-304">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="e680e-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="e680e-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e680e-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="e680e-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e680e-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="e680e-307">Der Parameter `IsAzureADOnlyAuthentication` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-308">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="e680e-309">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="e680e-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="e680e-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="e680e-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e680e-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="e680e-312">Die Parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` und `RestorePoint` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-313">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="e680e-314">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="e680e-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e680e-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="e680e-316">Die Parameter `Suspend` und `Resume` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="e680e-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e680e-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="e680e-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="e680e-319">Der Parameter `PrivateLinkResourceType` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-320">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="e680e-321">Danach</span><span class="sxs-lookup"><span data-stu-id="e680e-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="e680e-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="e680e-323">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="e680e-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="e680e-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="e680e-325">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="e680e-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="e680e-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="e680e-327">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="e680e-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="e680e-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e680e-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="e680e-329">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="e680e-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="e680e-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e680e-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="e680e-331">Die Parameter `FilterType` und `FilterItem` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="e680e-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="e680e-332">Vorher</span><span class="sxs-lookup"><span data-stu-id="e680e-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="e680e-333">Nach</span><span class="sxs-lookup"><span data-stu-id="e680e-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
