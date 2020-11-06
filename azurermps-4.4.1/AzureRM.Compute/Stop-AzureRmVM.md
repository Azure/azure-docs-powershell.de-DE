---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500081"
---
# <span data-ttu-id="b6946-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b6946-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="b6946-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6946-102">SYNOPSIS</span></span>
<span data-ttu-id="b6946-103">Beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="b6946-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6946-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6946-104">SYNTAX</span></span>

### <span data-ttu-id="b6946-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6946-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6946-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b6946-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6946-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6946-107">DESCRIPTION</span></span>
<span data-ttu-id="b6946-108">Das Cmdlet **Stop-AzureRmVM** beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="b6946-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="b6946-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6946-109">EXAMPLES</span></span>

### <span data-ttu-id="b6946-110">Beispiel 1: Beenden eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="b6946-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b6946-111">Dieser Befehl beendet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b6946-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b6946-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6946-112">PARAMETERS</span></span>

### <span data-ttu-id="b6946-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6946-113">-DefaultProfile</span></span>
<span data-ttu-id="b6946-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6946-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6946-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b6946-115">-Force</span></span>
<span data-ttu-id="b6946-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b6946-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6946-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b6946-117">-Id</span></span>
<span data-ttu-id="b6946-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b6946-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6946-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b6946-119">-Name</span></span>
<span data-ttu-id="b6946-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b6946-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6946-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6946-121">-ResourceGroupName</span></span>
<span data-ttu-id="b6946-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b6946-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6946-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="b6946-123">-StayProvisioned</span></span>
<span data-ttu-id="b6946-124">Das Cmdlet beendet alle virtuellen Computer innerhalb des VMSS, gibt diese jedoch nicht aus.</span><span class="sxs-lookup"><span data-stu-id="b6946-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="b6946-125">Das Konto wird für die angehalten virtuellen Computer berechnet.</span><span class="sxs-lookup"><span data-stu-id="b6946-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="b6946-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6946-126">-Confirm</span></span>
<span data-ttu-id="b6946-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6946-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6946-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6946-128">-WhatIf</span></span>
<span data-ttu-id="b6946-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6946-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6946-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6946-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6946-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6946-131">CommonParameters</span></span>
<span data-ttu-id="b6946-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6946-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6946-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6946-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6946-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6946-134">INPUTS</span></span>

## <span data-ttu-id="b6946-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6946-135">OUTPUTS</span></span>

## <span data-ttu-id="b6946-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6946-136">NOTES</span></span>

## <span data-ttu-id="b6946-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6946-137">RELATED LINKS</span></span>

[<span data-ttu-id="b6946-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b6946-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b6946-139">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b6946-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b6946-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b6946-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="b6946-141">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b6946-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="b6946-142">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b6946-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b6946-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b6946-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


