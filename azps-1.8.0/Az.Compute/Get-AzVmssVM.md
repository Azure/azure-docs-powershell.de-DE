---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: d7eb7d8dd6fd8bb9f9071a00aef6a90057b81d02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820707"
---
# <span data-ttu-id="b6a06-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="b6a06-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="b6a06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6a06-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a06-103">Ruft die Eigenschaften eines virtuellen VMSS-Computers ab.</span><span class="sxs-lookup"><span data-stu-id="b6a06-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="b6a06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6a06-104">SYNTAX</span></span>

### <span data-ttu-id="b6a06-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6a06-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6a06-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b6a06-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a06-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6a06-107">DESCRIPTION</span></span>
<span data-ttu-id="b6a06-108">Das Cmdlet " **Get-AzVmssVM** " Ruft die Modellansicht und die Instanzen Ansicht einer virtuellen Maschine für einen virtuellen Computer-Skalierungs Satz (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="b6a06-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="b6a06-109">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b6a06-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="b6a06-110">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b6a06-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="b6a06-111">Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b6a06-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="b6a06-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6a06-112">EXAMPLES</span></span>

### <span data-ttu-id="b6a06-113">Beispiel 1: Abrufen der Eigenschaften eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="b6a06-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b6a06-114">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS001 ab, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="b6a06-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="b6a06-115">Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="b6a06-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="b6a06-116">Beispiel 2: Abrufen der Modell Ansichtseigenschaften eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="b6a06-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="b6a06-117">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS004 ab, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="b6a06-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="b6a06-118">Der Befehl ruft die in der Variablen $ID gespeicherte Instanz-ID ab, für die die Modellansicht abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6a06-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="b6a06-119">Beispiel 3: Abrufen der Eigenschaften der Instanzen Ansicht eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="b6a06-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="b6a06-120">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS004 ab, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="b6a06-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="b6a06-121">Da der Befehl den *InstanceView* -Switch-Parameter angibt, ruft das Cmdlet die Instanzen Ansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="b6a06-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="b6a06-122">Der Befehl ruft die in der Variablen $ID gespeicherte Instanz-ID ab, für die die Instanzen Ansicht abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6a06-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="b6a06-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6a06-123">PARAMETERS</span></span>

### <span data-ttu-id="b6a06-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a06-124">-DefaultProfile</span></span>
<span data-ttu-id="b6a06-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6a06-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a06-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b6a06-126">-InstanceId</span></span>
<span data-ttu-id="b6a06-127">Gibt die Instanz-ID an, für die die Modellansicht abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6a06-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a06-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="b6a06-128">-InstanceView</span></span>
<span data-ttu-id="b6a06-129">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="b6a06-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="b6a06-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a06-130">-ResourceGroupName</span></span>
<span data-ttu-id="b6a06-131">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="b6a06-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a06-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b6a06-132">-VMScaleSetName</span></span>
<span data-ttu-id="b6a06-133">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="b6a06-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a06-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a06-134">CommonParameters</span></span>
<span data-ttu-id="b6a06-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a06-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a06-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6a06-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a06-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6a06-137">INPUTS</span></span>

### <span data-ttu-id="b6a06-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a06-138">System.String</span></span>

## <span data-ttu-id="b6a06-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6a06-139">OUTPUTS</span></span>

### <span data-ttu-id="b6a06-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b6a06-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b6a06-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6a06-141">NOTES</span></span>

## <span data-ttu-id="b6a06-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6a06-142">RELATED LINKS</span></span>

[<span data-ttu-id="b6a06-143">Satz-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="b6a06-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="b6a06-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6a06-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


