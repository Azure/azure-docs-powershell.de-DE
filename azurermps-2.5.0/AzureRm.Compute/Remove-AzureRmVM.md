---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f816be5d3c024e43074d6a75c5ba79df4b2fdb3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848887"
---
# <span data-ttu-id="06625-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06625-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="06625-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06625-102">SYNOPSIS</span></span>
<span data-ttu-id="06625-103">Entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="06625-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06625-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06625-104">SYNTAX</span></span>

### <span data-ttu-id="06625-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="06625-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06625-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="06625-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06625-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06625-107">DESCRIPTION</span></span>
<span data-ttu-id="06625-108">Das Cmdlet **Remove-AzureRmVM** entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="06625-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="06625-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06625-109">EXAMPLES</span></span>

### <span data-ttu-id="06625-110">Beispiel 1: Entfernen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="06625-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="06625-111">Dieser Befehl entfernt den virtuellen Computer mit dem Namen VirtualMachine07 in der Ressourcengruppe ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="06625-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="06625-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="06625-112">PARAMETERS</span></span>

### <span data-ttu-id="06625-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06625-113">-AsJob</span></span>
<span data-ttu-id="06625-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="06625-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="06625-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06625-115">-DefaultProfile</span></span>
<span data-ttu-id="06625-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06625-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06625-117">-Force</span><span class="sxs-lookup"><span data-stu-id="06625-117">-Force</span></span>
<span data-ttu-id="06625-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="06625-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06625-119">-ID</span><span class="sxs-lookup"><span data-stu-id="06625-119">-Id</span></span>
<span data-ttu-id="06625-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06625-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06625-121">-Name</span><span class="sxs-lookup"><span data-stu-id="06625-121">-Name</span></span>
<span data-ttu-id="06625-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="06625-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06625-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06625-123">-ResourceGroupName</span></span>
<span data-ttu-id="06625-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="06625-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06625-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06625-125">-Confirm</span></span>
<span data-ttu-id="06625-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06625-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06625-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06625-127">-WhatIf</span></span>
<span data-ttu-id="06625-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06625-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="06625-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06625-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06625-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06625-130">CommonParameters</span></span>
<span data-ttu-id="06625-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06625-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06625-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06625-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06625-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06625-133">INPUTS</span></span>

### <span data-ttu-id="06625-134">Keine</span><span class="sxs-lookup"><span data-stu-id="06625-134">None</span></span>
<span data-ttu-id="06625-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="06625-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06625-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06625-136">OUTPUTS</span></span>

### <span data-ttu-id="06625-137">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="06625-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="06625-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="06625-138">NOTES</span></span>

## <span data-ttu-id="06625-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06625-139">RELATED LINKS</span></span>

[<span data-ttu-id="06625-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06625-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="06625-141">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06625-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="06625-142">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06625-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="06625-143">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06625-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="06625-144">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06625-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="06625-145">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06625-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


