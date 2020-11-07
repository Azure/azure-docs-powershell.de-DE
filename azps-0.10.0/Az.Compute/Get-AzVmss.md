---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844552"
---
# <span data-ttu-id="e312e-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-101">Get-AzVmss</span></span>

## <span data-ttu-id="e312e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e312e-102">SYNOPSIS</span></span>
<span data-ttu-id="e312e-103">Ruft die Eigenschaften eines VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="e312e-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="e312e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e312e-104">SYNTAX</span></span>

### <span data-ttu-id="e312e-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="e312e-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e312e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="e312e-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e312e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e312e-107">DESCRIPTION</span></span>
<span data-ttu-id="e312e-108">Das Cmdlet " **Get-AzVmss** " Ruft die Modell-und Instanzen Ansicht eines virtuellen Computer-Skalierungs Satzes (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="e312e-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e312e-109">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e312e-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="e312e-110">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e312e-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="e312e-111">Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e312e-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="e312e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e312e-112">EXAMPLES</span></span>

### <span data-ttu-id="e312e-113">Beispiel 1: Abrufen der Eigenschaften eines VMSS</span><span class="sxs-lookup"><span data-stu-id="e312e-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e312e-114">Dieser Befehl ruft die Eigenschaften des VMSS mit dem Namen VMSS001 ab, das zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="e312e-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="e312e-115">Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="e312e-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="e312e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="e312e-116">PARAMETERS</span></span>

### <span data-ttu-id="e312e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e312e-117">-DefaultProfile</span></span>
<span data-ttu-id="e312e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e312e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e312e-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="e312e-119">-InstanceView</span></span>
<span data-ttu-id="e312e-120">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="e312e-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="e312e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e312e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e312e-122">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="e312e-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="e312e-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e312e-123">-VMScaleSetName</span></span>
<span data-ttu-id="e312e-124">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="e312e-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="e312e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e312e-125">CommonParameters</span></span>
<span data-ttu-id="e312e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e312e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e312e-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e312e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e312e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e312e-128">INPUTS</span></span>

### <span data-ttu-id="e312e-129">Keine</span><span class="sxs-lookup"><span data-stu-id="e312e-129">None</span></span>
<span data-ttu-id="e312e-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e312e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e312e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e312e-131">OUTPUTS</span></span>

### <span data-ttu-id="e312e-132">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e312e-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e312e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e312e-133">NOTES</span></span>

## <span data-ttu-id="e312e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e312e-134">RELATED LINKS</span></span>

[<span data-ttu-id="e312e-135">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="e312e-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="e312e-137">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="e312e-138">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="e312e-139">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="e312e-140">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="e312e-141">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e312e-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


