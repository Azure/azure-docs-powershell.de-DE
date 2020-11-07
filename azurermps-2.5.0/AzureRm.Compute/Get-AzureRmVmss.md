---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849776"
---
# <span data-ttu-id="46f51-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="46f51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46f51-102">SYNOPSIS</span></span>
<span data-ttu-id="46f51-103">Ruft die Eigenschaften eines VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="46f51-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46f51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46f51-104">SYNTAX</span></span>

### <span data-ttu-id="46f51-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="46f51-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46f51-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="46f51-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46f51-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46f51-107">DESCRIPTION</span></span>
<span data-ttu-id="46f51-108">Das Cmdlet " **Get-AzureRmVmss** " Ruft die Modell-und Instanzen Ansicht eines virtuellen Computer-Skalierungs Satzes (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="46f51-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="46f51-109">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="46f51-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="46f51-110">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="46f51-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="46f51-111">Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="46f51-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="46f51-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46f51-112">EXAMPLES</span></span>

### <span data-ttu-id="46f51-113">Beispiel 1: Abrufen der Eigenschaften eines VMSS</span><span class="sxs-lookup"><span data-stu-id="46f51-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="46f51-114">Dieser Befehl ruft die Eigenschaften des VMSS mit dem Namen VMSS001 ab, das zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="46f51-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="46f51-115">Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="46f51-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="46f51-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="46f51-116">PARAMETERS</span></span>

### <span data-ttu-id="46f51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f51-117">-DefaultProfile</span></span>
<span data-ttu-id="46f51-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46f51-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46f51-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="46f51-119">-InstanceView</span></span>
<span data-ttu-id="46f51-120">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="46f51-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="46f51-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f51-121">-ResourceGroupName</span></span>
<span data-ttu-id="46f51-122">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="46f51-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="46f51-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="46f51-123">-VMScaleSetName</span></span>
<span data-ttu-id="46f51-124">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="46f51-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="46f51-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f51-125">CommonParameters</span></span>
<span data-ttu-id="46f51-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f51-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f51-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f51-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f51-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46f51-128">INPUTS</span></span>

### <span data-ttu-id="46f51-129">Keine</span><span class="sxs-lookup"><span data-stu-id="46f51-129">None</span></span>
<span data-ttu-id="46f51-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="46f51-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46f51-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46f51-131">OUTPUTS</span></span>

### <span data-ttu-id="46f51-132">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="46f51-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="46f51-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="46f51-133">NOTES</span></span>

## <span data-ttu-id="46f51-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46f51-134">RELATED LINKS</span></span>

[<span data-ttu-id="46f51-135">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="46f51-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="46f51-137">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="46f51-138">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="46f51-139">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="46f51-140">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="46f51-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f51-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


