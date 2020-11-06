---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479362"
---
# <span data-ttu-id="18fbf-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="18fbf-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="18fbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="18fbf-103">Ändert den Zustand einer VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="18fbf-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18fbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18fbf-104">SYNTAX</span></span>

### <span data-ttu-id="18fbf-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="18fbf-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18fbf-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="18fbf-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18fbf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18fbf-107">DESCRIPTION</span></span>
<span data-ttu-id="18fbf-108">Das Cmdlet " **Satz-AzureRmVmssVM** " ändert den Zustand einer Virtual Machine Scale Sets (VMSS)-Instanz.</span><span class="sxs-lookup"><span data-stu-id="18fbf-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="18fbf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18fbf-109">EXAMPLES</span></span>

## <span data-ttu-id="18fbf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="18fbf-110">PARAMETERS</span></span>

### <span data-ttu-id="18fbf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fbf-111">-DefaultProfile</span></span>
<span data-ttu-id="18fbf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18fbf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18fbf-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="18fbf-113">-InstanceId</span></span>
<span data-ttu-id="18fbf-114">Gibt die ID der VMSS-Instanz an, für die dieses Cmdlet den Zustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="18fbf-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fbf-115">-Reimage</span><span class="sxs-lookup"><span data-stu-id="18fbf-115">-Reimage</span></span>
<span data-ttu-id="18fbf-116">Gibt an, dass dieses Cmdlet die VMSS-Instanz erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="18fbf-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="18fbf-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="18fbf-117">-ReimageAll</span></span>
<span data-ttu-id="18fbf-118">Gibt an, dass das Cmdlet alle Datenträger in der VMSS-Instanz umbildet.</span><span class="sxs-lookup"><span data-stu-id="18fbf-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="18fbf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fbf-119">-ResourceGroupName</span></span>
<span data-ttu-id="18fbf-120">Gibt den Namen der Ressourcengruppe an, die die VMSS-Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="18fbf-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="18fbf-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="18fbf-121">-VMScaleSetName</span></span>
<span data-ttu-id="18fbf-122">Gibt den Namen der VMSS-Instanz an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="18fbf-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="18fbf-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18fbf-123">-Confirm</span></span>
<span data-ttu-id="18fbf-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18fbf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18fbf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18fbf-125">-WhatIf</span></span>
<span data-ttu-id="18fbf-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18fbf-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18fbf-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18fbf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18fbf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fbf-128">CommonParameters</span></span>
<span data-ttu-id="18fbf-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fbf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fbf-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fbf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fbf-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18fbf-131">INPUTS</span></span>

## <span data-ttu-id="18fbf-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18fbf-132">OUTPUTS</span></span>

## <span data-ttu-id="18fbf-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="18fbf-133">NOTES</span></span>

## <span data-ttu-id="18fbf-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18fbf-134">RELATED LINKS</span></span>

[<span data-ttu-id="18fbf-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="18fbf-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
