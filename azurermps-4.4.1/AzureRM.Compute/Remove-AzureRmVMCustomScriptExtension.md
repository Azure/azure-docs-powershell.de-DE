---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 2d1edd8e511042f677928f171d7e31859cc5390f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477321"
---
# <span data-ttu-id="7f44e-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7f44e-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="7f44e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f44e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f44e-103">Entfernt eine benutzerdefinierte Skripterweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7f44e-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f44e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f44e-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f44e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f44e-105">DESCRIPTION</span></span>
<span data-ttu-id="7f44e-106">Das Cmdlet " **Remove-AzureRmVMCustomScriptExtension** " entfernt eine benutzerdefinierte Skript Virtual Machine-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7f44e-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="7f44e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f44e-107">EXAMPLES</span></span>

## <span data-ttu-id="7f44e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f44e-108">PARAMETERS</span></span>

### <span data-ttu-id="7f44e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f44e-109">-DefaultProfile</span></span>
<span data-ttu-id="7f44e-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f44e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f44e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7f44e-111">-Force</span></span>
<span data-ttu-id="7f44e-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7f44e-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f44e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7f44e-113">-Name</span></span>
<span data-ttu-id="7f44e-114">Gibt den Namen der benutzerdefinierten Skripterweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7f44e-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7f44e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f44e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7f44e-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7f44e-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7f44e-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="7f44e-117">-VMName</span></span>
<span data-ttu-id="7f44e-118">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die benutzerdefinierte Skripterweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f44e-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="7f44e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f44e-119">-Confirm</span></span>
<span data-ttu-id="7f44e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f44e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f44e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f44e-121">-WhatIf</span></span>
<span data-ttu-id="7f44e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f44e-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7f44e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f44e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f44e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f44e-124">CommonParameters</span></span>
<span data-ttu-id="7f44e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f44e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f44e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f44e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f44e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f44e-127">INPUTS</span></span>

## <span data-ttu-id="7f44e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f44e-128">OUTPUTS</span></span>

## <span data-ttu-id="7f44e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f44e-129">NOTES</span></span>

## <span data-ttu-id="7f44e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f44e-130">RELATED LINKS</span></span>

[<span data-ttu-id="7f44e-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7f44e-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="7f44e-132">Satz-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7f44e-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
