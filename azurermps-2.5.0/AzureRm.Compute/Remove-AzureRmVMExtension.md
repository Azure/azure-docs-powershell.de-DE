---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: 835413728b22dd8bbb80d472eed71e0f4185db89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849740"
---
# <span data-ttu-id="866e3-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="866e3-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="866e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="866e3-102">SYNOPSIS</span></span>
<span data-ttu-id="866e3-103">Entfernt eine Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="866e3-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="866e3-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="866e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="866e3-105">DESCRIPTION</span></span>
<span data-ttu-id="866e3-106">Das Cmdlet " **Remove-AzureRmVMExtension** " entfernt eine Erweiterung von den Virtual Machine-Erweiterungen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="866e3-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="866e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="866e3-107">EXAMPLES</span></span>

### <span data-ttu-id="866e3-108">Beispiel 1: Entfernen einer Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="866e3-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="866e3-109">Dieser Befehl entfernt die Erweiterung mit dem Namen ContosoTest aus dem virtuellen Computer mit dem Namen VirtualMachine22 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="866e3-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="866e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="866e3-110">PARAMETERS</span></span>

### <span data-ttu-id="866e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866e3-111">-DefaultProfile</span></span>
<span data-ttu-id="866e3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="866e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="866e3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="866e3-113">-Force</span></span>
<span data-ttu-id="866e3-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="866e3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="866e3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="866e3-115">-Name</span></span>
<span data-ttu-id="866e3-116">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="866e3-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="866e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="866e3-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="866e3-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="866e3-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="866e3-119">-VMName</span></span>
<span data-ttu-id="866e3-120">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="866e3-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="866e3-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="866e3-121">-Confirm</span></span>
<span data-ttu-id="866e3-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="866e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866e3-123">-WhatIf</span></span>
<span data-ttu-id="866e3-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="866e3-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="866e3-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="866e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866e3-126">CommonParameters</span></span>
<span data-ttu-id="866e3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866e3-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866e3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="866e3-129">INPUTS</span></span>

### <span data-ttu-id="866e3-130">Keine</span><span class="sxs-lookup"><span data-stu-id="866e3-130">None</span></span>
<span data-ttu-id="866e3-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="866e3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="866e3-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="866e3-132">OUTPUTS</span></span>

### <span data-ttu-id="866e3-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="866e3-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="866e3-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="866e3-134">NOTES</span></span>

## <span data-ttu-id="866e3-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="866e3-135">RELATED LINKS</span></span>

[<span data-ttu-id="866e3-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="866e3-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="866e3-137">Satz-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="866e3-137">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


