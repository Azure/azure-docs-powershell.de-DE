---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842431"
---
# <span data-ttu-id="d9a78-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9a78-101">Update-AzVM</span></span>

## <span data-ttu-id="d9a78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9a78-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a78-103">Aktualisiert den Zustand eines Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="d9a78-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="d9a78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9a78-104">SYNTAX</span></span>

### <span data-ttu-id="d9a78-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9a78-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9a78-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9a78-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9a78-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9a78-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a78-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d9a78-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a78-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9a78-109">DESCRIPTION</span></span>
<span data-ttu-id="d9a78-110">Das Cmdlet **Update-AzVM** aktualisiert den Zustand eines Azure Virtual Machine auf den Zustand eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="d9a78-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="d9a78-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9a78-111">EXAMPLES</span></span>

### <span data-ttu-id="d9a78-112">Beispiel 1: Aktualisieren eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="d9a78-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="d9a78-113">Mit diesem Befehl wird der virtuelle Computer $VirtualMachine in ResourceGroup11 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d9a78-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="d9a78-114">Der Befehl aktualisiert ihn mit dem in der $VirtualMachine Variablen gespeicherten virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="d9a78-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d9a78-115">Verwenden Sie das Cmdlet **Get-AzVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9a78-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="d9a78-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9a78-116">PARAMETERS</span></span>

### <span data-ttu-id="d9a78-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9a78-117">-AsJob</span></span>
<span data-ttu-id="d9a78-118">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="d9a78-118">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d9a78-119">-AssignIdentity</span></span>
<span data-ttu-id="d9a78-120">Geben Sie die dem virtuellen Computer zugewiesene Identität für das System an.</span><span class="sxs-lookup"><span data-stu-id="d9a78-120">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a78-121">-DefaultProfile</span></span>
<span data-ttu-id="d9a78-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9a78-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-123">-ID</span><span class="sxs-lookup"><span data-stu-id="d9a78-123">-Id</span></span>
<span data-ttu-id="d9a78-124">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d9a78-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-125">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="d9a78-125">-IdentityId</span></span>
<span data-ttu-id="d9a78-126">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9a78-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="d9a78-127">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="d9a78-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d9a78-128">-IdentityType</span></span>
<span data-ttu-id="d9a78-129">Der Typ der für den virtuellen Computer verwendeten Identität.</span><span class="sxs-lookup"><span data-stu-id="d9a78-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="d9a78-130">Derzeit ist der einzige unterstützte Typ "SystemAssigned", der implizit eine Identität erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9a78-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d9a78-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="d9a78-132">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9a78-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a78-133">-ResourceGroupName</span></span>
<span data-ttu-id="d9a78-134">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d9a78-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9a78-135">-Tag</span></span>
<span data-ttu-id="d9a78-136">Gibt an, dass die Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="d9a78-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="d9a78-137">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="d9a78-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="d9a78-138">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d9a78-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-139">-VM</span><span class="sxs-lookup"><span data-stu-id="d9a78-139">-VM</span></span>
<span data-ttu-id="d9a78-140">Gibt ein lokales Objekt eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d9a78-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="d9a78-141">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9a78-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="d9a78-142">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d9a78-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9a78-143">-Confirm</span></span>
<span data-ttu-id="d9a78-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9a78-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a78-145">-WhatIf</span></span>
<span data-ttu-id="d9a78-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9a78-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d9a78-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9a78-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a78-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a78-148">CommonParameters</span></span>
<span data-ttu-id="d9a78-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a78-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a78-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a78-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a78-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9a78-151">INPUTS</span></span>

### <span data-ttu-id="d9a78-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d9a78-152">PSVirtualMachine</span></span>
<span data-ttu-id="d9a78-153">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9a78-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d9a78-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9a78-154">OUTPUTS</span></span>

### <span data-ttu-id="d9a78-155">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d9a78-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d9a78-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9a78-156">NOTES</span></span>

## <span data-ttu-id="d9a78-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9a78-157">RELATED LINKS</span></span>

[<span data-ttu-id="d9a78-158">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9a78-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d9a78-159">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="d9a78-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d9a78-160">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9a78-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d9a78-161">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9a78-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d9a78-162">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9a78-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d9a78-163">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9a78-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d9a78-164">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d9a78-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


