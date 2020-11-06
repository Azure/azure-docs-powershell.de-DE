---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505194"
---
# <span data-ttu-id="c69f5-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c69f5-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="c69f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c69f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c69f5-103">Deaktiviert die Datenträgerverschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="c69f5-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c69f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c69f5-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c69f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c69f5-105">DESCRIPTION</span></span>
<span data-ttu-id="c69f5-106">Deaktiviert die Datenträgerverschlüsselung auf einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="c69f5-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="c69f5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c69f5-107">EXAMPLES</span></span>

### <span data-ttu-id="c69f5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c69f5-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c69f5-109">Deaktiviert die Datenträgerverschlüsselung auf dem VM-Skalierungs Satz mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="c69f5-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c69f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c69f5-110">PARAMETERS</span></span>

### <span data-ttu-id="c69f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69f5-111">-DefaultProfile</span></span>
<span data-ttu-id="c69f5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c69f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c69f5-113">-ExtensionName</span></span>
<span data-ttu-id="c69f5-114">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c69f5-114">The extension name.</span></span>
<span data-ttu-id="c69f5-115">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="c69f5-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c69f5-116">-Force</span></span>
<span data-ttu-id="c69f5-117">, Um das Entfernen der Erweiterung vom virtuellen Computer zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c69f5-117">To force the removal of the extension from the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="c69f5-118">-ForceUpdate</span></span>
<span data-ttu-id="c69f5-119">Generieren einer Kategorie für die Erzwingung des Updates</span><span class="sxs-lookup"><span data-stu-id="c69f5-119">Generate a tag for force update.</span></span>  <span data-ttu-id="c69f5-120">Dies sollte angegeben werden, um wiederholte Verschlüsselungsvorgänge für denselben virtuellen Computer durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c69f5-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="c69f5-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c69f5-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c69f5-123">-VMScaleSetName</span></span>
<span data-ttu-id="c69f5-124">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c69f5-124">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-125">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="c69f5-125">-VolumeType</span></span>
<span data-ttu-id="c69f5-126">Typ des Volumes (Betriebssystem oder Daten) zum Durchführen eines Verschlüsselungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="c69f5-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c69f5-127">-Confirm</span></span>
<span data-ttu-id="c69f5-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c69f5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c69f5-129">-WhatIf</span></span>
<span data-ttu-id="c69f5-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c69f5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c69f5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c69f5-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69f5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69f5-132">CommonParameters</span></span>
<span data-ttu-id="c69f5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69f5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69f5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69f5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69f5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c69f5-135">INPUTS</span></span>

### <span data-ttu-id="c69f5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c69f5-136">System.String</span></span>

## <span data-ttu-id="c69f5-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c69f5-137">OUTPUTS</span></span>

### <span data-ttu-id="c69f5-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c69f5-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c69f5-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c69f5-139">NOTES</span></span>

## <span data-ttu-id="c69f5-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c69f5-140">RELATED LINKS</span></span>

