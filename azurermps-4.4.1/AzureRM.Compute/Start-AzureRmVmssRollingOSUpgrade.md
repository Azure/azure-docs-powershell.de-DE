---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 7f4e28c00b0238b519ad2b038676a295147b5c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500085"
---
# <span data-ttu-id="10926-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="10926-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="10926-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10926-102">SYNOPSIS</span></span>
<span data-ttu-id="10926-103">Startet ein paralleles Upgrade, um alle Scale-Instanzen von virtuellen Computern auf die neueste verfügbare Platt Form Abbild-Betriebssystemversion zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="10926-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10926-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10926-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10926-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10926-105">DESCRIPTION</span></span>
<span data-ttu-id="10926-106">Startet ein paralleles Upgrade, um alle Scale-Instanzen von virtuellen Computern auf die neueste verfügbare Platt Form Abbild-Betriebssystemversion zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="10926-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="10926-107">Instanzen, die bereits die neueste verfügbare Betriebssystemversion ausführen, sind davon nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="10926-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="10926-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10926-108">EXAMPLES</span></span>

### <span data-ttu-id="10926-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10926-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="10926-110">Mit diesem Befehl wird ein paralleles Upgrade aller VM-Instanzen des VM-Skalierungs Satzes "VMSS001" in der Ressourcengruppe "Group001" gestartet.</span><span class="sxs-lookup"><span data-stu-id="10926-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="10926-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="10926-111">PARAMETERS</span></span>

### <span data-ttu-id="10926-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10926-112">-DefaultProfile</span></span>
<span data-ttu-id="10926-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10926-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10926-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10926-114">-ResourceGroupName</span></span>
<span data-ttu-id="10926-115">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10926-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="10926-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="10926-116">-VMScaleSetName</span></span>
<span data-ttu-id="10926-117">Der Name der VM-Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="10926-117">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="10926-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="10926-118">-Confirm</span></span>
<span data-ttu-id="10926-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10926-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10926-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10926-120">-WhatIf</span></span>
<span data-ttu-id="10926-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10926-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10926-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10926-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10926-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10926-123">CommonParameters</span></span>
<span data-ttu-id="10926-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10926-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10926-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10926-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10926-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10926-126">INPUTS</span></span>

### <span data-ttu-id="10926-127">System. String</span><span class="sxs-lookup"><span data-stu-id="10926-127">System.String</span></span>

## <span data-ttu-id="10926-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10926-128">OUTPUTS</span></span>

### <span data-ttu-id="10926-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="10926-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="10926-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="10926-130">NOTES</span></span>

## <span data-ttu-id="10926-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10926-131">RELATED LINKS</span></span>

