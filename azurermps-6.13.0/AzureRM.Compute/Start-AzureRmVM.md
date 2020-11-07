---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 121d9353baaa10058e101d3f8a7d398f345052ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664090"
---
# <span data-ttu-id="da76f-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da76f-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="da76f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da76f-102">SYNOPSIS</span></span>
<span data-ttu-id="da76f-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="da76f-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da76f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da76f-104">SYNTAX</span></span>

### <span data-ttu-id="da76f-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="da76f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da76f-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="da76f-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da76f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da76f-107">DESCRIPTION</span></span>
<span data-ttu-id="da76f-108">Das Cmdlet **Start-AzureRmVM** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="da76f-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="da76f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da76f-109">EXAMPLES</span></span>

### <span data-ttu-id="da76f-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="da76f-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="da76f-111">Dieser Befehl startet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="da76f-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="da76f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="da76f-112">PARAMETERS</span></span>

### <span data-ttu-id="da76f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da76f-113">-AsJob</span></span>
<span data-ttu-id="da76f-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="da76f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="da76f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da76f-115">-DefaultProfile</span></span>
<span data-ttu-id="da76f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da76f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da76f-117">-ID</span><span class="sxs-lookup"><span data-stu-id="da76f-117">-Id</span></span>
<span data-ttu-id="da76f-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da76f-118">The resource group name.</span></span>

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

### <span data-ttu-id="da76f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="da76f-119">-Name</span></span>
<span data-ttu-id="da76f-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="da76f-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="da76f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da76f-121">-ResourceGroupName</span></span>
<span data-ttu-id="da76f-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="da76f-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="da76f-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da76f-123">-Confirm</span></span>
<span data-ttu-id="da76f-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da76f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da76f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da76f-125">-WhatIf</span></span>
<span data-ttu-id="da76f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da76f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da76f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da76f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da76f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da76f-128">CommonParameters</span></span>
<span data-ttu-id="da76f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da76f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da76f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da76f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da76f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da76f-131">INPUTS</span></span>

### <span data-ttu-id="da76f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="da76f-132">System.String</span></span>

## <span data-ttu-id="da76f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da76f-133">OUTPUTS</span></span>

### <span data-ttu-id="da76f-134">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="da76f-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="da76f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="da76f-135">NOTES</span></span>

## <span data-ttu-id="da76f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da76f-136">RELATED LINKS</span></span>

[<span data-ttu-id="da76f-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da76f-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="da76f-138">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da76f-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="da76f-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da76f-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="da76f-140">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da76f-140">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="da76f-141">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da76f-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="da76f-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da76f-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


