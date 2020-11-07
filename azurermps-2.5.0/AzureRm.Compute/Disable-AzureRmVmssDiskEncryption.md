---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: b130be059432a6ca21fb0c1669660ebed34c670e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850164"
---
# <span data-ttu-id="dd658-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="dd658-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="dd658-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd658-102">SYNOPSIS</span></span>
<span data-ttu-id="dd658-103">Deaktiviert die Datenträgerverschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="dd658-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd658-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd658-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd658-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd658-105">DESCRIPTION</span></span>
<span data-ttu-id="dd658-106">Deaktiviert die Datenträgerverschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="dd658-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="dd658-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd658-107">EXAMPLES</span></span>

### <span data-ttu-id="dd658-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd658-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="dd658-109">Deaktiviert die Datenträgerverschlüsselung auf dem VM-Skalierungs Satz mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="dd658-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="dd658-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd658-110">PARAMETERS</span></span>

### <span data-ttu-id="dd658-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd658-111">-AsJob</span></span>
<span data-ttu-id="dd658-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dd658-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd658-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd658-113">-DefaultProfile</span></span>
<span data-ttu-id="dd658-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd658-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd658-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="dd658-115">-ExtensionName</span></span>
<span data-ttu-id="dd658-116">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd658-116">The extension name.</span></span>
<span data-ttu-id="dd658-117">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd658-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd658-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dd658-118">-Force</span></span>
<span data-ttu-id="dd658-119">, Um das Entfernen der Erweiterung vom virtuellen Computer zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="dd658-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="dd658-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="dd658-120">-ForceUpdate</span></span>
<span data-ttu-id="dd658-121">Generieren einer Kategorie für die Erzwingung des Updates</span><span class="sxs-lookup"><span data-stu-id="dd658-121">Generate a tag for force update.</span></span>  <span data-ttu-id="dd658-122">Dies sollte angegeben werden, um wiederholte Verschlüsselungsvorgänge für denselben virtuellen Computer durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="dd658-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd658-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd658-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd658-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd658-124">The resource group name.</span></span>

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

### <span data-ttu-id="dd658-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dd658-125">-VMScaleSetName</span></span>
<span data-ttu-id="dd658-126">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="dd658-126">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd658-127">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="dd658-127">-VolumeType</span></span>
<span data-ttu-id="dd658-128">Typ des Volumes (Betriebssystem oder Daten) zum Durchführen eines Verschlüsselungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="dd658-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd658-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd658-129">-Confirm</span></span>
<span data-ttu-id="dd658-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd658-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd658-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd658-131">-WhatIf</span></span>
<span data-ttu-id="dd658-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd658-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd658-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd658-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd658-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd658-134">CommonParameters</span></span>
<span data-ttu-id="dd658-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd658-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd658-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd658-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd658-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd658-137">INPUTS</span></span>

### <span data-ttu-id="dd658-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dd658-138">System.String</span></span>

## <span data-ttu-id="dd658-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd658-139">OUTPUTS</span></span>

### <span data-ttu-id="dd658-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd658-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dd658-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd658-141">NOTES</span></span>

## <span data-ttu-id="dd658-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd658-142">RELATED LINKS</span></span>

