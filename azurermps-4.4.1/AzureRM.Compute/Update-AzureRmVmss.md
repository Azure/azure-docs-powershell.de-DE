---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499173"
---
# <span data-ttu-id="fa19a-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="fa19a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa19a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa19a-103">Aktualisiert den Zustand eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa19a-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa19a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa19a-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa19a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa19a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa19a-106">Das Cmdlet **Update-AzureRmVmss** aktualisiert den Zustand eines virtuellen Computer-Skalierungs Satzes (VMSS) auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fa19a-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="fa19a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa19a-107">EXAMPLES</span></span>

### <span data-ttu-id="fa19a-108">Beispiel 1: Aktualisieren Sie den Zustand eines VMSS auf den Zustand eines lokalen VMSS-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fa19a-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="fa19a-109">Dieser Befehl aktualisiert den Zustand des VMSS mit dem Namen VMSS001, der zur Ressourcengruppe namens Group001 gehört, in den Zustand eines lokalen VMSS-Objekts mit dem Namen LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="fa19a-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="fa19a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa19a-110">PARAMETERS</span></span>

### <span data-ttu-id="fa19a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa19a-111">-DefaultProfile</span></span>
<span data-ttu-id="fa19a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa19a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa19a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa19a-113">-ResourceGroupName</span></span>
<span data-ttu-id="fa19a-114">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="fa19a-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="fa19a-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fa19a-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fa19a-116">Gibt ein lokales VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fa19a-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="fa19a-117">Verwenden Sie das Get-AzureRmVmss-Cmdlet, um ein VMSS-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fa19a-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="fa19a-118">Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für die VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa19a-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa19a-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fa19a-119">-VMScaleSetName</span></span>
<span data-ttu-id="fa19a-120">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="fa19a-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fa19a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa19a-121">-Confirm</span></span>
<span data-ttu-id="fa19a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa19a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa19a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa19a-123">-WhatIf</span></span>
<span data-ttu-id="fa19a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa19a-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fa19a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa19a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa19a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa19a-126">CommonParameters</span></span>
<span data-ttu-id="fa19a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa19a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa19a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa19a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa19a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa19a-129">INPUTS</span></span>

## <span data-ttu-id="fa19a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa19a-130">OUTPUTS</span></span>

## <span data-ttu-id="fa19a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa19a-131">NOTES</span></span>

## <span data-ttu-id="fa19a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa19a-132">RELATED LINKS</span></span>

[<span data-ttu-id="fa19a-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="fa19a-134">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="fa19a-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="fa19a-136">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="fa19a-137">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="fa19a-138">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="fa19a-139">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fa19a-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


