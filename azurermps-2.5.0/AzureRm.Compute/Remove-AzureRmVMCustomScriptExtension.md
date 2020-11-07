---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850051"
---
# <span data-ttu-id="8a85e-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8a85e-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="8a85e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a85e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a85e-103">Entfernt eine benutzerdefinierte Skripterweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8a85e-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a85e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a85e-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a85e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a85e-105">DESCRIPTION</span></span>
<span data-ttu-id="8a85e-106">Das Cmdlet " **Remove-AzureRmVMCustomScriptExtension** " entfernt eine benutzerdefinierte Skript Virtual Machine-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8a85e-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="8a85e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a85e-107">EXAMPLES</span></span>

## <span data-ttu-id="8a85e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a85e-108">PARAMETERS</span></span>

### <span data-ttu-id="8a85e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a85e-109">-DefaultProfile</span></span>
<span data-ttu-id="8a85e-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a85e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a85e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8a85e-111">-Force</span></span>
<span data-ttu-id="8a85e-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8a85e-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a85e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8a85e-113">-Name</span></span>
<span data-ttu-id="8a85e-114">Gibt den Namen der benutzerdefinierten Skripterweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8a85e-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a85e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a85e-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a85e-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8a85e-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8a85e-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="8a85e-117">-VMName</span></span>
<span data-ttu-id="8a85e-118">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die benutzerdefinierte Skripterweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="8a85e-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="8a85e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a85e-119">-Confirm</span></span>
<span data-ttu-id="8a85e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a85e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a85e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a85e-121">-WhatIf</span></span>
<span data-ttu-id="8a85e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a85e-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8a85e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a85e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a85e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a85e-124">CommonParameters</span></span>
<span data-ttu-id="8a85e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a85e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a85e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a85e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a85e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a85e-127">INPUTS</span></span>

### <span data-ttu-id="8a85e-128">Keine</span><span class="sxs-lookup"><span data-stu-id="8a85e-128">None</span></span>
<span data-ttu-id="8a85e-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8a85e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a85e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a85e-130">OUTPUTS</span></span>

### <span data-ttu-id="8a85e-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8a85e-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8a85e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a85e-132">NOTES</span></span>

## <span data-ttu-id="8a85e-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a85e-133">RELATED LINKS</span></span>

[<span data-ttu-id="8a85e-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8a85e-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="8a85e-135">Satz-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8a85e-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
