---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1e2dc6fe56cfaf182fb0614121ad9511edcfc2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483081"
---
# <span data-ttu-id="89e9b-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89e9b-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="89e9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="89e9b-103">Entfernt eine benutzerdefinierte Skripterweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="89e9b-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89e9b-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e9b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="89e9b-106">Das Cmdlet " **Remove-AzureRmVMCustomScriptExtension** " entfernt eine benutzerdefinierte Skript Virtual Machine-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="89e9b-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="89e9b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89e9b-107">EXAMPLES</span></span>

## <span data-ttu-id="89e9b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89e9b-108">PARAMETERS</span></span>

### <span data-ttu-id="89e9b-109">-Force</span><span class="sxs-lookup"><span data-stu-id="89e9b-109">-Force</span></span>
<span data-ttu-id="89e9b-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="89e9b-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89e9b-111">-Name</span><span class="sxs-lookup"><span data-stu-id="89e9b-111">-Name</span></span>
<span data-ttu-id="89e9b-112">Gibt den Namen der benutzerdefinierten Skripterweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="89e9b-112">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89e9b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e9b-113">-ResourceGroupName</span></span>
<span data-ttu-id="89e9b-114">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="89e9b-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="89e9b-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="89e9b-115">-VMName</span></span>
<span data-ttu-id="89e9b-116">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die benutzerdefinierte Skripterweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="89e9b-116">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="89e9b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89e9b-117">-Confirm</span></span>
<span data-ttu-id="89e9b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89e9b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e9b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e9b-119">-WhatIf</span></span>
<span data-ttu-id="89e9b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89e9b-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="89e9b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89e9b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e9b-122">CommonParameters</span></span>
<span data-ttu-id="89e9b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e9b-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e9b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e9b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89e9b-125">INPUTS</span></span>

### <span data-ttu-id="89e9b-126">Keine</span><span class="sxs-lookup"><span data-stu-id="89e9b-126">None</span></span>
<span data-ttu-id="89e9b-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="89e9b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89e9b-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89e9b-128">OUTPUTS</span></span>

## <span data-ttu-id="89e9b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="89e9b-129">NOTES</span></span>

## <span data-ttu-id="89e9b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89e9b-130">RELATED LINKS</span></span>

[<span data-ttu-id="89e9b-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89e9b-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="89e9b-132">Satz-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89e9b-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
