---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005547"
---
# <span data-ttu-id="efc15-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="efc15-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="efc15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="efc15-102">SYNOPSIS</span></span>
<span data-ttu-id="efc15-103">Erstellen Sie eine Virtual Machine-Erweiterungs Abbildung mit Publisher, Version.</span><span class="sxs-lookup"><span data-stu-id="efc15-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="efc15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="efc15-104">SYNTAX</span></span>

### <span data-ttu-id="efc15-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="efc15-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="efc15-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="efc15-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="efc15-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="efc15-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efc15-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="efc15-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efc15-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efc15-109">DESCRIPTION</span></span>
<span data-ttu-id="efc15-110">Erstellen Sie eine Virtual Machine-Erweiterungs Abbildung mit Publisher, Version.</span><span class="sxs-lookup"><span data-stu-id="efc15-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="efc15-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efc15-111">EXAMPLES</span></span>

### <span data-ttu-id="efc15-112">Beispiel 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="efc15-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="efc15-113">Verwenden Sie einen öffentlich zugänglichen Link, um den Speicherort der Erweiterung oder den URI zu einem Azure-BLOB mithilfe des SasUri bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="efc15-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="efc15-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="efc15-114">PARAMETERS</span></span>

### <span data-ttu-id="efc15-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="efc15-115">-ComputeRole</span></span>
<span data-ttu-id="efc15-116">Compute-Rolle</span><span class="sxs-lookup"><span data-stu-id="efc15-116">Compute role</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc15-117">-DefaultProfile</span></span>
<span data-ttu-id="efc15-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="efc15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc15-119">-Extension</span><span class="sxs-lookup"><span data-stu-id="efc15-119">-Extension</span></span>
<span data-ttu-id="efc15-120">Parameter, die zum Erstellen eines neuen Virtual Machine Extension-Bilds verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efc15-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="efc15-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Erweiterungseigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="efc15-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="efc15-122">-InputObject</span></span>
<span data-ttu-id="efc15-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="efc15-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="efc15-124">-IsSystemExtension</span></span>
<span data-ttu-id="efc15-125">Gibt an, ob die Erweiterung für das System gilt.</span><span class="sxs-lookup"><span data-stu-id="efc15-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="efc15-126">-Location</span></span>
<span data-ttu-id="efc15-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="efc15-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="efc15-128">-PropertiesPublisher</span></span>
<span data-ttu-id="efc15-129">Der Herausgeber der VM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="efc15-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="efc15-130">-ProvisioningState</span></span>
<span data-ttu-id="efc15-131">Bereitstellungsstatus der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="efc15-131">Provisioning state of extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="efc15-132">-Publisher</span></span>
<span data-ttu-id="efc15-133">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="efc15-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="efc15-134">-SourceBlob</span></span>
<span data-ttu-id="efc15-135">URI zu Azure oder AzureStack BLOB.</span><span class="sxs-lookup"><span data-stu-id="efc15-135">URI to Azure or AzureStack blob.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="efc15-136">-SubscriptionId</span></span>
<span data-ttu-id="efc15-137">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="efc15-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="efc15-138">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="efc15-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="efc15-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="efc15-140">True, wenn mehrere Erweiterungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="efc15-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-141">-Typ</span><span class="sxs-lookup"><span data-stu-id="efc15-141">-Type</span></span>
<span data-ttu-id="efc15-142">Der Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="efc15-142">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-143">-Version</span><span class="sxs-lookup"><span data-stu-id="efc15-143">-Version</span></span>
<span data-ttu-id="efc15-144">Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="efc15-144">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="efc15-145">-VmOsType</span></span>
<span data-ttu-id="efc15-146">Der für die Bereitstellung des Erweiterungs Handlers erforderliche Betriebssystemtyp des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="efc15-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="efc15-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="efc15-148">Wert, der angibt, ob die Erweiterung für die Unterstützung von Skalierungs Sätzen für virtuelle Maschinen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="efc15-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="efc15-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="efc15-149">-Confirm</span></span>
<span data-ttu-id="efc15-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="efc15-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc15-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc15-151">-WhatIf</span></span>
<span data-ttu-id="efc15-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efc15-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc15-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efc15-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc15-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc15-154">CommonParameters</span></span>
<span data-ttu-id="efc15-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc15-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc15-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efc15-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc15-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="efc15-157">INPUTS</span></span>

### <span data-ttu-id="efc15-158">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="efc15-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="efc15-159">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="efc15-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="efc15-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="efc15-160">OUTPUTS</span></span>

### <span data-ttu-id="efc15-161">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="efc15-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="efc15-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="efc15-162">NOTES</span></span>

<span data-ttu-id="efc15-163">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="efc15-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efc15-164">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="efc15-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="efc15-165">Erweiterung <IVMExtensionParameters> : Parameter, die zum Erstellen eines neuen Virtual Machine Extension-Bilds verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efc15-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="efc15-166">`[ComputeRole <String>]`: Compute-Rolle</span><span class="sxs-lookup"><span data-stu-id="efc15-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="efc15-167">`[IsSystemExtension <Boolean?>]`: Gibt an, ob die Erweiterung für das System gilt.</span><span class="sxs-lookup"><span data-stu-id="efc15-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="efc15-168">`[ProvisioningState <ProvisioningState?>]`: Bereitstellungsstatus der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="efc15-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="efc15-169">`[Publisher <String>]`: Der Herausgeber der VM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="efc15-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="efc15-170">`[SourceBlobUri <String>]`: URI zu Azure oder AzureStack BLOB.</span><span class="sxs-lookup"><span data-stu-id="efc15-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="efc15-171">`[SupportMultipleExtension <Boolean?>]`: True, wenn mehrere Erweiterungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="efc15-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="efc15-172">`[VMScaleSetEnabled <Boolean?>]`: Wert, der angibt, ob die Erweiterung für die Unterstützung des Skalierungs Sets für virtuelle Maschinen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="efc15-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="efc15-173">`[VmosType <OSType?>]`: Ziel des Betriebssystemtyps des virtuellen Computers, der für die Bereitstellung des Erweiterungs Handlers erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="efc15-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="efc15-174">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="efc15-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="efc15-175">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="efc15-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="efc15-176">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="efc15-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efc15-177">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="efc15-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="efc15-178">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="efc15-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="efc15-179">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="efc15-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="efc15-180">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="efc15-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="efc15-181">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="efc15-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="efc15-182">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="efc15-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="efc15-183">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="efc15-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="efc15-184">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="efc15-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="efc15-185">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="efc15-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="efc15-186">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="efc15-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="efc15-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="efc15-187">RELATED LINKS</span></span>

