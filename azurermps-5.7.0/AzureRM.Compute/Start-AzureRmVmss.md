---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497677"
---
# <span data-ttu-id="45509-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="45509-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45509-102">SYNOPSIS</span></span>
<span data-ttu-id="45509-103">Startet die VMSS oder einen Satz virtueller Computer innerhalb des VMSS.</span><span class="sxs-lookup"><span data-stu-id="45509-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45509-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45509-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45509-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45509-105">DESCRIPTION</span></span>
<span data-ttu-id="45509-106">Mit dem **Start-AzureRmVmss-** Cmdlet werden alle virtuellen Computer im virtuellen Computer-Skalierungs Satz (VMSS) oder eine Gruppe virtueller Computer gestartet.</span><span class="sxs-lookup"><span data-stu-id="45509-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="45509-107">Sie können den *InstanceId* -Parameter verwenden, um einen Satz virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="45509-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="45509-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45509-108">EXAMPLES</span></span>

### <span data-ttu-id="45509-109">Beispiel 1: Starten einer bestimmten Gruppe von virtuellen Computern innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="45509-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="45509-110">Mit diesem Befehl wird ein bestimmter Satz virtueller Computer gestartet, die durch das Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="45509-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="45509-111">Beispiel 2: Starten aller virtuellen Computer innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="45509-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="45509-112">Mit diesem Befehl werden alle virtuellen Computer gestartet, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="45509-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="45509-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="45509-113">PARAMETERS</span></span>

### <span data-ttu-id="45509-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="45509-114">-InstanceId</span></span>
<span data-ttu-id="45509-115">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen an, die vom Cmdlet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="45509-115">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="45509-116">Zum Beispiel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="45509-116">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="45509-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45509-117">-ResourceGroupName</span></span>
<span data-ttu-id="45509-118">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="45509-118">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="45509-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="45509-119">-VMScaleSetName</span></span>
<span data-ttu-id="45509-120">Gibt den Namen des VMSS an, mit dem das Cmdlet die virtuellen Computer startet.</span><span class="sxs-lookup"><span data-stu-id="45509-120">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="45509-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45509-121">-Confirm</span></span>
<span data-ttu-id="45509-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45509-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45509-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45509-123">-WhatIf</span></span>
<span data-ttu-id="45509-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45509-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45509-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45509-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45509-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45509-126">CommonParameters</span></span>
<span data-ttu-id="45509-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45509-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45509-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45509-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45509-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45509-129">INPUTS</span></span>

### <span data-ttu-id="45509-130">Keine</span><span class="sxs-lookup"><span data-stu-id="45509-130">None</span></span>
<span data-ttu-id="45509-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="45509-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45509-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45509-132">OUTPUTS</span></span>

###  
<span data-ttu-id="45509-133">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="45509-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="45509-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="45509-134">NOTES</span></span>

## <span data-ttu-id="45509-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45509-135">RELATED LINKS</span></span>

[<span data-ttu-id="45509-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="45509-137">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="45509-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="45509-139">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="45509-140">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="45509-141">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="45509-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="45509-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


