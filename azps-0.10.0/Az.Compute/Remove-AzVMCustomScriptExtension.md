---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844387"
---
# <span data-ttu-id="d95cd-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d95cd-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="d95cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d95cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d95cd-103">Entfernt eine benutzerdefinierte Skripterweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d95cd-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="d95cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d95cd-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d95cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d95cd-105">DESCRIPTION</span></span>
<span data-ttu-id="d95cd-106">Das Cmdlet " **Remove-AzVMCustomScriptExtension** " entfernt eine benutzerdefinierte Skript Virtual Machine-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d95cd-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="d95cd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d95cd-107">EXAMPLES</span></span>

## <span data-ttu-id="d95cd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d95cd-108">PARAMETERS</span></span>

### <span data-ttu-id="d95cd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95cd-109">-DefaultProfile</span></span>
<span data-ttu-id="d95cd-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d95cd-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d95cd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d95cd-111">-Force</span></span>
<span data-ttu-id="d95cd-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d95cd-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d95cd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d95cd-113">-Name</span></span>
<span data-ttu-id="d95cd-114">Gibt den Namen der benutzerdefinierten Skripterweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d95cd-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d95cd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d95cd-115">-ResourceGroupName</span></span>
<span data-ttu-id="d95cd-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d95cd-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d95cd-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="d95cd-117">-VMName</span></span>
<span data-ttu-id="d95cd-118">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die benutzerdefinierte Skripterweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="d95cd-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="d95cd-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d95cd-119">-Confirm</span></span>
<span data-ttu-id="d95cd-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d95cd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d95cd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d95cd-121">-WhatIf</span></span>
<span data-ttu-id="d95cd-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d95cd-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d95cd-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d95cd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d95cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95cd-124">CommonParameters</span></span>
<span data-ttu-id="d95cd-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95cd-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95cd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95cd-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d95cd-127">INPUTS</span></span>

### <span data-ttu-id="d95cd-128">Keine</span><span class="sxs-lookup"><span data-stu-id="d95cd-128">None</span></span>
<span data-ttu-id="d95cd-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d95cd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d95cd-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d95cd-130">OUTPUTS</span></span>

### <span data-ttu-id="d95cd-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d95cd-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d95cd-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d95cd-132">NOTES</span></span>

## <span data-ttu-id="d95cd-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d95cd-133">RELATED LINKS</span></span>

[<span data-ttu-id="d95cd-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d95cd-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="d95cd-135">Satz-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d95cd-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
