---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 131fec8efa9075640d367726e5178caa54b9402a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476182"
---
# <span data-ttu-id="c4d1e-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="c4d1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d1e-103">Startet die VMSS oder einen Satz virtueller Computer innerhalb des VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4d1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4d1e-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d1e-106">Mit dem **Start-AzureRmVmss-** Cmdlet werden alle virtuellen Computer im virtuellen Computer-Skalierungs Satz (VMSS) oder eine Gruppe virtueller Computer gestartet.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c4d1e-107">Sie können den *InstanceId* -Parameter verwenden, um einen Satz virtueller Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c4d1e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4d1e-108">EXAMPLES</span></span>

### <span data-ttu-id="c4d1e-109">Beispiel 1: Starten einer bestimmten Gruppe von virtuellen Computern innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="c4d1e-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="c4d1e-110">Mit diesem Befehl wird ein bestimmter Satz virtueller Computer gestartet, die durch das Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c4d1e-111">Beispiel 2: Starten aller virtuellen Computer innerhalb des VMSS</span><span class="sxs-lookup"><span data-stu-id="c4d1e-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c4d1e-112">Mit diesem Befehl werden alle virtuellen Computer gestartet, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c4d1e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4d1e-113">PARAMETERS</span></span>

### <span data-ttu-id="c4d1e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4d1e-114">-AsJob</span></span>
<span data-ttu-id="c4d1e-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c4d1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d1e-116">-DefaultProfile</span></span>
<span data-ttu-id="c4d1e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4d1e-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c4d1e-118">-InstanceId</span></span>
<span data-ttu-id="c4d1e-119">Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen an, die vom Cmdlet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="c4d1e-120">Zum Beispiel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="c4d1e-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4d1e-122">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c4d1e-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c4d1e-123">-VMScaleSetName</span></span>
<span data-ttu-id="c4d1e-124">Gibt den Namen des VMSS an, mit dem das Cmdlet die virtuellen Computer startet.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d1e-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4d1e-125">-Confirm</span></span>
<span data-ttu-id="c4d1e-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d1e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d1e-127">-WhatIf</span></span>
<span data-ttu-id="c4d1e-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4d1e-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d1e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d1e-130">CommonParameters</span></span>
<span data-ttu-id="c4d1e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d1e-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d1e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d1e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4d1e-133">INPUTS</span></span>

### <span data-ttu-id="c4d1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d1e-134">System.String</span></span>

### <span data-ttu-id="c4d1e-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="c4d1e-135">System.String[]</span></span>

## <span data-ttu-id="c4d1e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4d1e-136">OUTPUTS</span></span>

### <span data-ttu-id="c4d1e-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c4d1e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c4d1e-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4d1e-138">NOTES</span></span>

## <span data-ttu-id="c4d1e-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4d1e-139">RELATED LINKS</span></span>

[<span data-ttu-id="c4d1e-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c4d1e-141">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c4d1e-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c4d1e-143">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c4d1e-144">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c4d1e-145">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c4d1e-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4d1e-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


