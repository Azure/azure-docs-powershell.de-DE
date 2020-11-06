---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503826"
---
# <span data-ttu-id="9fedc-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="9fedc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fedc-102">SYNOPSIS</span></span>
<span data-ttu-id="9fedc-103">Beendet die VMSS oder einen Satz virtueller Computer innerhalb des VMSS.</span><span class="sxs-lookup"><span data-stu-id="9fedc-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fedc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fedc-104">SYNTAX</span></span>

### <span data-ttu-id="9fedc-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fedc-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fedc-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9fedc-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fedc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fedc-107">DESCRIPTION</span></span>
<span data-ttu-id="9fedc-108">Das Cmdlet **Stop-AzureRmVmss** beendet alle virtuellen Maschinen innerhalb des Scale-Sets (Virtual Machine Scale) (VMSS) oder einer Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="9fedc-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="9fedc-109">Sie können den *InstanceId* -Parameter verwenden, um einen Satz virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9fedc-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="9fedc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fedc-110">EXAMPLES</span></span>

### <span data-ttu-id="9fedc-111">Beispiel 1: Beenden aller virtuellen Computer innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="9fedc-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="9fedc-112">Dieser Befehl beendet alle virtuellen Computer, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="9fedc-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="9fedc-113">Beispiel 2: Beenden einer bestimmten Gruppe von virtuellen Computern innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="9fedc-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="9fedc-114">Mit diesem Befehl wird eine bestimmte Gruppe von virtuellen Computern beendet, die durch das Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="9fedc-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="9fedc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fedc-115">PARAMETERS</span></span>

### <span data-ttu-id="9fedc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9fedc-116">-Force</span></span>
<span data-ttu-id="9fedc-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9fedc-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fedc-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9fedc-118">-InstanceId</span></span>
<span data-ttu-id="9fedc-119">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen des virtuellen Computers an, die von diesem Cmdlet angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="9fedc-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="9fedc-120">Beispiel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="9fedc-120">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fedc-121">-ResourceGroupName</span></span>
<span data-ttu-id="9fedc-122">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="9fedc-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedc-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="9fedc-123">-StayProvisioned</span></span>
<span data-ttu-id="9fedc-124">Wenn angegeben, wird der virtuelle Computer in den Zustand beendet gesetzt.</span><span class="sxs-lookup"><span data-stu-id="9fedc-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="9fedc-125">Wenn keine Angabe erfolgt, gibt der virtuelle Computer den Status "Stopped-dereserviert" ein.</span><span class="sxs-lookup"><span data-stu-id="9fedc-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="9fedc-126">Der Benutzer wird weiterhin für VMS im Zustand "beendet", jedoch nicht für VMS im Status "nicht mehr zugewiesen" berechnet.</span><span class="sxs-lookup"><span data-stu-id="9fedc-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fedc-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9fedc-127">-VMScaleSetName</span></span>
<span data-ttu-id="9fedc-128">Gibt den Namen der VMSS an, für die dieses Cmdlet die virtuellen Computer beendet.</span><span class="sxs-lookup"><span data-stu-id="9fedc-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedc-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9fedc-129">-Confirm</span></span>
<span data-ttu-id="9fedc-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fedc-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fedc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fedc-131">-WhatIf</span></span>
<span data-ttu-id="9fedc-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fedc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fedc-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fedc-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fedc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fedc-134">CommonParameters</span></span>
<span data-ttu-id="9fedc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fedc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fedc-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fedc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fedc-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fedc-137">INPUTS</span></span>

### <span data-ttu-id="9fedc-138">Keine</span><span class="sxs-lookup"><span data-stu-id="9fedc-138">None</span></span>
<span data-ttu-id="9fedc-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9fedc-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fedc-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fedc-140">OUTPUTS</span></span>

## <span data-ttu-id="9fedc-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fedc-141">NOTES</span></span>

## <span data-ttu-id="9fedc-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fedc-142">RELATED LINKS</span></span>

[<span data-ttu-id="9fedc-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="9fedc-144">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="9fedc-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="9fedc-146">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="9fedc-147">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="9fedc-148">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="9fedc-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fedc-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


