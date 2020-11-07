---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664113"
---
# <span data-ttu-id="54377-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="54377-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54377-102">SYNOPSIS</span></span>
<span data-ttu-id="54377-103">Ruft die Eigenschaften eines VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="54377-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54377-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54377-104">SYNTAX</span></span>

### <span data-ttu-id="54377-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="54377-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54377-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="54377-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54377-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="54377-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54377-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54377-108">DESCRIPTION</span></span>
<span data-ttu-id="54377-109">Das Cmdlet " **Get-AzureRmVmss** " Ruft die Modell-und Instanzen Ansicht eines virtuellen Computer-Skalierungs Satzes (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="54377-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="54377-110">Die Modellansicht ist die benutzerdefinierten Eigenschaften des Skalierungs Satzes für virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="54377-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="54377-111">Bei der Instanzansicht handelt es sich um den Status der Instanzebene für den Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="54377-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="54377-112">Geben Sie den *InstanceView* -Parameter an, um nur die Instanzen Ansicht eines Skalierungs Satzes für virtuelle Maschinen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="54377-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="54377-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54377-113">EXAMPLES</span></span>

### <span data-ttu-id="54377-114">Beispiel 1: Abrufen der Eigenschaften eines VMSS</span><span class="sxs-lookup"><span data-stu-id="54377-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="54377-115">Dieser Befehl ruft die Eigenschaften des VMSS mit dem Namen VMSS001 ab, das zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="54377-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="54377-116">Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des Skalierungs Satzes für virtuelle Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="54377-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="54377-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="54377-117">PARAMETERS</span></span>

### <span data-ttu-id="54377-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54377-118">-DefaultProfile</span></span>
<span data-ttu-id="54377-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54377-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54377-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="54377-120">-InstanceView</span></span>
<span data-ttu-id="54377-121">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des Skalierungs Satzes für virtuelle Maschinen abruft.</span><span class="sxs-lookup"><span data-stu-id="54377-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="54377-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="54377-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="54377-123">Gibt an, dass dieses Cmdlet das Betriebssystem-Upgrade-Protokoll des Skalierungs Satzes für virtuelle Maschinen aufführt.</span><span class="sxs-lookup"><span data-stu-id="54377-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54377-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54377-124">-ResourceGroupName</span></span>
<span data-ttu-id="54377-125">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="54377-125">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54377-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="54377-126">-VMScaleSetName</span></span>
<span data-ttu-id="54377-127">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="54377-127">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54377-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54377-128">CommonParameters</span></span>
<span data-ttu-id="54377-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54377-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54377-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54377-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54377-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54377-131">INPUTS</span></span>

### <span data-ttu-id="54377-132">System. String</span><span class="sxs-lookup"><span data-stu-id="54377-132">System.String</span></span>

## <span data-ttu-id="54377-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54377-133">OUTPUTS</span></span>

### <span data-ttu-id="54377-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54377-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="54377-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="54377-135">NOTES</span></span>

## <span data-ttu-id="54377-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54377-136">RELATED LINKS</span></span>

[<span data-ttu-id="54377-137">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="54377-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="54377-139">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="54377-140">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="54377-141">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="54377-142">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="54377-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54377-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


