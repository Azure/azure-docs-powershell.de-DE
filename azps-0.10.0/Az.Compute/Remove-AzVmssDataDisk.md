---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844348"
---
# <span data-ttu-id="368d2-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="368d2-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="368d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="368d2-102">SYNOPSIS</span></span>
<span data-ttu-id="368d2-103">Entfernt einen Datenträger aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="368d2-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="368d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="368d2-104">SYNTAX</span></span>

### <span data-ttu-id="368d2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="368d2-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="368d2-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="368d2-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="368d2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="368d2-107">DESCRIPTION</span></span>
<span data-ttu-id="368d2-108">Das Cmdlet **Remove-AzVmssDataDisk** entfernt einen Datenträger aus der Instanz des virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="368d2-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="368d2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="368d2-109">EXAMPLES</span></span>

### <span data-ttu-id="368d2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="368d2-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="368d2-111">Dieser Befehl entfernt den Datenträger mit dem Namen "DataDisk1" aus dem VMSS-Objekt.</span><span class="sxs-lookup"><span data-stu-id="368d2-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="368d2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="368d2-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="368d2-113">Mit diesem Befehl wird der Daten Datenträger von LUN 0 aus dem VMSS-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="368d2-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="368d2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="368d2-114">PARAMETERS</span></span>

### <span data-ttu-id="368d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368d2-115">-DefaultProfile</span></span>
<span data-ttu-id="368d2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="368d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="368d2-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="368d2-117">-Lun</span></span>
<span data-ttu-id="368d2-118">Gibt die logische Einheitsnummer des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="368d2-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="368d2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="368d2-119">-Name</span></span>
<span data-ttu-id="368d2-120">Gibt den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="368d2-120">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="368d2-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="368d2-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="368d2-122">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="368d2-122">Specify the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="368d2-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="368d2-123">-Confirm</span></span>
<span data-ttu-id="368d2-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="368d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="368d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="368d2-125">-WhatIf</span></span>
<span data-ttu-id="368d2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="368d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="368d2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="368d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="368d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368d2-128">CommonParameters</span></span>
<span data-ttu-id="368d2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="368d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368d2-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="368d2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368d2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="368d2-131">INPUTS</span></span>

### <span data-ttu-id="368d2-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="368d2-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="368d2-133">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="368d2-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="368d2-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="368d2-134">OUTPUTS</span></span>

### <span data-ttu-id="368d2-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="368d2-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="368d2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="368d2-136">NOTES</span></span>

## <span data-ttu-id="368d2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="368d2-137">RELATED LINKS</span></span>

