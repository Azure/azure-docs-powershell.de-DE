---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
ms.openlocfilehash: 7f1cd0680d42ab83ec797b675e4505515a90548e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850896"
---
# <span data-ttu-id="46e0b-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="46e0b-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="46e0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="46e0b-103">Startet ein paralleles Upgrade, um alle Scale-Instanzen von virtuellen Computern auf die neueste verfügbare Platt Form Abbild-Betriebssystemversion zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="46e0b-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e0b-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="46e0b-106">Startet ein paralleles Upgrade, um alle Scale-Instanzen von virtuellen Computern auf die neueste verfügbare Platt Form Abbild-Betriebssystemversion zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="46e0b-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="46e0b-107">Instanzen, die bereits die neueste verfügbare Betriebssystemversion ausführen, sind davon nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="46e0b-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="46e0b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46e0b-108">EXAMPLES</span></span>

### <span data-ttu-id="46e0b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46e0b-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="46e0b-110">Mit diesem Befehl wird ein paralleles Upgrade aller VM-Instanzen des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" gestartet.</span><span class="sxs-lookup"><span data-stu-id="46e0b-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="46e0b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e0b-111">PARAMETERS</span></span>

### <span data-ttu-id="46e0b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46e0b-112">-AsJob</span></span>
<span data-ttu-id="46e0b-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="46e0b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46e0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e0b-114">-DefaultProfile</span></span>
<span data-ttu-id="46e0b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46e0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e0b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e0b-116">-ResourceGroupName</span></span>
<span data-ttu-id="46e0b-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46e0b-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="46e0b-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="46e0b-118">-VMScaleSetName</span></span>
<span data-ttu-id="46e0b-119">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="46e0b-119">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e0b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46e0b-120">-Confirm</span></span>
<span data-ttu-id="46e0b-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46e0b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e0b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e0b-122">-WhatIf</span></span>
<span data-ttu-id="46e0b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46e0b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e0b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46e0b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e0b-125">CommonParameters</span></span>
<span data-ttu-id="46e0b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e0b-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e0b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e0b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46e0b-128">INPUTS</span></span>

### <span data-ttu-id="46e0b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="46e0b-129">System.String</span></span>

## <span data-ttu-id="46e0b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46e0b-130">OUTPUTS</span></span>

### <span data-ttu-id="46e0b-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="46e0b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="46e0b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="46e0b-132">NOTES</span></span>

## <span data-ttu-id="46e0b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46e0b-133">RELATED LINKS</span></span>

