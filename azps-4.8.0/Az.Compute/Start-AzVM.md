---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008594"
---
# <span data-ttu-id="34e29-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="34e29-101">Start-AzVM</span></span>

## <span data-ttu-id="34e29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34e29-102">SYNOPSIS</span></span>
<span data-ttu-id="34e29-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="34e29-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="34e29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34e29-104">SYNTAX</span></span>

### <span data-ttu-id="34e29-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="34e29-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e29-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="34e29-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34e29-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34e29-107">DESCRIPTION</span></span>
<span data-ttu-id="34e29-108">Das Cmdlet **Start-AzVM** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="34e29-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="34e29-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34e29-109">EXAMPLES</span></span>

### <span data-ttu-id="34e29-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="34e29-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="34e29-111">Dieser Befehl startet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="34e29-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="34e29-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="34e29-112">PARAMETERS</span></span>

### <span data-ttu-id="34e29-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34e29-113">-AsJob</span></span>
<span data-ttu-id="34e29-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="34e29-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="34e29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e29-115">-DefaultProfile</span></span>
<span data-ttu-id="34e29-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34e29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e29-117">-ID</span><span class="sxs-lookup"><span data-stu-id="34e29-117">-Id</span></span>
<span data-ttu-id="34e29-118">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="34e29-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="34e29-119">-Name</span><span class="sxs-lookup"><span data-stu-id="34e29-119">-Name</span></span>
<span data-ttu-id="34e29-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="34e29-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="34e29-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="34e29-121">-NoWait</span></span>
<span data-ttu-id="34e29-122">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="34e29-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="34e29-123">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="34e29-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="34e29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e29-124">-ResourceGroupName</span></span>
<span data-ttu-id="34e29-125">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="34e29-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="34e29-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34e29-126">-Confirm</span></span>
<span data-ttu-id="34e29-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34e29-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e29-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e29-128">-WhatIf</span></span>
<span data-ttu-id="34e29-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34e29-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34e29-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34e29-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e29-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e29-131">CommonParameters</span></span>
<span data-ttu-id="34e29-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e29-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e29-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34e29-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e29-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34e29-134">INPUTS</span></span>

### <span data-ttu-id="34e29-135">System. String</span><span class="sxs-lookup"><span data-stu-id="34e29-135">System.String</span></span>

## <span data-ttu-id="34e29-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34e29-136">OUTPUTS</span></span>

### <span data-ttu-id="34e29-137">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="34e29-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="34e29-138">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="34e29-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="34e29-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="34e29-139">NOTES</span></span>

## <span data-ttu-id="34e29-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34e29-140">RELATED LINKS</span></span>

[<span data-ttu-id="34e29-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="34e29-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="34e29-142">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="34e29-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="34e29-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="34e29-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="34e29-144">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="34e29-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="34e29-145">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="34e29-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="34e29-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="34e29-146">Update-AzVM</span></span>](./Update-AzVM.md)


