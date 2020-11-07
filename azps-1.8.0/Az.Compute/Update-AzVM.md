---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820480"
---
# <span data-ttu-id="dc6ea-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-101">Update-AzVM</span></span>

## <span data-ttu-id="dc6ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6ea-103">Aktualisiert den Zustand eines Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="dc6ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc6ea-104">SYNTAX</span></span>

### <span data-ttu-id="dc6ea-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc6ea-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc6ea-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc6ea-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc6ea-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc6ea-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc6ea-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dc6ea-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6ea-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc6ea-109">DESCRIPTION</span></span>
<span data-ttu-id="dc6ea-110">Das Cmdlet **Update-AzVM** aktualisiert den Zustand eines Azure Virtual Machine auf den Zustand eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="dc6ea-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc6ea-111">EXAMPLES</span></span>

### <span data-ttu-id="dc6ea-112">Beispiel 1: Aktualisieren eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="dc6ea-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="dc6ea-113">Mit diesem Befehl wird der virtuelle Computer $VirtualMachine in ResourceGroup11 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="dc6ea-114">Der Befehl aktualisiert ihn mit dem in der $VirtualMachine Variablen gespeicherten virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dc6ea-115">Verwenden Sie das Cmdlet **Get-AzVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="dc6ea-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc6ea-116">PARAMETERS</span></span>

### <span data-ttu-id="dc6ea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc6ea-117">-AsJob</span></span>
<span data-ttu-id="dc6ea-118">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dc6ea-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dc6ea-119">-AssignIdentity</span></span>
<span data-ttu-id="dc6ea-120">Geben Sie die vom System zugewiesene Identität für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="dc6ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6ea-121">-DefaultProfile</span></span>
<span data-ttu-id="dc6ea-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc6ea-123">-ID</span><span class="sxs-lookup"><span data-stu-id="dc6ea-123">-Id</span></span>
<span data-ttu-id="dc6ea-124">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="dc6ea-125">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="dc6ea-125">-IdentityId</span></span>
<span data-ttu-id="dc6ea-126">Gibt die Liste der Benutzeridentitäten an, die dem virtuellen Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="dc6ea-127">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="dc6ea-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="dc6ea-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="dc6ea-128">-IdentityType</span></span>
<span data-ttu-id="dc6ea-129">Der Typ der für den virtuellen Computer verwendeten Identität.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="dc6ea-130">Gültige Werte sind SystemAssigned, UserAssigned, SystemAssignedUserAssigned und None.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="dc6ea-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dc6ea-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="dc6ea-132">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="dc6ea-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6ea-133">-ResourceGroupName</span></span>
<span data-ttu-id="dc6ea-134">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dc6ea-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc6ea-135">-Tag</span></span>
<span data-ttu-id="dc6ea-136">Gibt an, dass die Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="dc6ea-137">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="dc6ea-138">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="dc6ea-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="dc6ea-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="dc6ea-140">Das Flag, mit dem eine Funktion für einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem virtuellen Computer aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="dc6ea-141">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="dc6ea-142">-VM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-142">-VM</span></span>
<span data-ttu-id="dc6ea-143">Gibt ein lokales Objekt eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="dc6ea-144">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="dc6ea-145">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="dc6ea-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc6ea-146">-Confirm</span></span>
<span data-ttu-id="dc6ea-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc6ea-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc6ea-148">-WhatIf</span></span>
<span data-ttu-id="dc6ea-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc6ea-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc6ea-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6ea-151">CommonParameters</span></span>
<span data-ttu-id="dc6ea-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6ea-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6ea-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6ea-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6ea-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc6ea-154">INPUTS</span></span>

### <span data-ttu-id="dc6ea-155">System. String</span><span class="sxs-lookup"><span data-stu-id="dc6ea-155">System.String</span></span>

### <span data-ttu-id="dc6ea-156">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dc6ea-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="dc6ea-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc6ea-157">System.Boolean</span></span>

## <span data-ttu-id="dc6ea-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc6ea-158">OUTPUTS</span></span>

### <span data-ttu-id="dc6ea-159">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dc6ea-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dc6ea-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc6ea-160">NOTES</span></span>

## <span data-ttu-id="dc6ea-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc6ea-161">RELATED LINKS</span></span>

[<span data-ttu-id="dc6ea-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="dc6ea-163">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="dc6ea-164">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="dc6ea-165">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="dc6ea-166">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="dc6ea-167">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc6ea-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="dc6ea-168">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dc6ea-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


