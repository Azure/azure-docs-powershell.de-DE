---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472910"
---
# <span data-ttu-id="7d1e2-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-101">Update-AzVM</span></span>

## <span data-ttu-id="7d1e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1e2-103">Aktualisiert den Zustand eines virtuellen Azure-Computers.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="7d1e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d1e2-104">SYNTAX</span></span>

### <span data-ttu-id="7d1e2-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d1e2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1e2-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1e2-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1e2-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7d1e2-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1e2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d1e2-108">DESCRIPTION</span></span>
<span data-ttu-id="7d1e2-109">Das **Update-AzVM-Cmdlet** aktualisiert den Zustand eines virtuellen Azure-Computers auf den Zustand eines Objekts des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="7d1e2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d1e2-110">EXAMPLES</span></span>

### <span data-ttu-id="7d1e2-111">Beispiel 1: Aktualisieren eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="7d1e2-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7d1e2-112">Mit diesem Befehl wird der virtuelle Computer ($VirtualMachine) in ResourceGroup11 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="7d1e2-113">Der Befehl aktualisiert ihn mit dem Objekt des virtuellen Computers, das in der Variablen $VirtualMachine ist.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7d1e2-114">Verwenden Sie das **Get-AzVM-Cmdlet,** um ein Objekt des virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="7d1e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d1e2-115">PARAMETERS</span></span>

### <span data-ttu-id="7d1e2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d1e2-116">-AsJob</span></span>
<span data-ttu-id="7d1e2-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1e2-118">-DefaultProfile</span></span>
<span data-ttu-id="7d1e2-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-120">-HostId</span></span>
<span data-ttu-id="7d1e2-121">Die ID des Hosts</span><span class="sxs-lookup"><span data-stu-id="7d1e2-121">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="7d1e2-122">-EncryptionAtHost</span></span>
<span data-ttu-id="7d1e2-123">Die "EncryptionAtHost"-Eigenschaft kann vom Benutzer in der Anforderung verwendet werden, um die Hostverschlüsselung für den Skalierungssatz des virtuellen Computers oder virtuellen Computers zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="7d1e2-124">Dadurch wird die Verschlüsselung für alle Datenträger aktiviert, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-125">-ID</span><span class="sxs-lookup"><span data-stu-id="7d1e2-125">-Id</span></span>
<span data-ttu-id="7d1e2-126">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-126">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-127">-IdentityId</span></span>
<span data-ttu-id="7d1e2-128">Gibt die Liste der Benutzeridentitäten an, die dem virtuellen Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="7d1e2-129">Die Benutzeridentitätsverweise werden ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' angegeben.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7d1e2-130">-IdentityType</span></span>
<span data-ttu-id="7d1e2-131">Der für den virtuellen Computer verwendete Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="7d1e2-132">Gültige Werte sind "SystemAssigned", "UserAssigned", "SystemAssignedUserAssigned" und "None".</span><span class="sxs-lookup"><span data-stu-id="7d1e2-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7d1e2-133">-MaxPrice</span></span>
<span data-ttu-id="7d1e2-134">Gibt den Maximalpreis an, den Sie für eine VM/VMSS mit niedriger Priorität bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="7d1e2-135">Dieser Preis wird in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-135">This price is in US Dollars.</span></span> <span data-ttu-id="7d1e2-136">Dieser Preis wird mit dem aktuellen Preis mit niedriger Priorität für die Größe der VM verglichen.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="7d1e2-137">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM/VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der "maxPrice" größer als der aktuelle Preis mit niedriger Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="7d1e2-138">Der "maxPrice" wird auch zum Entfernung einer VM/VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis mit niedriger Priorität nach der Erstellung von VM/VMSS über den maxPrice hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="7d1e2-139">Mögliche Werte sind: beliebige Dezimalwerte größer als Null.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="7d1e2-140">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-140">Example: 0.01538.</span></span>  <span data-ttu-id="7d1e2-141">-1 gibt an, dass die VM/VMSS mit niedriger Priorität aus Preisgründen nicht entfernt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="7d1e2-142">Außerdem beträgt der standardmäßige Maximalpreis -1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-142">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7d1e2-143">-NoWait</span></span>
<span data-ttu-id="7d1e2-144">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7d1e2-145">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7d1e2-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="7d1e2-147">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7d1e2-149">Die Ressourcen-ID der Näherungsplatzierungsgruppe, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="7d1e2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1e2-150">-ResourceGroupName</span></span>
<span data-ttu-id="7d1e2-151">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d1e2-152">-Tag</span></span>
<span data-ttu-id="7d1e2-153">Gibt die Ressourcen und Ressourcengruppen an, die mit einem Satz von Name-Wert-Paaren markiert werden können.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="7d1e2-154">Das Hinzufügen von Tags zu Ressourcen ermöglicht es Ihnen, Ressourcen in Ressourcengruppen zu gruppieren und eigene Ansichten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="7d1e2-155">Jede Ressource oder Ressourcengruppe kann maximal 15 Tags enthalten.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="7d1e2-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="7d1e2-157">Das Kennzeichen, mit dem eine Funktion aktiviert oder deaktiviert wird, um eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf der VM zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="7d1e2-158">Verwaltete Datenträger mit Speicherkontotyp UltraSSD_LRS einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-159">-VM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-159">-VM</span></span>
<span data-ttu-id="7d1e2-160">Gibt ein Objekt für einen lokalen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="7d1e2-161">Verwenden Sie zum Abrufen eines Objekts für einen virtuellen Computer das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="7d1e2-162">Dieses Objekt des virtuellen Computers enthält den aktualisierten Zustand für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d1e2-163">-Confirm</span></span>
<span data-ttu-id="7d1e2-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7d1e2-165">-WhatIf</span></span>
<span data-ttu-id="7d1e2-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1e2-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="7d1e2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1e2-168">CommonParameters</span></span>
<span data-ttu-id="7d1e2-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1e2-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d1e2-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1e2-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d1e2-171">INPUTS</span></span>

### <span data-ttu-id="7d1e2-172">System.String</span><span class="sxs-lookup"><span data-stu-id="7d1e2-172">System.String</span></span>

### <span data-ttu-id="7d1e2-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7d1e2-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7d1e2-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d1e2-174">System.Boolean</span></span>

## <span data-ttu-id="7d1e2-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d1e2-175">OUTPUTS</span></span>

### <span data-ttu-id="7d1e2-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7d1e2-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7d1e2-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d1e2-177">NOTES</span></span>

## <span data-ttu-id="7d1e2-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d1e2-178">RELATED LINKS</span></span>

[<span data-ttu-id="7d1e2-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7d1e2-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7d1e2-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7d1e2-182">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="7d1e2-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7d1e2-184">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d1e2-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="7d1e2-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7d1e2-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


