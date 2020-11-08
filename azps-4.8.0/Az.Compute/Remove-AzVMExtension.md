---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010001"
---
# <span data-ttu-id="d90d1-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d90d1-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="d90d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d90d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d90d1-103">Entfernt eine Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d90d1-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="d90d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90d1-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d90d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d90d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d90d1-106">Das Cmdlet " **Remove-AzVMExtension** " entfernt eine Erweiterung von den Virtual Machine-Erweiterungen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="d90d1-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="d90d1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d90d1-107">EXAMPLES</span></span>

### <span data-ttu-id="d90d1-108">Beispiel 1: Entfernen einer Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d90d1-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="d90d1-109">Dieser Befehl entfernt die Erweiterung mit dem Namen ContosoTest aus dem virtuellen Computer mit dem Namen VirtualMachine22 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d90d1-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="d90d1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d90d1-110">PARAMETERS</span></span>

### <span data-ttu-id="d90d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90d1-111">-DefaultProfile</span></span>
<span data-ttu-id="d90d1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d90d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d90d1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d90d1-113">-Force</span></span>
<span data-ttu-id="d90d1-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d90d1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d90d1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d90d1-115">-Name</span></span>
<span data-ttu-id="d90d1-116">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d90d1-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d90d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="d90d1-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d90d1-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d90d1-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="d90d1-119">-VMName</span></span>
<span data-ttu-id="d90d1-120">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="d90d1-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="d90d1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d90d1-121">-Confirm</span></span>
<span data-ttu-id="d90d1-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d90d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90d1-123">-WhatIf</span></span>
<span data-ttu-id="d90d1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d90d1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d90d1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d90d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90d1-126">CommonParameters</span></span>
<span data-ttu-id="d90d1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90d1-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d90d1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90d1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d90d1-129">INPUTS</span></span>

### <span data-ttu-id="d90d1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d90d1-130">System.String</span></span>

## <span data-ttu-id="d90d1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d90d1-131">OUTPUTS</span></span>

### <span data-ttu-id="d90d1-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d90d1-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d90d1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d90d1-133">NOTES</span></span>

## <span data-ttu-id="d90d1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d90d1-134">RELATED LINKS</span></span>

[<span data-ttu-id="d90d1-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d90d1-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="d90d1-136">Satz-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d90d1-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


