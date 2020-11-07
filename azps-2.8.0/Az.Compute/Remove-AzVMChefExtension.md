---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 8a64b97fb936daae2840392abe7dff8702207638
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652004"
---
# <span data-ttu-id="3f8cb-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3f8cb-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="3f8cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8cb-103">Entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="3f8cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f8cb-104">SYNTAX</span></span>

### <span data-ttu-id="3f8cb-105">Linux</span><span class="sxs-lookup"><span data-stu-id="3f8cb-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f8cb-106">Windows</span><span class="sxs-lookup"><span data-stu-id="3f8cb-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f8cb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f8cb-107">DESCRIPTION</span></span>
<span data-ttu-id="3f8cb-108">Das Cmdlet **Remove-AzVMChefExtension** entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="3f8cb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f8cb-109">EXAMPLES</span></span>

### <span data-ttu-id="3f8cb-110">Beispiel 1: Entfernen einer Chefkoch-Erweiterung von einem Windows-virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="3f8cb-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="3f8cb-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Windows-basierten virtuellen Computer mit dem Namen "WindowsVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="3f8cb-112">Beispiel 2: Entfernen einer Erweiterung des Chefkochs von einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="3f8cb-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="3f8cb-113">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Linux-basierten virtuellen Computer mit dem Namen "LinuxVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="3f8cb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f8cb-114">PARAMETERS</span></span>

### <span data-ttu-id="3f8cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8cb-115">-DefaultProfile</span></span>
<span data-ttu-id="3f8cb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f8cb-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="3f8cb-117">-Linux</span></span>
<span data-ttu-id="3f8cb-118">Gibt an, dass dieses Cmdlet auf einen virtuellen Linux-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="3f8cb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3f8cb-119">-Name</span></span>
<span data-ttu-id="3f8cb-120">Gibt den Namen der Erweiterung des Chefkochs an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f8cb-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3f8cb-121">-NoWait</span></span>
<span data-ttu-id="3f8cb-122">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3f8cb-123">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3f8cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f8cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f8cb-125">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="3f8cb-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="3f8cb-126">-VMName</span></span>
<span data-ttu-id="3f8cb-127">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die Erweiterung "Chef" entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="3f8cb-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="3f8cb-128">-Windows</span></span>
<span data-ttu-id="3f8cb-129">Gibt an, dass dieses Cmdlet auf einen virtuellen Windows-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="3f8cb-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f8cb-130">-Confirm</span></span>
<span data-ttu-id="3f8cb-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f8cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f8cb-132">-WhatIf</span></span>
<span data-ttu-id="3f8cb-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f8cb-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f8cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8cb-135">CommonParameters</span></span>
<span data-ttu-id="3f8cb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f8cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8cb-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f8cb-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8cb-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f8cb-138">INPUTS</span></span>

### <span data-ttu-id="3f8cb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3f8cb-139">System.String</span></span>

## <span data-ttu-id="3f8cb-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f8cb-140">OUTPUTS</span></span>

### <span data-ttu-id="3f8cb-141">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3f8cb-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3f8cb-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f8cb-142">NOTES</span></span>

## <span data-ttu-id="3f8cb-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f8cb-143">RELATED LINKS</span></span>

[<span data-ttu-id="3f8cb-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3f8cb-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="3f8cb-145">Satz-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3f8cb-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
