---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652000"
---
# <span data-ttu-id="3f457-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f457-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="3f457-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f457-102">SYNOPSIS</span></span>
<span data-ttu-id="3f457-103">Entfernt eine benutzerdefinierte Skripterweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3f457-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="3f457-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f457-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f457-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f457-105">DESCRIPTION</span></span>
<span data-ttu-id="3f457-106">Das Cmdlet " **Remove-AzVMCustomScriptExtension** " entfernt eine benutzerdefinierte Skript Virtual Machine-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3f457-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="3f457-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f457-107">EXAMPLES</span></span>

## <span data-ttu-id="3f457-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f457-108">PARAMETERS</span></span>

### <span data-ttu-id="3f457-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f457-109">-DefaultProfile</span></span>
<span data-ttu-id="3f457-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f457-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f457-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3f457-111">-Force</span></span>
<span data-ttu-id="3f457-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3f457-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f457-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3f457-113">-Name</span></span>
<span data-ttu-id="3f457-114">Gibt den Namen der benutzerdefinierten Skripterweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3f457-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f457-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3f457-115">-NoWait</span></span>
<span data-ttu-id="3f457-116">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="3f457-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3f457-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3f457-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3f457-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f457-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f457-119">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3f457-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3f457-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="3f457-120">-VMName</span></span>
<span data-ttu-id="3f457-121">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die benutzerdefinierte Skripterweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f457-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="3f457-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f457-122">-Confirm</span></span>
<span data-ttu-id="3f457-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f457-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f457-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f457-124">-WhatIf</span></span>
<span data-ttu-id="3f457-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f457-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f457-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f457-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f457-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f457-127">CommonParameters</span></span>
<span data-ttu-id="3f457-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f457-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f457-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f457-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f457-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f457-130">INPUTS</span></span>

### <span data-ttu-id="3f457-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3f457-131">System.String</span></span>

## <span data-ttu-id="3f457-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f457-132">OUTPUTS</span></span>

### <span data-ttu-id="3f457-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3f457-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3f457-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f457-134">NOTES</span></span>

## <span data-ttu-id="3f457-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f457-135">RELATED LINKS</span></span>

[<span data-ttu-id="3f457-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f457-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="3f457-137">Satz-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f457-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
