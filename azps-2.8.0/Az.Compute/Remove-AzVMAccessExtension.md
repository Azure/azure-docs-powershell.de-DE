---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 1fececa1c7d40e8ea2667ecd6461740a6714d744
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652007"
---
# <span data-ttu-id="604b2-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="604b2-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="604b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="604b2-102">SYNOPSIS</span></span>
<span data-ttu-id="604b2-103">Entfernt die VMAccess-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="604b2-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="604b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="604b2-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="604b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="604b2-105">DESCRIPTION</span></span>
<span data-ttu-id="604b2-106">Das Cmdlet **Remove-AzVMAccessExtension** entfernt die Virtual Machine Access-Erweiterung (Virtual Machine Access, VMAccess) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="604b2-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="604b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="604b2-107">EXAMPLES</span></span>

## <span data-ttu-id="604b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="604b2-108">PARAMETERS</span></span>

### <span data-ttu-id="604b2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604b2-109">-DefaultProfile</span></span>
<span data-ttu-id="604b2-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="604b2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="604b2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="604b2-111">-Force</span></span>
<span data-ttu-id="604b2-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="604b2-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="604b2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="604b2-113">-Name</span></span>
<span data-ttu-id="604b2-114">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="604b2-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="604b2-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="604b2-115">-NoWait</span></span>
<span data-ttu-id="604b2-116">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="604b2-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="604b2-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="604b2-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="604b2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="604b2-118">-ResourceGroupName</span></span>
<span data-ttu-id="604b2-119">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="604b2-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="604b2-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="604b2-120">-VMName</span></span>
<span data-ttu-id="604b2-121">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="604b2-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="604b2-122">Dieses Cmdlet entfernt VMAccess für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="604b2-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="604b2-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="604b2-123">-Confirm</span></span>
<span data-ttu-id="604b2-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="604b2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="604b2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="604b2-125">-WhatIf</span></span>
<span data-ttu-id="604b2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="604b2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="604b2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="604b2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="604b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604b2-128">CommonParameters</span></span>
<span data-ttu-id="604b2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="604b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604b2-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="604b2-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604b2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="604b2-131">INPUTS</span></span>

### <span data-ttu-id="604b2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="604b2-132">System.String</span></span>

## <span data-ttu-id="604b2-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="604b2-133">OUTPUTS</span></span>

### <span data-ttu-id="604b2-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="604b2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="604b2-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="604b2-135">NOTES</span></span>

## <span data-ttu-id="604b2-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="604b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="604b2-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="604b2-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="604b2-138">Satz-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="604b2-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="604b2-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="604b2-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
