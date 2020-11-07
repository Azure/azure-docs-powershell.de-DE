---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 11b387e4022bce98e1275bb2af09bc97beff0041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663331"
---
# <span data-ttu-id="d551b-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="d551b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d551b-102">SYNOPSIS</span></span>
<span data-ttu-id="d551b-103">Beendet die VMSS oder einen Satz virtueller Computer innerhalb des VMSS.</span><span class="sxs-lookup"><span data-stu-id="d551b-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d551b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d551b-104">SYNTAX</span></span>

### <span data-ttu-id="d551b-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="d551b-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d551b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d551b-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d551b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d551b-107">DESCRIPTION</span></span>
<span data-ttu-id="d551b-108">Das Cmdlet **Stop-AzureRmVmss** beendet alle virtuellen Maschinen innerhalb des Scale-Sets (Virtual Machine Scale) (VMSS) oder einer Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="d551b-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="d551b-109">Sie können den *InstanceId* -Parameter verwenden, um einen Satz virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d551b-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="d551b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d551b-110">EXAMPLES</span></span>

### <span data-ttu-id="d551b-111">Beispiel 1: Beenden aller virtuellen Computer innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="d551b-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d551b-112">Dieser Befehl beendet alle virtuellen Computer, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="d551b-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="d551b-113">Beispiel 2: Beenden einer bestimmten Gruppe von virtuellen Computern innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="d551b-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="d551b-114">Mit diesem Befehl wird eine bestimmte Gruppe von virtuellen Computern beendet, die durch das Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="d551b-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d551b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d551b-115">PARAMETERS</span></span>

### <span data-ttu-id="d551b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d551b-116">-DefaultProfile</span></span>
<span data-ttu-id="d551b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d551b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d551b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d551b-118">-Force</span></span>
<span data-ttu-id="d551b-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d551b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d551b-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d551b-120">-InstanceId</span></span>
<span data-ttu-id="d551b-121">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen des virtuellen Computers an, die von diesem Cmdlet angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="d551b-121">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="d551b-122">Beispiel: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="d551b-122">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d551b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d551b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d551b-124">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="d551b-124">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d551b-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="d551b-125">-StayProvisioned</span></span>
<span data-ttu-id="d551b-126">Wenn angegeben, wird der virtuelle Computer in den Zustand beendet gesetzt.</span><span class="sxs-lookup"><span data-stu-id="d551b-126">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="d551b-127">Wenn keine Angabe erfolgt, gibt der virtuelle Computer den Status "Stopped-dereserviert" ein.</span><span class="sxs-lookup"><span data-stu-id="d551b-127">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="d551b-128">Der Benutzer wird weiterhin für VMS im Zustand "beendet", jedoch nicht für VMS im Status "nicht mehr zugewiesen" berechnet.</span><span class="sxs-lookup"><span data-stu-id="d551b-128">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d551b-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d551b-129">-VMScaleSetName</span></span>
<span data-ttu-id="d551b-130">Gibt den Namen der VMSS an, für die dieses Cmdlet die virtuellen Computer beendet.</span><span class="sxs-lookup"><span data-stu-id="d551b-130">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d551b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d551b-131">-Confirm</span></span>
<span data-ttu-id="d551b-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d551b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d551b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d551b-133">-WhatIf</span></span>
<span data-ttu-id="d551b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d551b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d551b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d551b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d551b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d551b-136">CommonParameters</span></span>
<span data-ttu-id="d551b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d551b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d551b-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d551b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d551b-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d551b-139">INPUTS</span></span>

## <span data-ttu-id="d551b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d551b-140">OUTPUTS</span></span>

## <span data-ttu-id="d551b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d551b-141">NOTES</span></span>

## <span data-ttu-id="d551b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d551b-142">RELATED LINKS</span></span>

[<span data-ttu-id="d551b-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="d551b-144">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d551b-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d551b-146">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="d551b-147">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="d551b-148">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="d551b-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d551b-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


