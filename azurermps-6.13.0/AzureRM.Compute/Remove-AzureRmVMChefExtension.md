---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: da19894751c7b653dbc70d606a44464973d9b38c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504486"
---
# <span data-ttu-id="015c8-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="015c8-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="015c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="015c8-102">SYNOPSIS</span></span>
<span data-ttu-id="015c8-103">Entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="015c8-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="015c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="015c8-104">SYNTAX</span></span>

### <span data-ttu-id="015c8-105">Linux</span><span class="sxs-lookup"><span data-stu-id="015c8-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="015c8-106">Windows</span><span class="sxs-lookup"><span data-stu-id="015c8-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="015c8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="015c8-107">DESCRIPTION</span></span>
<span data-ttu-id="015c8-108">Das Cmdlet **Remove-AzureVMChefExtension** entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="015c8-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="015c8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="015c8-109">EXAMPLES</span></span>

### <span data-ttu-id="015c8-110">Beispiel 1: Entfernen einer Chefkoch-Erweiterung von einem Windows-virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="015c8-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="015c8-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Windows-basierten virtuellen Computer mit dem Namen "WindowsVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="015c8-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="015c8-112">Beispiel 2: Entfernen einer Erweiterung des Chefkochs von einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="015c8-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="015c8-113">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Linux-basierten virtuellen Computer mit dem Namen "LinuxVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="015c8-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="015c8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="015c8-114">PARAMETERS</span></span>

### <span data-ttu-id="015c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015c8-115">-DefaultProfile</span></span>
<span data-ttu-id="015c8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="015c8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="015c8-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="015c8-117">-Linux</span></span>
<span data-ttu-id="015c8-118">Gibt an, dass dieses Cmdlet auf einen virtuellen Linux-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="015c8-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015c8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="015c8-119">-Name</span></span>
<span data-ttu-id="015c8-120">Gibt den Namen der Erweiterung des Chefkochs an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="015c8-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="015c8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="015c8-121">-ResourceGroupName</span></span>
<span data-ttu-id="015c8-122">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="015c8-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="015c8-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="015c8-123">-VMName</span></span>
<span data-ttu-id="015c8-124">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die Erweiterung "Chef" entfernt.</span><span class="sxs-lookup"><span data-stu-id="015c8-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="015c8-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="015c8-125">-Windows</span></span>
<span data-ttu-id="015c8-126">Gibt an, dass dieses Cmdlet auf einen virtuellen Windows-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="015c8-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015c8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="015c8-127">-Confirm</span></span>
<span data-ttu-id="015c8-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="015c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="015c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="015c8-129">-WhatIf</span></span>
<span data-ttu-id="015c8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="015c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="015c8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="015c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="015c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015c8-132">CommonParameters</span></span>
<span data-ttu-id="015c8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="015c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015c8-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="015c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015c8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="015c8-135">INPUTS</span></span>

### <span data-ttu-id="015c8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="015c8-136">System.String</span></span>

## <span data-ttu-id="015c8-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="015c8-137">OUTPUTS</span></span>

### <span data-ttu-id="015c8-138">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="015c8-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="015c8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="015c8-139">NOTES</span></span>

## <span data-ttu-id="015c8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="015c8-140">RELATED LINKS</span></span>

[<span data-ttu-id="015c8-141">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="015c8-141">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="015c8-142">Satz-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="015c8-142">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
