---
title: Migrationsleitfaden für Az 5.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit Breaking Changes, die in Az-Version 5.0.0 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: edfbe14ae3a42bb0b385fe9d6b5fa681a1aa2101
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684926"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="0a9f1-103">Migrationsleitfaden für Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="0a9f1-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="0a9f1-104">In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 4.0.0 und 5.0.0 von Az vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="0a9f1-105">Migrationsleitfaden für Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="0a9f1-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="0a9f1-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a9f1-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="0a9f1-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0a9f1-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="0a9f1-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0a9f1-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="0a9f1-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a9f1-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="0a9f1-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a9f1-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="0a9f1-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="0a9f1-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="0a9f1-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0a9f1-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="0a9f1-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0a9f1-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="0a9f1-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a9f1-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="0a9f1-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a9f1-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="0a9f1-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a9f1-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="0a9f1-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0a9f1-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="0a9f1-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0a9f1-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="0a9f1-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0a9f1-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="0a9f1-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="0a9f1-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="0a9f1-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0a9f1-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="0a9f1-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="0a9f1-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="0a9f1-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="0a9f1-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="0a9f1-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="0a9f1-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="0a9f1-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="0a9f1-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="0a9f1-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="0a9f1-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="0a9f1-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="0a9f1-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="0a9f1-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="0a9f1-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="0a9f1-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="0a9f1-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="0a9f1-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="0a9f1-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="0a9f1-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="0a9f1-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="0a9f1-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="0a9f1-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="0a9f1-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="0a9f1-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="0a9f1-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="0a9f1-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="0a9f1-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="0a9f1-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="0a9f1-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="0a9f1-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="0a9f1-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="0a9f1-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="0a9f1-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="0a9f1-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="0a9f1-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a9f1-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="0a9f1-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0a9f1-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="0a9f1-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="0a9f1-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="0a9f1-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a9f1-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="0a9f1-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a9f1-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="0a9f1-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a9f1-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="0a9f1-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="0a9f1-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="0a9f1-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="0a9f1-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="0a9f1-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="0a9f1-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0a9f1-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="0a9f1-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a9f1-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="0a9f1-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0a9f1-169">New-AzAksCluster</span></span>

- <span data-ttu-id="0a9f1-170">Der Parameter `NodeOsType` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden. Er lautet immer `Linux`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="0a9f1-171">Der Alias `ClientIdAndSecret` für den Parameter `ServicePrincipalIdAndSecret` wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="0a9f1-172">Der Standardwert von `NodeVmSetType` wurde von `AvailabilitySet` in `VirtualMachineScaleSets` geändert.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="0a9f1-173">Der Standardwert von `NetworkPlugin` wurde von `none` in `azure` geändert.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-174">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-175">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="0a9f1-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0a9f1-176">Set-AzAksCluster</span></span>

<span data-ttu-id="0a9f1-177">Der Alias `ClientIdAndSecret` für den Parameter `ServicePrincipalIdAndSecret` wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-178">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-179">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="0a9f1-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a9f1-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="0a9f1-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a9f1-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="0a9f1-182">Der Parameter `StorageAccountName` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-183">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="0a9f1-184">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-184">After</span></span>

<span data-ttu-id="0a9f1-185">`Classic` wurde als veraltet eingestuft, und der Parameter `StorageAccountName` wurde entfernt, da er nur mit der klassischen Containerregistrierung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="0a9f1-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="0a9f1-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="0a9f1-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0a9f1-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="0a9f1-188">Der Switch-Parameter `IncludeSlot` wurde aus allen Parametersätzen von „`Get-AzFunctionApp`“ entfernt (bis auf einen).</span><span class="sxs-lookup"><span data-stu-id="0a9f1-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="0a9f1-189">Das Cmdlet unterstützt jetzt das Abrufen von Bereitstellungsslots in den Ergebnissen, wenn `-IncludeSlot` angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="0a9f1-190">Diese Funktionalität war in der vorherigen Cmdlet-Version beschädigt.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="0a9f1-191">Der Fehler ist jetzt aber behoben.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="0a9f1-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0a9f1-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="0a9f1-193">`-DisableApplicationInsights` wurde in `New-AzFunctionApp` korrigiert, damit bei Angabe dieser Option kein Application Insights-Projekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="0a9f1-194">Die Unterstützung für die Erstellung von PowerShell 6.2-Funktions-Apps wurde entfernt, da für PowerShell 6.2 der EOL-Zeitpunkt erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="0a9f1-195">Für Kunden wird derzeit empfohlen, stattdessen PowerShell 7.0-Funktions-Apps zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="0a9f1-196">Es wurde festgelegt, dass in Functions-Version 3 von Windows für PowerShell-Funktions-Apps anstelle der Runtime-Standardversion 6.2 die Version 7.0 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="0a9f1-197">Es wurde festgelegt, dass in Functions-Version 3 von Windows/Linux für Node-Funktions-Apps anstelle der Runtime-Standardversion 10 die Version 12 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="0a9f1-198">Benutzer können aber weiterhin Node 10-Funktions-Apps erstellen, indem sie `-Runtime Node` und `-RuntimeVersion 10` angeben.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="0a9f1-199">Es wurde festgelegt, dass in Functions-Version 3 von Linux für Python-Funktions-Apps anstelle der Runtime-Standardversion 3.7 die Version 3.8 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="0a9f1-200">Benutzer können aber weiterhin Python 3.7-Funktions-Apps erstellen, indem sie `-Runtime Python` und `-RuntimeVersion 3.7` angeben.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-201">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="0a9f1-202">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="0a9f1-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a9f1-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="0a9f1-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a9f1-204">New-AzKeyVault</span></span>

<span data-ttu-id="0a9f1-205">Der Parameter `DisableSoftDelete` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-206">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="0a9f1-207">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-207">After</span></span>

<span data-ttu-id="0a9f1-208">Die Möglichkeit zum Aktualisieren der Einstellung für das vorläufige Löschen wurde in Az.KeyVault 3.0.0 als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="0a9f1-209">Weitere Informationen: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="0a9f1-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="0a9f1-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a9f1-210">Update-AzKeyVault</span></span>

<span data-ttu-id="0a9f1-211">Die Parameter `EnableSoftDelete` und `SoftDeleteRetentionInDays` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-212">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="0a9f1-213">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-213">After</span></span>

<span data-ttu-id="0a9f1-214">Die Möglichkeit zum Aktualisieren der Einstellung für das vorläufige Löschen wurde in Az.KeyVault 3.0.0 als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="0a9f1-215">Weitere Informationen: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="0a9f1-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="0a9f1-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0a9f1-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="0a9f1-217">Die `SecretValueText`-Eigenschaft vom Typ `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="0a9f1-218">Wenden Sie entweder `-AsPlainText` auf den Aufruf an, um das Nur-Text-Geheimnis zu erhalten, oder verwenden Sie `$secret.SecretValue` vom Typ `SecureString` im Skript.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-218">Either apply a `-AsPlainText` to the call to get the plain text secret, or use `$secret.SecretValue` of type `SecureString` in your script.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-219">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="0a9f1-220">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-220">After</span></span>

```powershell
$secretInPlainText = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret -AsPlainText
```

## <a name="azmanagedservices"></a><span data-ttu-id="0a9f1-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0a9f1-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="0a9f1-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0a9f1-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="0a9f1-223">Der Parameter `ResourceId` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-224">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-225">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="0a9f1-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="0a9f1-227">Die Parameter `RegistrationDefinitionName` und `RegistrationDefinitionResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-228">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-229">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="0a9f1-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="0a9f1-231">Die Parameter `Id` und `ResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-232">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-233">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="0a9f1-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0a9f1-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="0a9f1-235">Die Parameter `Id` und `ResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-236">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-237">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="0a9f1-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="0a9f1-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="0a9f1-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0a9f1-240">Der Parameter `ApiVersion` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-241">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-242">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="0a9f1-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="0a9f1-244">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="0a9f1-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-245">Get-AzDeployment</span></span>

<span data-ttu-id="0a9f1-246">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="0a9f1-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="0a9f1-248">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="0a9f1-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="0a9f1-250">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="0a9f1-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="0a9f1-252">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="0a9f1-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="0a9f1-254">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="0a9f1-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0a9f1-256">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="0a9f1-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-257">New-AzDeployment</span></span>

<span data-ttu-id="0a9f1-258">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="0a9f1-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="0a9f1-260">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="0a9f1-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0a9f1-262">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="0a9f1-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-263">Remove-AzDeployment</span></span>

<span data-ttu-id="0a9f1-264">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="0a9f1-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="0a9f1-266">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="0a9f1-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="0a9f1-268">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="0a9f1-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="0a9f1-270">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="0a9f1-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="0a9f1-272">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="0a9f1-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0a9f1-274">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="0a9f1-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-275">Stop-AzDeployment</span></span>

<span data-ttu-id="0a9f1-276">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="0a9f1-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="0a9f1-278">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="0a9f1-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0a9f1-280">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="0a9f1-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-281">Test-AzDeployment</span></span>

<span data-ttu-id="0a9f1-282">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="0a9f1-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="0a9f1-284">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="0a9f1-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0a9f1-286">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="0a9f1-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a9f1-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="0a9f1-288">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="0a9f1-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="0a9f1-290">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="0a9f1-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0a9f1-292">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="0a9f1-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0a9f1-294">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="0a9f1-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0a9f1-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="0a9f1-296">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="0a9f1-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0a9f1-298">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="0a9f1-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a9f1-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0a9f1-300">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="0a9f1-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="0a9f1-302">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="0a9f1-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0a9f1-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="0a9f1-304">Identisch mit `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="0a9f1-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a9f1-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="0a9f1-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0a9f1-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="0a9f1-307">Der Parameter `IsAzureADOnlyAuthentication` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-308">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="0a9f1-309">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="0a9f1-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="0a9f1-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="0a9f1-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a9f1-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="0a9f1-312">Die Parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` und `RestorePoint` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-313">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="0a9f1-314">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="0a9f1-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a9f1-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="0a9f1-316">Die Parameter `Suspend` und `Resume` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="0a9f1-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a9f1-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="0a9f1-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0a9f1-319">Der Parameter `PrivateLinkResourceType` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-320">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="0a9f1-321">Danach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="0a9f1-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0a9f1-323">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="0a9f1-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0a9f1-325">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="0a9f1-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0a9f1-327">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="0a9f1-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a9f1-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0a9f1-329">Identisch mit `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="0a9f1-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0a9f1-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="0a9f1-331">Die Parameter `FilterType` und `FilterItem` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="0a9f1-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0a9f1-332">Vorher</span><span class="sxs-lookup"><span data-stu-id="0a9f1-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="0a9f1-333">Nach</span><span class="sxs-lookup"><span data-stu-id="0a9f1-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
