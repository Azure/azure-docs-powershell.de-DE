---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850895"
---
# <span data-ttu-id="27a8f-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="27a8f-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="27a8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="27a8f-103">Ändert den Zustand einer VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="27a8f-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27a8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27a8f-104">SYNTAX</span></span>

### <span data-ttu-id="27a8f-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="27a8f-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a8f-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="27a8f-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27a8f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27a8f-107">DESCRIPTION</span></span>
<span data-ttu-id="27a8f-108">Das Cmdlet " **Satz-AzureRmVmssVM** " ändert den Zustand einer Virtual Machine Scale Sets (VMSS)-Instanz.</span><span class="sxs-lookup"><span data-stu-id="27a8f-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="27a8f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27a8f-109">EXAMPLES</span></span>

## <span data-ttu-id="27a8f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="27a8f-110">PARAMETERS</span></span>

### <span data-ttu-id="27a8f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27a8f-111">-AsJob</span></span>
<span data-ttu-id="27a8f-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="27a8f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27a8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a8f-113">-DefaultProfile</span></span>
<span data-ttu-id="27a8f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27a8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27a8f-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="27a8f-115">-InstanceId</span></span>
<span data-ttu-id="27a8f-116">Gibt die ID der VMSS-Instanz an, für die dieses Cmdlet den Zustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="27a8f-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a8f-117">-Reimage</span><span class="sxs-lookup"><span data-stu-id="27a8f-117">-Reimage</span></span>
<span data-ttu-id="27a8f-118">Gibt an, dass dieses Cmdlet die VMSS-Instanz erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="27a8f-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a8f-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="27a8f-119">-ReimageAll</span></span>
<span data-ttu-id="27a8f-120">Gibt an, dass das Cmdlet alle Datenträger in der VMSS-Instanz umbildet.</span><span class="sxs-lookup"><span data-stu-id="27a8f-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="27a8f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a8f-121">-ResourceGroupName</span></span>
<span data-ttu-id="27a8f-122">Gibt den Namen der Ressourcengruppe an, die die VMSS-Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="27a8f-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="27a8f-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="27a8f-123">-VMScaleSetName</span></span>
<span data-ttu-id="27a8f-124">Gibt den Namen der VMSS-Instanz an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="27a8f-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="27a8f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27a8f-125">-Confirm</span></span>
<span data-ttu-id="27a8f-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27a8f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a8f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a8f-127">-WhatIf</span></span>
<span data-ttu-id="27a8f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27a8f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27a8f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27a8f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a8f-130">CommonParameters</span></span>
<span data-ttu-id="27a8f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a8f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a8f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a8f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27a8f-133">INPUTS</span></span>

### <span data-ttu-id="27a8f-134">Keine</span><span class="sxs-lookup"><span data-stu-id="27a8f-134">None</span></span>
<span data-ttu-id="27a8f-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="27a8f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27a8f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27a8f-136">OUTPUTS</span></span>

### <span data-ttu-id="27a8f-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="27a8f-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="27a8f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="27a8f-138">NOTES</span></span>

## <span data-ttu-id="27a8f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27a8f-139">RELATED LINKS</span></span>

[<span data-ttu-id="27a8f-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="27a8f-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
