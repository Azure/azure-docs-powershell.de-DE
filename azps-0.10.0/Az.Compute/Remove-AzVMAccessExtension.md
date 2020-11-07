---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844400"
---
# <span data-ttu-id="223af-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="223af-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="223af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="223af-102">SYNOPSIS</span></span>
<span data-ttu-id="223af-103">Entfernt die VMAccess-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="223af-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="223af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="223af-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="223af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="223af-105">DESCRIPTION</span></span>
<span data-ttu-id="223af-106">Das Cmdlet **Remove-AzVMAccessExtension** entfernt die Virtual Machine Access-Erweiterung (Virtual Machine Access, VMAccess) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="223af-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="223af-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="223af-107">EXAMPLES</span></span>

## <span data-ttu-id="223af-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="223af-108">PARAMETERS</span></span>

### <span data-ttu-id="223af-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223af-109">-DefaultProfile</span></span>
<span data-ttu-id="223af-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="223af-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="223af-111">-Force</span><span class="sxs-lookup"><span data-stu-id="223af-111">-Force</span></span>
<span data-ttu-id="223af-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="223af-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="223af-113">-Name</span><span class="sxs-lookup"><span data-stu-id="223af-113">-Name</span></span>
<span data-ttu-id="223af-114">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="223af-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="223af-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="223af-115">-ResourceGroupName</span></span>
<span data-ttu-id="223af-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="223af-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="223af-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="223af-117">-VMName</span></span>
<span data-ttu-id="223af-118">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="223af-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="223af-119">Dieses Cmdlet entfernt VMAccess für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="223af-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="223af-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="223af-120">-Confirm</span></span>
<span data-ttu-id="223af-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="223af-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223af-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="223af-122">-WhatIf</span></span>
<span data-ttu-id="223af-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="223af-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="223af-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="223af-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223af-125">CommonParameters</span></span>
<span data-ttu-id="223af-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="223af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223af-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="223af-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223af-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="223af-128">INPUTS</span></span>

### <span data-ttu-id="223af-129">Keine</span><span class="sxs-lookup"><span data-stu-id="223af-129">None</span></span>
<span data-ttu-id="223af-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="223af-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="223af-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="223af-131">OUTPUTS</span></span>

### <span data-ttu-id="223af-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="223af-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="223af-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="223af-133">NOTES</span></span>

## <span data-ttu-id="223af-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="223af-134">RELATED LINKS</span></span>

[<span data-ttu-id="223af-135">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="223af-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="223af-136">Satz-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="223af-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="223af-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="223af-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
