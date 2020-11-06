---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 5733939c24437c974f629588106d6240766a9df1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483129"
---
# <span data-ttu-id="385bb-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="385bb-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="385bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="385bb-102">SYNOPSIS</span></span>
<span data-ttu-id="385bb-103">Ruft Informationen zur Erweiterung des Chefkochs ab.</span><span class="sxs-lookup"><span data-stu-id="385bb-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="385bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="385bb-104">SYNTAX</span></span>

### <span data-ttu-id="385bb-105">Linux</span><span class="sxs-lookup"><span data-stu-id="385bb-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [<CommonParameters>]
```

### <span data-ttu-id="385bb-106">Windows</span><span class="sxs-lookup"><span data-stu-id="385bb-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [<CommonParameters>]
```

## <span data-ttu-id="385bb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="385bb-107">DESCRIPTION</span></span>
<span data-ttu-id="385bb-108">Das Cmdlet " **Get-AzureVMChefExtension** " Ruft Informationen zu einer auf einem virtuellen Computer installierten Chefkoch-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="385bb-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="385bb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="385bb-109">EXAMPLES</span></span>

### <span data-ttu-id="385bb-110">Beispiel 1: Abrufen der Details der Erweiterung "Chef" für einen virtuellen Windows-Computer –</span><span class="sxs-lookup"><span data-stu-id="385bb-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="385bb-111">Dieser Befehl ruft die Erweiterung des Chefkochs von einem Windows-virtuellen Computer mit dem Namen WindowsVM001 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="385bb-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="385bb-112">Beispiel 2: Abrufen der Details der Erweiterung "Chef" für einen virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="385bb-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="385bb-113">Dieser Befehl ruft die Erweiterung des Chefkochs von einem virtuellen Linux-Computer mit dem Namen LinuxVM001 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="385bb-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="385bb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="385bb-114">PARAMETERS</span></span>

### <span data-ttu-id="385bb-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="385bb-115">-Linux</span></span>
<span data-ttu-id="385bb-116">Gibt an, dass dieses Cmdlet auf einem virtuellen Linux-Computer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="385bb-116">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385bb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="385bb-117">-Name</span></span>
<span data-ttu-id="385bb-118">Gibt den Namen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="385bb-118">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="385bb-120">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="385bb-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385bb-121">-Status</span><span class="sxs-lookup"><span data-stu-id="385bb-121">-Status</span></span>
<span data-ttu-id="385bb-122">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der Erweiterung "Chef" erhält.</span><span class="sxs-lookup"><span data-stu-id="385bb-122">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385bb-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="385bb-123">-VMName</span></span>
<span data-ttu-id="385bb-124">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="385bb-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385bb-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="385bb-125">-Windows</span></span>
<span data-ttu-id="385bb-126">Gibt an, dass dieses Cmdlet für einen virtuellen Windows-Computer gilt.</span><span class="sxs-lookup"><span data-stu-id="385bb-126">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385bb-127">CommonParameters</span></span>
<span data-ttu-id="385bb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385bb-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385bb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385bb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="385bb-130">INPUTS</span></span>

### <span data-ttu-id="385bb-131">Keine</span><span class="sxs-lookup"><span data-stu-id="385bb-131">None</span></span>
<span data-ttu-id="385bb-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="385bb-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="385bb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="385bb-133">OUTPUTS</span></span>

## <span data-ttu-id="385bb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="385bb-134">NOTES</span></span>

## <span data-ttu-id="385bb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="385bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="385bb-136">Satz-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="385bb-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="385bb-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="385bb-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


