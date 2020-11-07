---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844403"
---
# <span data-ttu-id="85754-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="85754-101">Remove-AzVM</span></span>

## <span data-ttu-id="85754-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85754-102">SYNOPSIS</span></span>
<span data-ttu-id="85754-103">Entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="85754-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="85754-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85754-104">SYNTAX</span></span>

### <span data-ttu-id="85754-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="85754-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85754-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="85754-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85754-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85754-107">DESCRIPTION</span></span>
<span data-ttu-id="85754-108">Das Cmdlet **Remove-AzVM** entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="85754-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="85754-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85754-109">EXAMPLES</span></span>

### <span data-ttu-id="85754-110">Beispiel 1: Entfernen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="85754-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="85754-111">Dieser Befehl entfernt den virtuellen Computer mit dem Namen VirtualMachine07 in der Ressourcengruppe ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="85754-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="85754-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="85754-112">PARAMETERS</span></span>

### <span data-ttu-id="85754-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85754-113">-AsJob</span></span>
<span data-ttu-id="85754-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="85754-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="85754-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85754-115">-DefaultProfile</span></span>
<span data-ttu-id="85754-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85754-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85754-117">-Force</span><span class="sxs-lookup"><span data-stu-id="85754-117">-Force</span></span>
<span data-ttu-id="85754-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="85754-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85754-119">-ID</span><span class="sxs-lookup"><span data-stu-id="85754-119">-Id</span></span>
<span data-ttu-id="85754-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85754-120">The resource group name.</span></span>

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

### <span data-ttu-id="85754-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85754-121">-Name</span></span>
<span data-ttu-id="85754-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="85754-122">The resource name.</span></span>

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

### <span data-ttu-id="85754-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85754-123">-ResourceGroupName</span></span>
<span data-ttu-id="85754-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="85754-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85754-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85754-125">-Confirm</span></span>
<span data-ttu-id="85754-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85754-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85754-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85754-127">-WhatIf</span></span>
<span data-ttu-id="85754-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85754-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="85754-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85754-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85754-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85754-130">CommonParameters</span></span>
<span data-ttu-id="85754-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85754-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85754-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85754-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85754-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85754-133">INPUTS</span></span>

### <span data-ttu-id="85754-134">Keine</span><span class="sxs-lookup"><span data-stu-id="85754-134">None</span></span>
<span data-ttu-id="85754-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="85754-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85754-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85754-136">OUTPUTS</span></span>

### <span data-ttu-id="85754-137">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="85754-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="85754-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="85754-138">NOTES</span></span>

## <span data-ttu-id="85754-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85754-139">RELATED LINKS</span></span>

[<span data-ttu-id="85754-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="85754-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="85754-141">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="85754-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="85754-142">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="85754-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="85754-143">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="85754-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="85754-144">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="85754-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="85754-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="85754-145">Update-AzVM</span></span>](./Update-AzVM.md)


