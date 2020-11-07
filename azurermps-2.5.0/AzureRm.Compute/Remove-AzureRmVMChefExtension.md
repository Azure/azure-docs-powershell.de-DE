---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: bc8dbd023d8730922614f749f540d182c63237a4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850052"
---
# <span data-ttu-id="9f640-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9f640-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="9f640-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f640-102">SYNOPSIS</span></span>
<span data-ttu-id="9f640-103">Entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9f640-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f640-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f640-104">SYNTAX</span></span>

### <span data-ttu-id="9f640-105">Linux</span><span class="sxs-lookup"><span data-stu-id="9f640-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f640-106">Windows</span><span class="sxs-lookup"><span data-stu-id="9f640-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f640-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f640-107">DESCRIPTION</span></span>
<span data-ttu-id="9f640-108">Das Cmdlet **Remove-AzureVMChefExtension** entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9f640-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="9f640-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f640-109">EXAMPLES</span></span>

### <span data-ttu-id="9f640-110">Beispiel 1: Entfernen einer Chefkoch-Erweiterung von einem Windows-virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="9f640-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="9f640-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Windows-basierten virtuellen Computer mit dem Namen "WindowsVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="9f640-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="9f640-112">Beispiel 2: Entfernen einer Erweiterung des Chefkochs von einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="9f640-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="9f640-113">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Linux-basierten virtuellen Computer mit dem Namen "LinuxVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="9f640-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="9f640-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f640-114">PARAMETERS</span></span>

### <span data-ttu-id="9f640-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f640-115">-DefaultProfile</span></span>
<span data-ttu-id="9f640-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f640-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f640-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="9f640-117">-Linux</span></span>
<span data-ttu-id="9f640-118">Gibt an, dass dieses Cmdlet auf einen virtuellen Linux-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="9f640-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f640-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9f640-119">-Name</span></span>
<span data-ttu-id="9f640-120">Gibt den Namen der Erweiterung des Chefkochs an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9f640-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f640-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f640-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f640-122">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="9f640-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="9f640-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="9f640-123">-VMName</span></span>
<span data-ttu-id="9f640-124">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die Erweiterung "Chef" entfernt.</span><span class="sxs-lookup"><span data-stu-id="9f640-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="9f640-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="9f640-125">-Windows</span></span>
<span data-ttu-id="9f640-126">Gibt an, dass dieses Cmdlet auf einen virtuellen Windows-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="9f640-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f640-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f640-127">-Confirm</span></span>
<span data-ttu-id="9f640-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f640-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f640-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f640-129">-WhatIf</span></span>
<span data-ttu-id="9f640-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f640-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9f640-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f640-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f640-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f640-132">CommonParameters</span></span>
<span data-ttu-id="9f640-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f640-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f640-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f640-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f640-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f640-135">INPUTS</span></span>

### <span data-ttu-id="9f640-136">Keine</span><span class="sxs-lookup"><span data-stu-id="9f640-136">None</span></span>
<span data-ttu-id="9f640-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9f640-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f640-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f640-138">OUTPUTS</span></span>

### <span data-ttu-id="9f640-139">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9f640-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9f640-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f640-140">NOTES</span></span>

## <span data-ttu-id="9f640-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f640-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f640-142">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9f640-142">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="9f640-143">Satz-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9f640-143">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
