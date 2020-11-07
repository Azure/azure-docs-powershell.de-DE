---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850447"
---
# <span data-ttu-id="e72e8-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="e72e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e72e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e72e8-103">Startet die VMSS oder einen virtuellen Computer im VMSS neu.</span><span class="sxs-lookup"><span data-stu-id="e72e8-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e72e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e72e8-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e72e8-105">DESCRIPTION</span></span>
<span data-ttu-id="e72e8-106">Mit dem Cmdlet " **Restart-AzureRmVmss** " wird der Skalierungs Satz für virtuelle Computer neu gestartet (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e72e8-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e72e8-107">Dieses Cmdlet kann auch verwendet werden, um einen bestimmten virtuellen Computer innerhalb des VMSS mit dem *InstanceId* -Parameter neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e72e8-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="e72e8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e72e8-108">EXAMPLES</span></span>

### <span data-ttu-id="e72e8-109">Beispiel 1: Neustarten des VMSS</span><span class="sxs-lookup"><span data-stu-id="e72e8-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="e72e8-110">Mit diesem Befehl wird der VMSS mit dem Namen VMSS001 neu gestartet, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="e72e8-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="e72e8-111">Beispiel 2: Neustarten eines bestimmten virtuellen Computers innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="e72e8-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="e72e8-112">Dieser Befehl startet einen virtuellen Computer mit der Instanz-ID 1 im VMSS mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="e72e8-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e72e8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e72e8-113">PARAMETERS</span></span>

### <span data-ttu-id="e72e8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e72e8-114">-AsJob</span></span>
<span data-ttu-id="e72e8-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="e72e8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72e8-116">-DefaultProfile</span></span>
<span data-ttu-id="e72e8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e72e8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e72e8-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e72e8-118">-InstanceId</span></span>
<span data-ttu-id="e72e8-119">Gibt als Zeichenfolgenarray die ID der Instanzen an, die neu gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e72e8-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="e72e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="e72e8-121">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="e72e8-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="e72e8-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e72e8-122">-VMScaleSetName</span></span>
<span data-ttu-id="e72e8-123">Art der Name des VMSS, den dieses Cmdlet neu startet.</span><span class="sxs-lookup"><span data-stu-id="e72e8-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="e72e8-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e72e8-124">-Confirm</span></span>
<span data-ttu-id="e72e8-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e72e8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72e8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72e8-126">-WhatIf</span></span>
<span data-ttu-id="e72e8-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e72e8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e72e8-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e72e8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e72e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72e8-129">CommonParameters</span></span>
<span data-ttu-id="e72e8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72e8-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e72e8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72e8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e72e8-132">INPUTS</span></span>

### <span data-ttu-id="e72e8-133">Keine</span><span class="sxs-lookup"><span data-stu-id="e72e8-133">None</span></span>
<span data-ttu-id="e72e8-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e72e8-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e72e8-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e72e8-135">OUTPUTS</span></span>

###  
<span data-ttu-id="e72e8-136">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e72e8-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e72e8-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e72e8-137">NOTES</span></span>

## <span data-ttu-id="e72e8-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e72e8-138">RELATED LINKS</span></span>

[<span data-ttu-id="e72e8-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e72e8-140">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e72e8-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e72e8-142">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="e72e8-143">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e72e8-144">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e72e8-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e72e8-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


