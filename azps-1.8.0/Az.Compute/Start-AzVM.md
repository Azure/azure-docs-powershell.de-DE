---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661421"
---
# <span data-ttu-id="b3035-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3035-101">Start-AzVM</span></span>

## <span data-ttu-id="b3035-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3035-102">SYNOPSIS</span></span>
<span data-ttu-id="b3035-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="b3035-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="b3035-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3035-104">SYNTAX</span></span>

### <span data-ttu-id="b3035-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3035-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3035-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b3035-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3035-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3035-107">DESCRIPTION</span></span>
<span data-ttu-id="b3035-108">Das Cmdlet **Start-AzVM** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="b3035-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="b3035-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3035-109">EXAMPLES</span></span>

### <span data-ttu-id="b3035-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="b3035-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b3035-111">Dieser Befehl startet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b3035-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b3035-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3035-112">PARAMETERS</span></span>

### <span data-ttu-id="b3035-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3035-113">-AsJob</span></span>
<span data-ttu-id="b3035-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="b3035-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3035-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3035-115">-DefaultProfile</span></span>
<span data-ttu-id="b3035-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3035-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3035-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b3035-117">-Id</span></span>
<span data-ttu-id="b3035-118">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b3035-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="b3035-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b3035-119">-Name</span></span>
<span data-ttu-id="b3035-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b3035-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3035-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3035-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3035-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b3035-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b3035-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3035-123">-Confirm</span></span>
<span data-ttu-id="b3035-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3035-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3035-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3035-125">-WhatIf</span></span>
<span data-ttu-id="b3035-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3035-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3035-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3035-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3035-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3035-128">CommonParameters</span></span>
<span data-ttu-id="b3035-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3035-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3035-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3035-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3035-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3035-131">INPUTS</span></span>

### <span data-ttu-id="b3035-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b3035-132">System.String</span></span>

## <span data-ttu-id="b3035-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3035-133">OUTPUTS</span></span>

### <span data-ttu-id="b3035-134">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b3035-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="b3035-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3035-135">NOTES</span></span>

## <span data-ttu-id="b3035-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3035-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3035-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3035-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b3035-138">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="b3035-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b3035-139">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3035-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b3035-140">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3035-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b3035-141">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3035-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b3035-142">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3035-142">Update-AzVM</span></span>](./Update-AzVM.md)


