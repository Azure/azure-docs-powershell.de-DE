---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477217"
---
# <span data-ttu-id="f30f7-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="f30f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f30f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f30f7-103">Legt bestimmte Aktionen für einen angegebenen VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="f30f7-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f30f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f30f7-104">SYNTAX</span></span>

### <span data-ttu-id="f30f7-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="f30f7-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30f7-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f30f7-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f30f7-107">DESCRIPTION</span></span>
<span data-ttu-id="f30f7-108">Das Cmdlet " **Set-AzureRmVmss** " legt bestimmte Aktionen für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f30f7-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f30f7-109">Die einzige Aktion, die dieses Cmdlet unterstützt, ist reimage.</span><span class="sxs-lookup"><span data-stu-id="f30f7-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="f30f7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f30f7-110">EXAMPLES</span></span>

### <span data-ttu-id="f30f7-111">Beispiel 1: umbilden einer VMSS</span><span class="sxs-lookup"><span data-stu-id="f30f7-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f30f7-112">Mit diesem Befehl wird der VMSS mit dem Namen ContosoVMSS, der zur Ressourcengruppe mit dem Namen contosogroup gehört, erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="f30f7-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f30f7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f30f7-113">PARAMETERS</span></span>

### <span data-ttu-id="f30f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30f7-114">-DefaultProfile</span></span>
<span data-ttu-id="f30f7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f30f7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30f7-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f30f7-116">-InstanceId</span></span>
<span data-ttu-id="f30f7-117">Die Instanz-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f30f7-117">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30f7-118">-Reimage</span><span class="sxs-lookup"><span data-stu-id="f30f7-118">-Reimage</span></span>
<span data-ttu-id="f30f7-119">Gibt an, dass das Cmdlet die VMSS.</span><span class="sxs-lookup"><span data-stu-id="f30f7-119">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30f7-120">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="f30f7-120">-ReimageAll</span></span>
<span data-ttu-id="f30f7-121">Gibt an, dass das Cmdlet alle Datenträger im VMSS umbildet.</span><span class="sxs-lookup"><span data-stu-id="f30f7-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="f30f7-123">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="f30f7-123">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30f7-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f30f7-124">-VMScaleSetName</span></span>
<span data-ttu-id="f30f7-125">Art der Name des VMSS, für das dieses Cmdlet Aktionen festlegt.</span><span class="sxs-lookup"><span data-stu-id="f30f7-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30f7-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f30f7-126">-Confirm</span></span>
<span data-ttu-id="f30f7-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f30f7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30f7-128">-WhatIf</span></span>
<span data-ttu-id="f30f7-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f30f7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f30f7-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f30f7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30f7-131">CommonParameters</span></span>
<span data-ttu-id="f30f7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30f7-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30f7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30f7-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f30f7-134">INPUTS</span></span>

## <span data-ttu-id="f30f7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f30f7-135">OUTPUTS</span></span>

### <span data-ttu-id="f30f7-136">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f30f7-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f30f7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f30f7-137">NOTES</span></span>

## <span data-ttu-id="f30f7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f30f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="f30f7-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="f30f7-140">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="f30f7-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="f30f7-142">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="f30f7-143">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="f30f7-144">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="f30f7-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f30f7-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


