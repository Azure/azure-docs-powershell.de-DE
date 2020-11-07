---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842476"
---
# <span data-ttu-id="87094-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="87094-101">Start-AzVM</span></span>

## <span data-ttu-id="87094-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87094-102">SYNOPSIS</span></span>
<span data-ttu-id="87094-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="87094-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="87094-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87094-104">SYNTAX</span></span>

### <span data-ttu-id="87094-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="87094-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87094-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="87094-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87094-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87094-107">DESCRIPTION</span></span>
<span data-ttu-id="87094-108">Das Cmdlet **Start-AzVM** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="87094-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="87094-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87094-109">EXAMPLES</span></span>

### <span data-ttu-id="87094-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="87094-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="87094-111">Dieser Befehl startet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="87094-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="87094-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87094-112">PARAMETERS</span></span>

### <span data-ttu-id="87094-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87094-113">-AsJob</span></span>
<span data-ttu-id="87094-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="87094-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="87094-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87094-115">-DefaultProfile</span></span>
<span data-ttu-id="87094-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87094-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87094-117">-ID</span><span class="sxs-lookup"><span data-stu-id="87094-117">-Id</span></span>
<span data-ttu-id="87094-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87094-118">The resource group name.</span></span>

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

### <span data-ttu-id="87094-119">-Name</span><span class="sxs-lookup"><span data-stu-id="87094-119">-Name</span></span>
<span data-ttu-id="87094-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="87094-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="87094-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87094-121">-ResourceGroupName</span></span>
<span data-ttu-id="87094-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="87094-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="87094-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87094-123">-Confirm</span></span>
<span data-ttu-id="87094-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87094-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87094-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87094-125">-WhatIf</span></span>
<span data-ttu-id="87094-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87094-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87094-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87094-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87094-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87094-128">CommonParameters</span></span>
<span data-ttu-id="87094-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87094-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87094-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87094-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87094-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87094-131">INPUTS</span></span>

### <span data-ttu-id="87094-132">Keine</span><span class="sxs-lookup"><span data-stu-id="87094-132">None</span></span>
<span data-ttu-id="87094-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="87094-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87094-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87094-134">OUTPUTS</span></span>

### <span data-ttu-id="87094-135">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="87094-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="87094-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="87094-136">NOTES</span></span>

## <span data-ttu-id="87094-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87094-137">RELATED LINKS</span></span>

[<span data-ttu-id="87094-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="87094-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="87094-139">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="87094-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="87094-140">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="87094-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="87094-141">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="87094-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="87094-142">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="87094-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="87094-143">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="87094-143">Update-AzVM</span></span>](./Update-AzVM.md)


