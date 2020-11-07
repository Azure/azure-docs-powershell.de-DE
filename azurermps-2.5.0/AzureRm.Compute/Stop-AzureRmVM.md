---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4bf5ec5ccdbe79f5557cb2f400fbcc0b9baf5e5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850907"
---
# <span data-ttu-id="d92e2-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d92e2-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="d92e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d92e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d92e2-103">Beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="d92e2-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d92e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d92e2-104">SYNTAX</span></span>

### <span data-ttu-id="d92e2-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d92e2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d92e2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d92e2-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d92e2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d92e2-107">DESCRIPTION</span></span>
<span data-ttu-id="d92e2-108">Das Cmdlet **Stop-AzureRmVM** beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="d92e2-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="d92e2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d92e2-109">EXAMPLES</span></span>

### <span data-ttu-id="d92e2-110">Beispiel 1: Beenden eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="d92e2-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d92e2-111">Dieser Befehl beendet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d92e2-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="d92e2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d92e2-112">PARAMETERS</span></span>

### <span data-ttu-id="d92e2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d92e2-113">-AsJob</span></span>
<span data-ttu-id="d92e2-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="d92e2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d92e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92e2-115">-DefaultProfile</span></span>
<span data-ttu-id="d92e2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d92e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d92e2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d92e2-117">-Force</span></span>
<span data-ttu-id="d92e2-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d92e2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d92e2-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d92e2-119">-Id</span></span>
<span data-ttu-id="d92e2-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d92e2-120">The resource group name.</span></span>

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

### <span data-ttu-id="d92e2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d92e2-121">-Name</span></span>
<span data-ttu-id="d92e2-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d92e2-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d92e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="d92e2-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d92e2-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d92e2-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="d92e2-125">-StayProvisioned</span></span>
<span data-ttu-id="d92e2-126">Das Cmdlet beendet alle virtuellen Computer innerhalb des VMSS, gibt diese jedoch nicht aus.</span><span class="sxs-lookup"><span data-stu-id="d92e2-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="d92e2-127">Das Konto wird für die angehalten virtuellen Computer berechnet.</span><span class="sxs-lookup"><span data-stu-id="d92e2-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="d92e2-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d92e2-128">-Confirm</span></span>
<span data-ttu-id="d92e2-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d92e2-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92e2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92e2-130">-WhatIf</span></span>
<span data-ttu-id="d92e2-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d92e2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d92e2-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d92e2-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92e2-133">CommonParameters</span></span>
<span data-ttu-id="d92e2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d92e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92e2-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92e2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92e2-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d92e2-136">INPUTS</span></span>

### <span data-ttu-id="d92e2-137">Keine</span><span class="sxs-lookup"><span data-stu-id="d92e2-137">None</span></span>
<span data-ttu-id="d92e2-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d92e2-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d92e2-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d92e2-139">OUTPUTS</span></span>

### <span data-ttu-id="d92e2-140">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d92e2-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="d92e2-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d92e2-141">NOTES</span></span>

## <span data-ttu-id="d92e2-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d92e2-142">RELATED LINKS</span></span>

[<span data-ttu-id="d92e2-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d92e2-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d92e2-144">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d92e2-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="d92e2-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d92e2-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="d92e2-146">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d92e2-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="d92e2-147">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d92e2-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="d92e2-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d92e2-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


