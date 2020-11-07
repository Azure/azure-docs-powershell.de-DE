---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 7b9e6aa5a9879e0f7abb281810d80a6900198ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662951"
---
# <span data-ttu-id="9255d-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9255d-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="9255d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9255d-102">SYNOPSIS</span></span>
<span data-ttu-id="9255d-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="9255d-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9255d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9255d-104">SYNTAX</span></span>

### <span data-ttu-id="9255d-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9255d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9255d-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9255d-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9255d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9255d-107">DESCRIPTION</span></span>
<span data-ttu-id="9255d-108">Das Cmdlet **Start-AzureRmVM** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="9255d-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="9255d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9255d-109">EXAMPLES</span></span>

### <span data-ttu-id="9255d-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="9255d-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="9255d-111">Dieser Befehl startet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9255d-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="9255d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9255d-112">PARAMETERS</span></span>

### <span data-ttu-id="9255d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9255d-113">-AsJob</span></span>
<span data-ttu-id="9255d-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="9255d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9255d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9255d-115">-DefaultProfile</span></span>
<span data-ttu-id="9255d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9255d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9255d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="9255d-117">-Id</span></span>
<span data-ttu-id="9255d-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9255d-118">The resource group name.</span></span>

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

### <span data-ttu-id="9255d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9255d-119">-Name</span></span>
<span data-ttu-id="9255d-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9255d-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="9255d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9255d-121">-ResourceGroupName</span></span>
<span data-ttu-id="9255d-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9255d-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9255d-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9255d-123">-Confirm</span></span>
<span data-ttu-id="9255d-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9255d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9255d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9255d-125">-WhatIf</span></span>
<span data-ttu-id="9255d-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9255d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9255d-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9255d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9255d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9255d-128">CommonParameters</span></span>
<span data-ttu-id="9255d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9255d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9255d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9255d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9255d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9255d-131">INPUTS</span></span>

### <span data-ttu-id="9255d-132">Keine</span><span class="sxs-lookup"><span data-stu-id="9255d-132">None</span></span>
<span data-ttu-id="9255d-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9255d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9255d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9255d-134">OUTPUTS</span></span>

### <span data-ttu-id="9255d-135">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9255d-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="9255d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="9255d-136">NOTES</span></span>

## <span data-ttu-id="9255d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9255d-137">RELATED LINKS</span></span>

[<span data-ttu-id="9255d-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9255d-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9255d-139">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9255d-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="9255d-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9255d-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9255d-141">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9255d-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9255d-142">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9255d-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9255d-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9255d-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


