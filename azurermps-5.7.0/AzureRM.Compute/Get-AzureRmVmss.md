---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503853"
---
# <span data-ttu-id="a69fb-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="a69fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a69fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a69fb-103">Ruft die Eigenschaften eines VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="a69fb-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a69fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a69fb-104">SYNTAX</span></span>

### <span data-ttu-id="a69fb-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="a69fb-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="a69fb-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a69fb-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## <span data-ttu-id="a69fb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a69fb-107">DESCRIPTION</span></span>
<span data-ttu-id="a69fb-108">Das Cmdlet " **Get-AzureRmVmss** " Ruft die Modell-und Instanzen Ansicht eines virtuellen Computer-Skalierungs Satzes (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="a69fb-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a69fb-109">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="a69fb-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="a69fb-110">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="a69fb-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="a69fb-111">Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a69fb-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="a69fb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a69fb-112">EXAMPLES</span></span>

### <span data-ttu-id="a69fb-113">Beispiel 1: Abrufen der Eigenschaften eines VMSS</span><span class="sxs-lookup"><span data-stu-id="a69fb-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a69fb-114">Dieser Befehl ruft die Eigenschaften des VMSS mit dem Namen VMSS001 ab, das zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="a69fb-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="a69fb-115">Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="a69fb-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="a69fb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a69fb-116">PARAMETERS</span></span>

### <span data-ttu-id="a69fb-117">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="a69fb-117">-InstanceView</span></span>
<span data-ttu-id="a69fb-118">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="a69fb-118">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="a69fb-120">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="a69fb-120">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="a69fb-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a69fb-121">-VMScaleSetName</span></span>
<span data-ttu-id="a69fb-122">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="a69fb-122">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="a69fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69fb-123">CommonParameters</span></span>
<span data-ttu-id="a69fb-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69fb-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a69fb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69fb-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a69fb-126">INPUTS</span></span>

### <span data-ttu-id="a69fb-127">Keine</span><span class="sxs-lookup"><span data-stu-id="a69fb-127">None</span></span>
<span data-ttu-id="a69fb-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a69fb-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a69fb-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a69fb-129">OUTPUTS</span></span>

### <span data-ttu-id="a69fb-130">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a69fb-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a69fb-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a69fb-131">NOTES</span></span>

## <span data-ttu-id="a69fb-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a69fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="a69fb-133">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a69fb-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a69fb-135">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a69fb-136">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="a69fb-137">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="a69fb-138">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a69fb-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a69fb-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


