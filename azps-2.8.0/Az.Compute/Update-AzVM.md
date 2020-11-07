---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 339d63fe02c8286dc5867428269dc2e2afe342d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651855"
---
# <span data-ttu-id="b3d5c-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-101">Update-AzVM</span></span>

## <span data-ttu-id="b3d5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d5c-103">Aktualisiert den Zustand eines Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="b3d5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d5c-104">SYNTAX</span></span>

### <span data-ttu-id="b3d5c-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3d5c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d5c-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3d5c-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d5c-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3d5c-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d5c-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b3d5c-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d5c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3d5c-109">DESCRIPTION</span></span>
<span data-ttu-id="b3d5c-110">Das Cmdlet **Update-AzVM** aktualisiert den Zustand eines Azure Virtual Machine auf den Zustand eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="b3d5c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3d5c-111">EXAMPLES</span></span>

### <span data-ttu-id="b3d5c-112">Beispiel 1: Aktualisieren eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="b3d5c-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b3d5c-113">Mit diesem Befehl wird der virtuelle Computer $VirtualMachine in ResourceGroup11 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="b3d5c-114">Der Befehl aktualisiert ihn mit dem in der $VirtualMachine Variablen gespeicherten virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b3d5c-115">Verwenden Sie das Cmdlet **Get-AzVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="b3d5c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3d5c-116">PARAMETERS</span></span>

### <span data-ttu-id="b3d5c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3d5c-117">-AsJob</span></span>
<span data-ttu-id="b3d5c-118">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3d5c-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b3d5c-119">-AssignIdentity</span></span>
<span data-ttu-id="b3d5c-120">Geben Sie die vom System zugewiesene Identität für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d5c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d5c-121">-DefaultProfile</span></span>
<span data-ttu-id="b3d5c-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d5c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="b3d5c-123">-Id</span></span>
<span data-ttu-id="b3d5c-124">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="b3d5c-125">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="b3d5c-125">-IdentityId</span></span>
<span data-ttu-id="b3d5c-126">Gibt die Liste der Benutzeridentitäten an, die dem virtuellen Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="b3d5c-127">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="b3d5c-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="b3d5c-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b3d5c-128">-IdentityType</span></span>
<span data-ttu-id="b3d5c-129">Der Typ der für den virtuellen Computer verwendeten Identität.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="b3d5c-130">Gültige Werte sind SystemAssigned, UserAssigned, SystemAssignedUserAssigned und None.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="b3d5c-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="b3d5c-131">-MaxPrice</span></span>
<span data-ttu-id="b3d5c-132">Gibt den Höchstpreis an, den Sie für eine VM-VMSS mit niedriger Priorität bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="b3d5c-133">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-133">This price is in US Dollars.</span></span> <span data-ttu-id="b3d5c-134">Dieser Preis wird mit dem aktuellen Preis für niedrige Priorität für die VM-Größe verglichen.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="b3d5c-135">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM-VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxprice größer als der aktuelle Preis für niedrige Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="b3d5c-136">Die maxprice wird auch zum Entfernen einer VM-VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis für niedrige Priorität über die maxprice nach der Erstellung von VM/VMSS hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="b3d5c-137">Mögliche Werte sind: beliebiger Dezimalwert größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b3d5c-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="b3d5c-138">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-138">Example: 0.01538.</span></span>  <span data-ttu-id="b3d5c-139">-1 gibt an, dass die VM-VMSS mit niedriger Priorität aus Preisgründen nicht vertrieben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="b3d5c-140">Außerdem ist der standardmäßige Höchstpreis-1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-140">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="b3d5c-141">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b3d5c-141">-NoWait</span></span>
<span data-ttu-id="b3d5c-142">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b3d5c-143">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b3d5c-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b3d5c-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="b3d5c-145">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="b3d5c-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d5c-146">-ResourceGroupName</span></span>
<span data-ttu-id="b3d5c-147">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-147">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d5c-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3d5c-148">-Tag</span></span>
<span data-ttu-id="b3d5c-149">Gibt an, dass die Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-149">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="b3d5c-150">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-150">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="b3d5c-151">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-151">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="b3d5c-152">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="b3d5c-152">-UltraSSDEnabled</span></span>
<span data-ttu-id="b3d5c-153">Das Flag, mit dem eine Funktion für einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem virtuellen Computer aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-153">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="b3d5c-154">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-154">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="b3d5c-155">-VM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-155">-VM</span></span>
<span data-ttu-id="b3d5c-156">Gibt ein lokales Objekt eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-156">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="b3d5c-157">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-157">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b3d5c-158">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-158">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="b3d5c-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3d5c-159">-Confirm</span></span>
<span data-ttu-id="b3d5c-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d5c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d5c-161">-WhatIf</span></span>
<span data-ttu-id="b3d5c-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d5c-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d5c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d5c-164">CommonParameters</span></span>
<span data-ttu-id="b3d5c-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d5c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d5c-166">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3d5c-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d5c-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3d5c-167">INPUTS</span></span>

### <span data-ttu-id="b3d5c-168">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d5c-168">System.String</span></span>

### <span data-ttu-id="b3d5c-169">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b3d5c-169">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b3d5c-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3d5c-170">System.Boolean</span></span>

## <span data-ttu-id="b3d5c-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3d5c-171">OUTPUTS</span></span>

### <span data-ttu-id="b3d5c-172">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b3d5c-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b3d5c-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3d5c-173">NOTES</span></span>

## <span data-ttu-id="b3d5c-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3d5c-174">RELATED LINKS</span></span>

[<span data-ttu-id="b3d5c-175">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-175">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b3d5c-176">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-176">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b3d5c-177">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-177">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b3d5c-178">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-178">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b3d5c-179">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-179">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b3d5c-180">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3d5c-180">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b3d5c-181">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b3d5c-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


