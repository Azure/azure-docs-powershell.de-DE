---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: bac1bf365ff1135366f2612bfbe5ba313e2300b8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850919"
---
# <span data-ttu-id="519ae-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="519ae-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="519ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="519ae-102">SYNOPSIS</span></span>
<span data-ttu-id="519ae-103">Ruft die Eigenschaften eines virtuellen VMSS-Computers ab.</span><span class="sxs-lookup"><span data-stu-id="519ae-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="519ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="519ae-104">SYNTAX</span></span>

### <span data-ttu-id="519ae-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="519ae-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="519ae-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="519ae-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="519ae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="519ae-107">DESCRIPTION</span></span>
<span data-ttu-id="519ae-108">Das Cmdlet " **Get-AzureRmVmssVM** " Ruft die Modellansicht und die Instanzen Ansicht einer virtuellen Maschine für einen virtuellen Computer-Skalierungs Satz (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="519ae-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="519ae-109">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="519ae-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="519ae-110">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="519ae-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="519ae-111">Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="519ae-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="519ae-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="519ae-112">EXAMPLES</span></span>

### <span data-ttu-id="519ae-113">Beispiel 1: Abrufen der Eigenschaften eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="519ae-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="519ae-114">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS001 ab, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="519ae-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="519ae-115">Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="519ae-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="519ae-116">Beispiel 2: Abrufen der Modell Ansichtseigenschaften eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="519ae-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="519ae-117">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS004 ab, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="519ae-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="519ae-118">Der Befehl ruft die in der Variablen $ID gespeicherte Instanz-ID ab, für die die Modellansicht abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="519ae-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="519ae-119">Beispiel 3: Abrufen der Eigenschaften der Instanzen Ansicht eines virtuellen VMSS-Computers</span><span class="sxs-lookup"><span data-stu-id="519ae-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="519ae-120">Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS004 ab, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="519ae-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="519ae-121">Da der Befehl den *InstanceView* -Switch-Parameter angibt, ruft das Cmdlet die Instanzen Ansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="519ae-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="519ae-122">Der Befehl ruft die in der Variablen $ID gespeicherte Instanz-ID ab, für die die Instanzen Ansicht abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="519ae-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="519ae-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="519ae-123">PARAMETERS</span></span>

### <span data-ttu-id="519ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519ae-124">-DefaultProfile</span></span>
<span data-ttu-id="519ae-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="519ae-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="519ae-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="519ae-126">-InstanceId</span></span>
<span data-ttu-id="519ae-127">Gibt die Instanz-ID an, für die die Modellansicht abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="519ae-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519ae-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="519ae-128">-InstanceView</span></span>
<span data-ttu-id="519ae-129">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="519ae-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519ae-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="519ae-130">-ResourceGroupName</span></span>
<span data-ttu-id="519ae-131">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="519ae-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519ae-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="519ae-132">-VMScaleSetName</span></span>
<span data-ttu-id="519ae-133">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="519ae-133">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519ae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519ae-134">CommonParameters</span></span>
<span data-ttu-id="519ae-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="519ae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519ae-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="519ae-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519ae-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="519ae-137">INPUTS</span></span>

### <span data-ttu-id="519ae-138">Keine</span><span class="sxs-lookup"><span data-stu-id="519ae-138">None</span></span>
<span data-ttu-id="519ae-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="519ae-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="519ae-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="519ae-140">OUTPUTS</span></span>

### <span data-ttu-id="519ae-141">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="519ae-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="519ae-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="519ae-142">NOTES</span></span>

## <span data-ttu-id="519ae-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="519ae-143">RELATED LINKS</span></span>

[<span data-ttu-id="519ae-144">Satz-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="519ae-144">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="519ae-145">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="519ae-145">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


