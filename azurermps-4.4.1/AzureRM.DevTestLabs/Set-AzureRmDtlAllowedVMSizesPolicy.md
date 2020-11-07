---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8248c5ef5e4de2ab945d7f5f39dd4eea6defdf8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663944"
---
# <span data-ttu-id="3759f-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="3759f-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="3759f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3759f-102">SYNOPSIS</span></span>
<span data-ttu-id="3759f-103">Legt die zulässige Größen Richtlinie für virtuelle Maschinen einer Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="3759f-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3759f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3759f-104">SYNTAX</span></span>

### <span data-ttu-id="3759f-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="3759f-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3759f-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="3759f-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3759f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3759f-107">DESCRIPTION</span></span>
<span data-ttu-id="3759f-108">Das Cmdlet " **Set-AzureRmDtlAllowedVMSizesPolicy** " legt die zulässige Größen Richtlinie für virtuelle Maschinen fest, die eine Liste der in einer Übungseinheit zulässigen virtuellen Computer Größen angibt.</span><span class="sxs-lookup"><span data-stu-id="3759f-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="3759f-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3759f-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="3759f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3759f-110">EXAMPLES</span></span>

## <span data-ttu-id="3759f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3759f-111">PARAMETERS</span></span>

### <span data-ttu-id="3759f-112">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="3759f-112">-Disable</span></span>
<span data-ttu-id="3759f-113">Gibt an, dass dieses Cmdlet die Richtlinie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3759f-113">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3759f-114">-Enable</span><span class="sxs-lookup"><span data-stu-id="3759f-114">-Enable</span></span>
<span data-ttu-id="3759f-115">Gibt an, dass dieses Cmdlet die Richtlinie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3759f-115">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3759f-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="3759f-116">-LabName</span></span>
<span data-ttu-id="3759f-117">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinien für virtuelle Computer Größen festlegt.</span><span class="sxs-lookup"><span data-stu-id="3759f-117">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="3759f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3759f-118">-ResourceGroupName</span></span>
<span data-ttu-id="3759f-119">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="3759f-119">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="3759f-120">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="3759f-120">-VmSizes</span></span>
<span data-ttu-id="3759f-121">Gibt als Zeichenfolgenarray die Liste der Größen für virtuelle Maschinen an, die in der Übungseinheit zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3759f-121">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3759f-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3759f-122">-Confirm</span></span>
<span data-ttu-id="3759f-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3759f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3759f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3759f-124">-WhatIf</span></span>
<span data-ttu-id="3759f-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3759f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3759f-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3759f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3759f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3759f-127">-DefaultProfile</span></span>
<span data-ttu-id="3759f-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3759f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3759f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3759f-129">CommonParameters</span></span>
<span data-ttu-id="3759f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3759f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3759f-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3759f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3759f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3759f-132">INPUTS</span></span>

## <span data-ttu-id="3759f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3759f-133">OUTPUTS</span></span>

### <span data-ttu-id="3759f-134">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="3759f-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="3759f-135">Dieses Cmdlet gibt die Richtlinie zurück, die die Liste der in der Übungseinheit zulässigen virtuellen Computer Größen angibt.</span><span class="sxs-lookup"><span data-stu-id="3759f-135">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="3759f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="3759f-136">NOTES</span></span>

## <span data-ttu-id="3759f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3759f-137">RELATED LINKS</span></span>

[<span data-ttu-id="3759f-138">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="3759f-138">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


