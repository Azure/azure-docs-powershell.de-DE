---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 8d2646c56a8ac659f5beeb6695dc2899fb2f2542
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850059"
---
# <span data-ttu-id="f926f-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f926f-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="f926f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f926f-102">SYNOPSIS</span></span>
<span data-ttu-id="f926f-103">Entfernt die VMAccess-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f926f-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f926f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f926f-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f926f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f926f-105">DESCRIPTION</span></span>
<span data-ttu-id="f926f-106">Das Cmdlet **Remove-AzureRmVMAccessExtension** entfernt die Virtual Machine Access-Erweiterung (Virtual Machine Access, VMAccess) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f926f-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="f926f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f926f-107">EXAMPLES</span></span>

## <span data-ttu-id="f926f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f926f-108">PARAMETERS</span></span>

### <span data-ttu-id="f926f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f926f-109">-DefaultProfile</span></span>
<span data-ttu-id="f926f-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f926f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f926f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f926f-111">-Force</span></span>
<span data-ttu-id="f926f-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f926f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f926f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f926f-113">-Name</span></span>
<span data-ttu-id="f926f-114">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f926f-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f926f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f926f-115">-ResourceGroupName</span></span>
<span data-ttu-id="f926f-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f926f-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f926f-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="f926f-117">-VMName</span></span>
<span data-ttu-id="f926f-118">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f926f-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f926f-119">Dieses Cmdlet entfernt VMAccess für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f926f-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f926f-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f926f-120">-Confirm</span></span>
<span data-ttu-id="f926f-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f926f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f926f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f926f-122">-WhatIf</span></span>
<span data-ttu-id="f926f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f926f-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f926f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f926f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f926f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f926f-125">CommonParameters</span></span>
<span data-ttu-id="f926f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f926f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f926f-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f926f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f926f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f926f-128">INPUTS</span></span>

### <span data-ttu-id="f926f-129">Keine</span><span class="sxs-lookup"><span data-stu-id="f926f-129">None</span></span>
<span data-ttu-id="f926f-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f926f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f926f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f926f-131">OUTPUTS</span></span>

### <span data-ttu-id="f926f-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f926f-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f926f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f926f-133">NOTES</span></span>

## <span data-ttu-id="f926f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f926f-134">RELATED LINKS</span></span>

[<span data-ttu-id="f926f-135">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f926f-135">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f926f-136">Satz-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f926f-136">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f926f-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f926f-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
